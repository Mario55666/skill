# Skill Animaciones Interactivas — MPI-DUAE (archivo único)

> Animaciones interactivas accesibles (HTML/CSS/JS) para enseñar y reforzar cualquier unidad didáctica en formato `.md`. Modelo: **MPI-DUAE** (DUA 3.0 con énfasis en Representación · ciclo experiencial de Kolb · competencias creativas de Torrance).

Reúne en un solo `.md` los cuatro componentes: (1) skill principal, (2) catálogo de patrones, (3) scaffold accesible y (4) ejemplo funcional.

---

# Parte 1 — Skill principal (SKILL.md)

---
name: skill-animaciones-mpi-duae
description: Convierte cualquier unidad didáctica en formato Markdown (*.md) en animaciones interactivas accesibles (HTML/CSS/JS) que explican y refuerzan los conceptos, alineadas con el Modelo Pedagógico Integrado DUA-Experiencial (MPI-DUAE). Úsalo cuando el usuario entregue una unidad, sesión, sílabo o tema en .md y pida animaciones interactivas, visualizaciones animadas, explicadores, simulaciones, scrollytelling, manipulativos digitales o recursos visuales dinámicos para educación superior.
---

# Skill Animaciones Interactivas — MPI-DUAE

Diseña **animaciones interactivas accesibles** (HTML/CSS/JS, sin dependencias pesadas) que hacen visible y manipulable un concepto de cualquier unidad didáctica entregada en Markdown. La animación no es decoración: es un **medio de representación** que reduce la carga cognitiva, muestra procesos invisibles y permite al estudiante *experimentar* la idea.

El modelo de referencia es el **MPI-DUAE** (Modelo Pedagógico Integrado DUA-Experiencial):

1. **DUA 3.0** (CAST, 2024) — con énfasis en **Representación** (mostrar el contenido de varias formas) y en **Implicación** (interacción que engancha), sin descuidar **Acción y Expresión**.
2. **Aprendizaje experiencial** (Kolb) — la interacción genera **Experiencia Concreta** y **Experimentación Activa**; las pausas y preguntas provocan **Observación Reflexiva** y **Conceptualización**.
3. **Competencias creativas** (Torrance) — animaciones manipulables que invitan a explorar, combinar y crear.

Todo ello **protegiendo el bienestar y la accesibilidad**: `prefers-reduced-motion`, controles de reproducción, navegación por teclado, subtítulos/texto alternativo y ausencia de estímulos que provoquen ansiedad o sobrecarga sensorial.

## Cuándo se activa

Usa este skill cuando el usuario:
- Adjunte o referencie una **unidad, sesión, sílabo o tema en `.md`** y pida animarlo.
- Pida "animaciones interactivas", "visualización animada", "explicador", "simulación", "scrollytelling", "manipulativo digital", "infografía animada" o "recurso visual dinámico".
- Quiera convertir un proceso, una relación o un concepto abstracto en algo que se vea y se manipule.

## Respuesta inicial

Cuando se invoque el skill **sin una unidad adjunta**, responde solo con:

> Soy tu diseñador de **Animaciones Interactivas — MPI-DUAE**. Pásame la unidad didáctica en `.md` (o pega su contenido) y la convertiré en animaciones interactivas accesibles (HTML/CSS/JS), alineadas con DUA 3.0, el ciclo experiencial de Kolb y las competencias creativas. ¿Quieres un explicador animado, una simulación manipulable o un scrollytelling de toda la unidad?

No generes nada más hasta recibir el contenido o una indicación concreta.

## Flujo de trabajo

Sigue estos pasos en orden.

### 1. Leer y extraer la estructura de la unidad

Lee el `.md` e identifica (infiere y marca *[inferido]* lo que falte):

| Campo | Qué buscar |
|---|---|
| Unidad / tema | Título y propósito |
| Resultados de aprendizaje | Capacidades / competencias / logros |
| Conceptos clave | Lo que conviene **hacer visible** |
| Procesos / relaciones | Secuencias, causas-efectos, sistemas dinámicos |
| Nivel y modalidad | Semestre, presencial/híbrido/virtual, dispositivos |

### 2. Decidir QUÉ merece animarse

No todo se anima. Animar tiene sentido cuando hay (elige el caso y la mecánica en `referencias/catalogo-animaciones.md`):
- **Proceso / secuencia** → línea de tiempo o reproductor paso a paso.
- **Relación entre variables** → simulación con controles (sliders/toggles).
- **Comparación / antes-después** → slider de comparación o capas conmutables.
- **Estructura / sistema** → diagrama interactivo (hover/click revela partes).
- **Concepto abstracto** → metáfora visual manipulable.
- **Narrativa con datos** → scrollytelling.

Si el contenido es solo definiciones sueltas, **no fuerces una animación**: una reveal progresiva simple basta.

### 3. Seleccionar el patrón y mapear a Kolb

Elige 1–3 patrones del catálogo. Garantiza que la interacción genere **Experiencia Concreta** (manipular) y **Experimentación Activa** (probar "¿qué pasa si…?"), y que haya un momento de **reflexión** (una pregunta, una pausa, un "predice antes de ver").

### 4. Aplicar el filtro DUA 3.0 (obligatorio)

Cada animación debe cumplir la [Lista de verificación DUA](#lista-de-verificación-dua). Punto innegociable: **toda animación se puede pausar, repetir y entender sin depender del color ni del sonido, y respeta `prefers-reduced-motion`.**

### 5. Integrar retroalimentación positiva

Cuando la animación incluya una micro-interacción de comprobación (predecir, ordenar, ajustar), la respuesta debe seguir el patrón **R-E-A** (ver [Marco de retroalimentación positiva](#marco-de-retroalimentación-positiva)). Nunca un "incorrecto" seco: orienta con una pista visual.

### 6. Implementar con el scaffold accesible

Construye sobre **`referencias/plantilla-scaffold.html`**: un archivo HTML autocontenido con controles, accesibilidad y `prefers-reduced-motion` ya resueltos. Sigue las [Reglas técnicas](#reglas-técnicas-de-animación). Entrega HTML/CSS/JS **vanilla y autocontenido** salvo que el usuario pida un framework.

### 7. Entregar

Produce uno o varios archivos `.html` listos para abrir en el navegador, más una nota docente. Si el usuario lo pide, entrega también una versión empaquetada en `.md` con el código en bloques. Mantén el idioma del usuario (por defecto, español).

## Marco de retroalimentación positiva

Igual que en el resto del MPI-DUAE, cada mensaje de comprobación sigue **R-E-A**:
- **R — Reconocer** la estrategia: *"Ajustaste primero el contraste, buena lectura del problema."*
- **E — Especificar** qué pasó y por qué: *"al subirlo, el ojo encontró el foco; eso es jerarquía."*
- **A — Avanzar** con un paso accionable: *"prueba ahora bajar el secundario y observa el cambio."*

Reglas: lenguaje de proceso (no de talento fijo), el error es información, pista progresiva antes que la respuesta, y reintentos sin penalización.

## Lista de verificación DUA

**Implicación**
- [ ] El estudiante **controla** la animación (play/pausa/repetir/velocidad o paso a paso).
- [ ] Hay interacción significativa (manipular, predecir, comparar), no solo mirar.
- [ ] Permite explorar a ritmo propio; sin autoplay agresivo ni sonido forzado.

**Representación**
- [ ] El concepto se presenta en ≥2 formas (animación **+** texto/etiquetas; idealmente + audio/voz opcional).
- [ ] La información **no depende solo del color** (usa forma, texto, patrón).
- [ ] Subtítulos / texto alternativo / descripción del movimiento disponibles.
- [ ] Vocabulario y símbolos clarificados in situ.

**Acción y Expresión**
- [ ] Operable **por teclado** (tab/enter/flechas) y por puntero/táctil.
- [ ] Objetivos de toque ≥44×44 px; foco visible.
- [ ] Ofrece una vía alternativa si la interacción motriz fina es difícil.

## Reglas técnicas de animación

Heredadas de buenas prácticas de animación + accesibilidad:

1. **`prefers-reduced-motion` obligatorio.** Movimiento reducido = animaciones más suaves y breves o transiciones de opacidad/color en lugar de desplazamiento; **nunca cero información**.
   ```css
   @media (prefers-reduced-motion: reduce) {
     *, *::before, *::after { animation-duration: .01ms !important; transition-duration: .01ms !important; }
   }
   ```
2. **Anima solo `transform` y `opacity`** (GPU; evita reflow de `width/height/top/left`).
3. **Easing con intención:** entradas/salidas `ease-out`; movimiento en pantalla `ease-in-out`. Curvas fuertes, p. ej. `cubic-bezier(0.23,1,0.32,1)`. Nunca `ease-in` para UI.
4. **Duraciones cortas para UI** (<300 ms); las explicativas pueden durar más pero **siempre controlables**.
5. **Sin parpadeos**: nada que destelle más de 3 veces por segundo (riesgo fotosensible).
6. **Controles reales**: botón play/pausa, repetir y, cuando aplique, barra de progreso o pasos.
7. **Sin dependencias** salvo necesidad; CSS/SVG/Canvas/WAAPI nativos antes que librerías.
8. **Autocontenido**: un solo `.html` que funcione offline, sin build.

## Salvaguardas de bienestar e inclusión

- **Carga cognitiva:** una idea por animación; revela por capas, no todo a la vez.
- **Sin sorpresas ansiógenas:** nada de cuentas regresivas estresantes ni penalización por explorar.
- **Sensorial:** sin sonido automático; colores de contraste suficiente (WCAG AA); opción de tema claro/oscuro si es viable.
- **Pertenencia:** ejemplos y contextos cercanos al estudiante.
- **Neurodiversidad:** ritmo autorregulado, instrucciones claras y persistentes, posibilidad de repetir sin límite.

## Mapeo a competencias creativas

Las animaciones **manipulables** (simulaciones, "¿qué pasa si…?") ejercitan creatividad: declara cuál dimensión cuando aplique — **fluidez** (probar muchas combinaciones), **flexibilidad** (variar enfoques), **originalidad** (configuraciones poco usuales), **elaboración** (refinar un resultado).

## Archivos de referencia

- `referencias/catalogo-animaciones.md` — patrones de animación interactiva con su caso de uso, fase de Kolb, opciones DUA y técnica recomendada. **Léelo en el paso 2–3.**
- `referencias/plantilla-scaffold.html` — scaffold HTML accesible (controles + `prefers-reduced-motion` + teclado) sobre el cual construir. **Úsalo en el paso 6.**
- `ejemplos/ejemplo-animacion.html` — ejemplo completo y funcional de una animación interactiva MPI-DUAE.

## Principios irrenunciables

1. **Toda animación hace visible o manipulable un resultado de aprendizaje explícito de la unidad.**
2. **Toda animación se puede pausar y repetir, y respeta `prefers-reduced-motion`.**
3. **El significado nunca depende solo del color ni del sonido.**
4. **Es operable por teclado y por táctil.**
5. **Interacción significativa > espectáculo visual.** Si solo "se ve bonito", rediséñala.

---

# Parte 2 — Catálogo de patrones

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

---

# Parte 3 — Scaffold HTML accesible

```html
<!DOCTYPE html>
<!--
  Scaffold accesible — Animaciones Interactivas MPI-DUAE
  Reemplaza los marcadores [[...]] y la lógica del "escenario" por tu animación.
  Ya resuelto: controles play/pausa/repetir, navegación por pasos, teclado,
  prefers-reduced-motion, región de estado (aria-live) y subtítulo/descripción.
-->
<html lang="es">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>[[Título de la animación]]</title>
<style>
  :root{
    --bg:#0f1220; --panel:#1a1f35; --ink:#eef1f8; --muted:#aab2cf;
    --accent:#7aa2ff; --ok:#5ed6a0; --warn:#ffd166; --focus:#ffffff;
    --ease-out:cubic-bezier(.23,1,.32,1);
  }
  @media (prefers-color-scheme: light){
    :root{ --bg:#f5f7ff; --panel:#fff; --ink:#161a2b; --muted:#52607f; }
  }
  *{box-sizing:border-box}
  body{margin:0;font:16px/1.55 system-ui,Segoe UI,Roboto,sans-serif;background:var(--bg);color:var(--ink);padding:1.5rem}
  .wrap{max-width:760px;margin:auto}
  h1{font-size:1.4rem;margin:.2rem 0}
  .lead{color:var(--muted);margin:.2rem 0 1rem}
  .stage{position:relative;background:var(--panel);border-radius:16px;min-height:280px;
    display:grid;place-items:center;overflow:hidden;padding:1.5rem}
  /* ---- Demo: caja que se mueve por pasos (reemplázalo) ---- */
  .obj{width:84px;height:84px;border-radius:14px;background:var(--accent);
    transform:translateX(var(--x,-160px));transition:transform .5s var(--ease-out)}
  /* -------------------------------------------------------- */
  .caption{margin:.8rem 0;padding:.7rem .9rem;background:var(--panel);border-radius:10px;color:var(--ink)}
  .controls{display:flex;flex-wrap:wrap;gap:.5rem;margin:.8rem 0}
  button{min-height:44px;min-width:44px;padding:.5rem 1rem;border:0;border-radius:10px;
    background:var(--accent);color:#0b0e1a;font-weight:600;cursor:pointer;transition:transform .12s var(--ease-out)}
  button.secondary{background:transparent;color:var(--ink);border:1px solid var(--muted)}
  button:active{transform:scale(.97)}
  button:focus-visible{outline:3px solid var(--focus);outline-offset:2px}
  .progress{display:flex;gap:.4rem;margin:.5rem 0}
  .dot{width:12px;height:12px;border-radius:50%;background:var(--muted);opacity:.4}
  .dot[aria-current="step"]{opacity:1;background:var(--ok)}
  .feedback{min-height:1.5rem;margin-top:.5rem;color:var(--ok);font-weight:600}
  .sr-only{position:absolute;width:1px;height:1px;padding:0;margin:-1px;overflow:hidden;clip:rect(0,0,0,0);border:0}
  @media (prefers-reduced-motion: reduce){
    *,*::before,*::after{animation-duration:.01ms!important;transition-duration:.01ms!important}
  }
</style>
</head>
<body>
<main class="wrap">
  <h1>[[Título de la animación]]</h1>
  <p class="lead">[[Resultado de aprendizaje que esta animación hace visible]]</p>

  <!-- ESCENARIO: reemplaza por tu visual (SVG/Canvas/DOM) -->
  <section class="stage" aria-label="Animación interactiva">
    <div class="obj" id="obj"></div>
  </section>

  <!-- Indicador de pasos -->
  <div class="progress" id="progress" aria-hidden="true"></div>

  <!-- Subtítulo/descripción del paso (representación textual del movimiento) -->
  <p class="caption" id="caption">[[Descripción del paso 1]]</p>

  <!-- Controles -->
  <div class="controls">
    <button id="prev" class="secondary">◀ Anterior</button>
    <button id="play">▶ Reproducir</button>
    <button id="next">Siguiente ▶</button>
    <button id="replay" class="secondary">↻ Repetir</button>
  </div>

  <!-- Región de estado para lectores de pantalla -->
  <p class="feedback" id="feedback" aria-live="polite"></p>
  <p class="sr-only" id="liveStep" aria-live="polite"></p>
</main>

<script>
(() => {
  // ====== DATOS DE LA ANIMACIÓN (reemplaza) ======
  // Cada paso define el estado visual (x) y su descripción textual.
  const steps = [
    { x:-160, text:"[[Descripción del paso 1]]" },
    { x:0,    text:"[[Descripción del paso 2]]" },
    { x:160,  text:"[[Descripción del paso 3]]" },
  ];
  // ===============================================

  const obj=document.getElementById('obj');
  const caption=document.getElementById('caption');
  const live=document.getElementById('liveStep');
  const progress=document.getElementById('progress');
  let i=0, playing=false, timer=null;

  // construir indicadores de paso
  steps.forEach((_,k)=>{const d=document.createElement('span');d.className='dot';if(k===0)d.setAttribute('aria-current','step');progress.appendChild(d);});
  const dots=[...progress.children];

  function render(){
    const s=steps[i];
    obj.style.setProperty('--x', s.x+'px');     // <- reemplaza por tu render real
    caption.textContent=s.text;
    live.textContent=`Paso ${i+1} de ${steps.length}: ${s.text}`;
    dots.forEach((d,k)=>k===i?d.setAttribute('aria-current','step'):d.removeAttribute('aria-current'));
  }
  function go(n){ i=Math.max(0,Math.min(steps.length-1,n)); render(); }
  function next(){ if(i<steps.length-1) go(i+1); else stop(); }
  function play(){ playing=true; document.getElementById('play').textContent='⏸ Pausar';
    timer=setInterval(()=>{ if(i>=steps.length-1){stop();return;} next(); }, 1600); }
  function stop(){ playing=false; clearInterval(timer); document.getElementById('play').textContent='▶ Reproducir'; }

  document.getElementById('next').onclick=()=>{stop();next();};
  document.getElementById('prev').onclick=()=>{stop();go(i-1);};
  document.getElementById('play').onclick=()=>playing?stop():play();
  document.getElementById('replay').onclick=()=>{stop();go(0);};

  // teclado: flechas para navegar, espacio para play/pausa
  document.addEventListener('keydown',e=>{
    if(e.key==='ArrowRight'){stop();next();}
    else if(e.key==='ArrowLeft'){stop();go(i-1);}
    else if(e.key===' '){e.preventDefault();playing?stop():play();}
  });

  render();
})();
</script>
</body>
</html>
```

---

# Parte 4 — Ejemplo funcional (abrir en navegador)

```html
<!DOCTYPE html>
<!--
  EJEMPLO MPI-DUAE — Animación interactiva
  Unidad: "Fundamentos de la composición visual" (Diseño Gráfico, I semestre)
  Resultado de aprendizaje: aplicar jerarquía y contraste para ordenar una pieza.
  Patrones usados: 2 Simulación con controles + 8 Micro-comprobación con feedback R-E-A.
  Accesible: teclado, prefers-reduced-motion, aria-live, sin dependencia del color.
-->
<html lang="es">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>Crea jerarquía visual — Animación interactiva</title>
<style>
  :root{ --bg:#0f1220; --panel:#1a1f35; --ink:#eef1f8; --muted:#aab2cf;
    --accent:#7aa2ff; --ok:#5ed6a0; --warn:#ffd166; --ease:cubic-bezier(.23,1,.32,1); }
  @media (prefers-color-scheme: light){ :root{ --bg:#f5f7ff; --panel:#fff; --ink:#161a2b; --muted:#52607f; } }
  *{box-sizing:border-box}
  body{margin:0;font:16px/1.55 system-ui,Segoe UI,Roboto,sans-serif;background:var(--bg);color:var(--ink);padding:1.5rem}
  .wrap{max-width:820px;margin:auto}
  h1{font-size:1.4rem;margin:.2rem 0}
  .lead{color:var(--muted);margin:.2rem 0 1rem}
  .grid{display:grid;grid-template-columns:1.2fr .8fr;gap:1rem}
  @media(max-width:680px){.grid{grid-template-columns:1fr}}
  .stage{background:var(--panel);border-radius:16px;padding:1.4rem;min-height:300px;display:flex;flex-direction:column;justify-content:center;gap:.6rem;overflow:hidden}
  .poster{background:linear-gradient(135deg,#222a4d,#11152b);border-radius:12px;padding:1.4rem;border:1px solid #2a335c}
  .t-title{font-weight:800;letter-spacing:.5px;transition:font-size .4s var(--ease),opacity .4s var(--ease),transform .4s var(--ease)}
  .t-sub{color:var(--muted);transition:font-size .4s var(--ease),opacity .4s var(--ease)}
  .t-body{color:var(--muted);font-size:.92rem;margin-top:.4rem}
  .panel{background:var(--panel);border-radius:16px;padding:1.2rem}
  label{display:block;margin:.7rem 0 .2rem;font-weight:600}
  input[type=range]{width:100%;height:34px}
  .val{color:var(--accent);font-variant-numeric:tabular-nums}
  .controls{display:flex;flex-wrap:wrap;gap:.5rem;margin-top:1rem}
  button{min-height:44px;min-width:44px;padding:.55rem 1rem;border:0;border-radius:10px;background:var(--accent);color:#0b0e1a;font-weight:700;cursor:pointer;transition:transform .12s var(--ease)}
  button.sec{background:transparent;color:var(--ink);border:1px solid var(--muted)}
  button:active{transform:scale(.97)}
  button:focus-visible,input:focus-visible{outline:3px solid #fff;outline-offset:2px}
  .feedback{margin-top:.9rem;min-height:3.2rem;padding:.7rem .9rem;border-radius:10px;background:#0d1126;border:1px solid #2a335c}
  .feedback.ok{border-color:var(--ok)} .feedback.try{border-color:var(--warn)}
  .tag{display:inline-block;font-size:.78rem;border:1px solid var(--muted);border-radius:999px;padding:.05rem .55rem;margin-right:.3rem;color:var(--muted)}
  .sr-only{position:absolute;width:1px;height:1px;overflow:hidden;clip:rect(0,0,0,0)}
  @media (prefers-reduced-motion: reduce){*,*::before,*::after{animation-duration:.01ms!important;transition-duration:.01ms!important}}
</style>
</head>
<body>
<main class="wrap">
  <h1>Crea jerarquía visual</h1>
  <p class="lead">Ajusta el <strong>tamaño</strong> y el <strong>contraste</strong> del título hasta que el ojo sepa qué leer primero. Manipula, predice y observa.</p>

  <div class="grid">
    <!-- ESCENARIO -->
    <section class="stage" aria-label="Pieza gráfica en vivo">
      <div class="poster">
        <div class="t-title" id="title" style="font-size:20px;opacity:.6">FESTIVAL DE DISEÑO</div>
        <div class="t-sub" id="sub" style="font-size:16px">12 de octubre · Auditorio central</div>
        <p class="t-body">Charlas, talleres y muestra de portafolios para estudiantes de primer semestre.</p>
      </div>
      <p class="sr-only" id="liveState" aria-live="polite"></p>
    </section>

    <!-- CONTROLES (simulación) -->
    <section class="panel" aria-label="Controles de la composición">
      <label for="size">Tamaño del título: <span class="val" id="sizeVal">20</span> px</label>
      <input id="size" type="range" min="16" max="56" value="20" step="2" />

      <label for="contrast">Contraste del título: <span class="val" id="contrastVal">60</span> %</label>
      <input id="contrast" type="range" min="30" max="100" value="60" step="5" />

      <div class="controls">
        <button id="check">Comprobar jerarquía</button>
        <button id="reset" class="sec">↻ Reiniciar</button>
      </div>

      <!-- Micro-comprobación con retroalimentación R-E-A -->
      <div class="feedback" id="feedback" role="status" aria-live="polite">
        Mueve los controles y pulsa <strong>Comprobar</strong> cuando creas que el título manda.
      </div>
      <p style="margin:.6rem 0 0;font-size:.82rem;color:var(--muted)">
        Creatividad ejercitada: <span class="tag">flexibilidad</span><span class="tag">elaboración</span>
      </p>
    </section>
  </div>
</main>

<script>
(() => {
  const title=document.getElementById('title'), sub=document.getElementById('sub');
  const size=document.getElementById('size'), contrast=document.getElementById('contrast');
  const sizeVal=document.getElementById('sizeVal'), contrastVal=document.getElementById('contrastVal');
  const fb=document.getElementById('feedback'), live=document.getElementById('liveState');
  const subSize=16; // tamaño fijo del subtítulo, referencia de jerarquía

  function render(){
    const s=+size.value, c=+contrast.value;
    sizeVal.textContent=s; contrastVal.textContent=c;
    title.style.fontSize=s+'px';
    title.style.opacity=(c/100).toFixed(2);
    live.textContent=`Título a ${s} px y ${c}% de contraste; subtítulo a ${subSize} px.`;
  }

  // Retroalimentación positiva R-E-A (acierto / intento) con pista progresiva
  function check(){
    const s=+size.value, c=+contrast.value;
    const ratio=s/subSize;                 // jerarquía por tamaño
    const strong = ratio>=1.8 && c>=85;    // meta: título claramente dominante
    const partial= ratio>=1.4 && c>=70;
    if(strong){
      fb.className='feedback ok';
      fb.innerHTML="✅ <strong>Lograste la jerarquía.</strong> Subiste tamaño y contraste juntos, así el ojo cae primero en el título y luego en la fecha — eso es jerarquía. <em>Avanza:</em> prueba bajar el subtítulo y observa cuánto más limpio queda el recorrido visual.";
    } else if(partial){
      fb.className='feedback try';
      fb.innerHTML="🟡 <strong>Vas bien.</strong> El título ya destaca, pero compite un poco con el resto. <em>Pista:</em> ¿qué pasa si subes un poco más el contraste? El tamaño solo no basta si el color se mezcla con el fondo.";
    } else {
      fb.className='feedback try';
      fb.innerHTML="🟡 <strong>Buen punto de partida.</strong> Ahora mismo el ojo duda entre título y subtítulo. <em>Pista:</em> haz el título claramente más grande que el subtítulo (≈ el doble) y súbele el contraste para que aparezca primero.";
    }
  }

  size.addEventListener('input',render);
  contrast.addEventListener('input',render);
  document.getElementById('check').onclick=check;
  document.getElementById('reset').onclick=()=>{size.value=20;contrast.value=60;render();fb.className='feedback';fb.textContent='Mueve los controles y pulsa Comprobar cuando creas que el título manda.';};

  render();
})();
</script>
</body>
</html>
```
