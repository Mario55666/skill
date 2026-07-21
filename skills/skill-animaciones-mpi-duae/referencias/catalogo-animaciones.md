# Catálogo de patrones — Animaciones Interactivas MPI-DUAE

Elige 1–3 patrones según lo que la unidad necesite hacer visible. Cada ficha indica el caso de uso, la fase de Kolb que activa, las opciones DUA que habilita y la técnica recomendada.

Leyenda Kolb: **EC** Experiencia Concreta · **OR** Observación Reflexiva · **CA** Conceptualización Abstracta · **EA** Experimentación Activa.

---

## 1. Reproductor paso a paso (procesos y secuencias)
- **Hace visible:** un proceso o procedimiento por etapas (algoritmo, técnica, flujo).
- **Kolb:** OR → CA.
- **Interacción:** botones Anterior/Siguiente, play/pausa, barra de pasos; cada paso resalta su parte y muestra una explicación.
- **DUA:** control total del ritmo; texto + visual por paso; navegable por teclado.
- **Técnica:** CSS transitions + JS de estado por paso; o WAAPI. Sin canvas.
- **Reflexión:** antes de avanzar, "¿qué crees que pasa ahora?".

## 2. Simulación con controles (relaciones entre variables)
- **Hace visible:** cómo una variable afecta a otra (causa-efecto, sistemas).
- **Kolb:** EA + EC.
- **Interacción:** sliders/toggles que actualizan en vivo la visualización; valores numéricos visibles.
- **DUA:** manipulación directa; muestra número + gráfico + etiqueta; teclado (flechas en el slider).
- **Creatividad:** fluidez/flexibilidad (probar combinaciones).
- **Técnica:** `input[type=range]` + actualización de `transform`/SVG; Canvas si hay muchas partículas.
- **Reflexión:** "predice el resultado, luego mueve el control".

## 3. Slider de comparación / capas conmutables (antes-después)
- **Hace visible:** contraste entre dos estados (buen/mal ejemplo, original/mejorado).
- **Kolb:** OR.
- **Interacción:** arrastrar el divisor o conmutar capas con un toggle.
- **DUA:** funciona con arrastre **y** con botones/teclado; etiquetas en ambos lados.
- **Técnica:** dos capas + `clip-path: inset()` controlado por la posición; sin librerías.

## 4. Diagrama interactivo (estructura / sistema / anatomía)
- **Hace visible:** las partes de un todo y sus relaciones.
- **Kolb:** CA.
- **Interacción:** hover/click/foco en una parte revela su nombre y función; resalta conexiones.
- **DUA:** disponible por hover **y** por foco de teclado; no depende del color para distinguir partes.
- **Técnica:** SVG con `<g>` por parte + `:focus`/`aria-describedby`.

## 5. Metáfora visual manipulable (conceptos abstractos)
- **Hace visible:** una idea intangible mediante un objeto manipulable (p. ej. "presupuesto = recipientes que se llenan").
- **Kolb:** EC → CA.
- **Interacción:** arrastrar, verter, agrupar, escalar; el sistema responde con la regla del concepto.
- **DUA:** arrastre con alternativa por botones; texto que nombra lo que ocurre.
- **Creatividad:** originalidad/elaboración.
- **Técnica:** drag por puntero + teclado (mover con flechas); estado en JS.

## 6. Scrollytelling (narrativa con datos o etapas)
- **Hace visible:** una historia o argumento donde el visual cambia al avanzar la lectura.
- **Kolb:** OR → CA.
- **Interacción:** al hacer scroll, cada sección dispara un cambio en una visual fija (sticky).
- **DUA:** **también navegable por enlaces/pasos** para quien no quiera scrollear; respeta movimiento reducido.
- **Técnica:** `IntersectionObserver` + `position: sticky`; transiciones de opacidad/transform.

## 7. Reveal progresiva / construcción guiada (definiciones y mapas)
- **Hace visible:** un esquema o mapa que se construye por partes.
- **Kolb:** CA.
- **Interacción:** clic/teclado añade el siguiente nodo; opción "mostrar todo".
- **DUA:** ritmo propio; texto + forma; sin dependencia de color.
- **Técnica:** lista de pasos + `@starting-style`/transición de opacidad.

## 8. Micro-interacción de comprobación (refuerzo dentro de la animación)
- **Hace visible:** si el estudiante captó la idea, con feedback inmediato.
- **Kolb:** EA → OR.
- **Interacción:** ordenar pasos, emparejar, ajustar hasta lograr la meta; respuesta R-E-A.
- **DUA:** varias formas de responder; reintentos; pista progresiva antes de la solución.
- **Técnica:** drag-and-drop accesible o botones; estado validado en JS.

---

## Tabla de selección rápida

| Necesidad de la unidad | Patrón | Kolb |
|---|---|---|
| Mostrar un proceso por etapas | 1 Paso a paso | OR→CA |
| Mostrar causa-efecto entre variables | 2 Simulación | EA, EC |
| Contrastar dos estados | 3 Comparación | OR |
| Explicar partes de un sistema | 4 Diagrama interactivo | CA |
| Explicar un concepto abstracto | 5 Metáfora manipulable | EC→CA |
| Contar una historia con datos | 6 Scrollytelling | OR→CA |
| Construir un esquema por partes | 7 Reveal progresiva | CA |
| Reforzar y comprobar comprensión | 8 Micro-comprobación | EA→OR |

**Regla:** combina **un patrón explicativo** (1–7) con **una micro-comprobación** (8) para cerrar el ciclo experiencial y reforzar con retroalimentación positiva.
