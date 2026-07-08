---
name: svg-font-forge
description: Pipeline completo para generar fuentes TrueType/OpenType desde SVG en el navegador (editores de glifos como ForjaType). Usar cuando Mario pida importar SVG complejos a un editor de fuentes, exportar TTF/OTF, corregir dirección de contornos (winding), convertir arcos a Béziers, o depurar por qué una fuente exportada se ve rellena/invertida/deformada. NO usar para tipografía de UI (tamaños, jerarquía, font pairing) — para eso existe la skill "typography".
---

# SVG Font Forge — SVG complejo → fuente TrueType

Conocimiento operativo para editores de fuentes web (ForjaType:
`50Projects-HTML-CSS-JavaScript/Source-Code/ForjaType/index.html`). El modelo de
datos de referencia es: `path = {id, closed, commands:[{type:'M'|'L'|'Q'|'C', x, y,
cx, cy, c1x, c1y, c2x, c2y}]}` en coordenadas tipográficas (Y hacia arriba,
baseline en y=0, unitsPerEm=1000).

## Reglas de oro (los 7 errores clásicos)

1. **Comandos relativos**: `c/s/q/t/m/l/h/v` suman la posición actual a TODAS sus
   coordenadas, incluidos los puntos de control. Un parser que solo convierte el
   punto final deforma cualquier SVG optimizado con SVGO.
2. **Arcos `A/a`**: no existen en fuentes; convertir a cúbicas con parametrización
   endpoint→centro (W3C SVG F.6.5), segmentos ≤90°, factor `k=(4/3)·tan(Δθ/4)`.
   Ojo con flags compactos (`A5 5 0 0110 0`): los flags son UN carácter, hay que
   leerlos con un lexer, no con regex de números.
3. **Eje Y**: SVG crece hacia abajo, las fuentes hacia arriba. Mapear
   `fontY = (bboxMaxY − svgY) · escala` y alinear el mínimo al baseline (y=0).
4. **Escala**: ajustar la altura del dibujo a una métrica (capHeight para
   mayúsculas, xHeight para minúsculas) y redondear a unidades enteras del em.
5. **Transforms**: acumular la matriz `[a,b,c,d,e,f]` de padre a hijo
   (matrix/translate/scale/rotate/skewX/skewY) y aplicarla a anclas Y controles.
   Como los arcos ya son cúbicas, la transformación afín es exacta.
6. **Winding (regla nonzero)**: los agujeros (interior de "o", "A", "B") deben ir
   en dirección OPUESTA al contorno exterior. Algoritmo: aplanar cada contorno
   cerrado (muestrear Béziers), calcular área con la fórmula del polígono
   (shoelace) y profundidad de anidamiento con point-in-polygon; profundidad par
   → área positiva (CCW en Y-arriba), impar → negativa (CW). Invertir un contorno
   = recorrer comandos al revés intercambiando c1↔c2 en las cúbicas.
   **Aplicarlo también al exportar** glifos dibujados a mano.
7. **Multi-path**: importar TODOS los `<path>` y formas (`rect` con rx/ry,
   `circle`, `ellipse`, `line`, `polyline`, `polygon` — círculos con 4 cúbicas y
   KAPPA=0.5522847498), recorriendo grupos. Saltar `defs`, `clipPath`, `mask`,
   gradientes y `<text>`; contar `<use>` omitidos y avisar.

## Exportación TTF vs OTF

- **opentype.js (1.3.4) solo escribe CFF** (contornos cúbicos, contenedor OTTO).
  Nombrar ese archivo `.ttf` es incorrecto: es un `.otf`.
- Para **TrueType real** (tabla `glyf`, curvas cuadráticas) en el navegador:
  generar el OTF con opentype.js y convertirlo con **fonteditor-core** (MIT):
  `Font.create(otfBuffer,{type:'otf',hinting:false}).write({type:'ttf',toBuffer:true})`.
  fonteditor-core no publica bundle UMD: empaquetar `lib/main.js` con esbuild
  (`--bundle --format=iife --global-name=FontEditorCore
  --alias:@xmldom/xmldom=stub`, el stub devuelve `window.DOMParser`) e incrustarlo
  (~216 KB min). En ForjaType ya está incrustado junto con opentype.js.
- Metadatos: opentype.js ignora designer/description en el constructor; asignar
  `font.names.designer={en:...}` y `font.names.description={en:...}` antes de
  `toArrayBuffer()`.
- Siempre incluir `.notdef` (unicode 0) como primer glifo y validar que cada
  comando tenga x/y numéricos antes de exportar.
- Alternativa fuera del navegador: fontTools (Python, `cu2qu` para cúbica→
  cuadrática) o svg2ttf (Node, requiere fuente SVG intermedia).

## Cómo verificar (receta probada)

1. **Unitario (Node)**: exportar las funciones puras del motor
   (`parsePathData`, `arcToCubics`, `normalizeWinding`...) con un guard
   `if(typeof module!=='undefined')` y probar: relativos, reflexión S/T, flags
   compactos de arco, multi-subpath, notación científica, agujero anidado
   (área exterior >0, agujero <0, isla a profundidad 2 >0).
2. **E2E (Playwright)**: cargar el HTML por `file://`, llamar `importSVGPath()`
   con un SVG que combine grupo transformado + path con arcos/relativos +
   círculo interior + rect redondeado rotado; verificar nº de contornos, bbox
   (baseline≈0, techo≈capHeight) y signos de área. Luego `buildFont()` +
   conversión TTF y re-parsear con opentype.js: `outlinesFormat==='truetype'`
   y comandos `M,L,Q,Z` (sin `C`).
3. **Visual**: instalar el .ttf o cargarlo con `FontFace` y renderizar texto de
   prueba; un glifo "relleno donde debía haber hueco" = winding mal.

## Contexto del documento original

`forjatype1.html` contenía TRES copias del documento concatenadas; la copia 1
(la más completa: SVG import, kerning, capas, plantillas) usaba `drawPath`, que
solo estaba definida en las copias 2/3. Si se reconstruye desde una sola copia,
recuperar esa función. La versión corregida y verificada vive en
`Source-Code/ForjaType/index.html` (rama `claude/truetype-svg-support-wi6bfr`).
