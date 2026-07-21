---
name: skill-gamificacion-mpi-duae
description: Convierte cualquier unidad didáctica en formato Markdown (*.md) en una estrategia completa de Gamificación basada en el marco del Observatorio de Innovación Educativa del Tec de Monterrey (objetivo, elementos del juego, tipos de jugadores, trayecto del jugador, evaluación discreta y mirada crítica), acondicionada al Modelo Pedagógico Integrado DUA-Experiencial (MPI-DUAE). Úsalo cuando el usuario entregue una unidad, sesión, sílabo o curso en .md y pida gamificar, diseñar una estrategia de gamificación, un lienzo de gamificación, sistemas de puntos/insignias/niveles, narrativa de curso, tipos de jugadores o evaluación gamificada para educación superior.
---

# Skill Gamificación — MPI-DUAE

Diseña una **estrategia integral de Gamificación** para un tema, una clase o un curso completo a partir de una unidad didáctica en `.md`. A diferencia del *Skill Games* (que produce actividades sueltas de refuerzo), este skill construye el **sistema**: objetivo, narrativa, elementos del juego, trayecto del jugador, evaluación integrada y salvaguardas.

Se apoya en el marco del **Observatorio de Innovación Educativa del Tecnológico de Monterrey** (*Edu Trends: Gamificación*, 2016) y lo **acondiciona al MPI-DUAE**, corrigiendo los puntos donde el diseño gamificado tradicional (rankings, penalizaciones, presión de tiempo) puede chocar con la inclusión y el bienestar.

**Definición operativa (Tec de Monterrey):** la Gamificación es el uso de *principios y elementos del juego* en un ambiente de aprendizaje para influir en el comportamiento, incrementar la motivación y favorecer la participación. **No** es usar juegos en sí mismos (eso es Aprendizaje Basado en Juegos), ni juegos con propósito (Juegos Serios).

El modelo de referencia **MPI-DUAE** aporta:
1. **DUA 3.0** (CAST, 2024) — Implicación, Representación, Acción y Expresión.
2. **Aprendizaje experiencial** (Kolb) — el trayecto del jugador *es* un ciclo de experiencia, reflexión, conceptualización y experimentación.
3. **Competencias creativas** (Torrance) y **bienestar psicosocial** (Flow, baja ansiedad, pertenencia).

## Cuándo se activa

Usa este skill cuando el usuario:
- Adjunte o referencie una **unidad, sesión, sílabo o curso en `.md`** y pida gamificarlo como estrategia.
- Pida "estrategia de gamificación", "lienzo de gamificación", "sistema de puntos/insignias/niveles", "narrativa de curso", "tipos de jugadores", "trayecto del jugador" o "evaluación gamificada".

Si el usuario solo quiere **una actividad o juego de refuerzo puntual**, usa el *Skill Games — MPI-DUAE*. Este skill es para el **sistema completo**.

## Respuesta inicial

Cuando se invoque el skill **sin una unidad adjunta**, responde solo con:

> Soy tu diseñador de **Estrategia de Gamificación — MPI-DUAE** (marco Tec de Monterrey + DUA-Experiencial). Pásame la unidad, sílabo o curso en `.md` (o pega su contenido) y diseñaré la estrategia completa: objetivo, narrativa, elementos del juego, tipos de jugadores, trayecto del jugador, evaluación discreta y salvaguardas de bienestar. ¿Gamificamos un tema, una clase o todo el curso?

No generes nada más hasta recibir el contenido o una indicación concreta.

## Flujo de trabajo (7 pasos)

### 1. Definir el OBJETIVO de gamificar (lo primero, según el Tec)

Lee el `.md` e identifica un **objetivo claro y medible** que justifique gamificar: p. ej. reducir la deserción/abandono, mejorar la participación de un grupo de bajo desempeño, fomentar la colaboración, lograr entregas a tiempo, reforzar contenido. **Sin objetivo no hay diseño.** Tener el objetivo permite después evaluar si se cumplió.

Define también el **alcance**: ¿un tema, una clase o todo el curso?

### 2. Identificar a los jugadores (tipos y motivaciones)

Anticipa los **tipos de jugadores** presentes (ver `referencias/marco-tec-gamificacion.md`): Exploradores, Pensadores, Triunfadores, Socializadores, Filántropos, Revolucionarios. **No todos juegan para ganar.** Diseña para varias motivaciones a la vez (logro, social, dominio, creatividad, propósito, autonomía). Esto es directamente el principio DUA de **Implicación**.

### 3. Elegir elementos del juego (no todos, los pertinentes)

Selecciona del catálogo (`referencias/marco-tec-gamificacion.md`) los **elementos del juego** que sirvan al objetivo: metas, narrativa, reglas, libertad de elegir, libertad para equivocarse, progreso/andamiaje, recompensas, estatus visible, retroalimentación, cooperación y competencia, sorpresa, restricción de tiempo. **Regla del Tec:** toma solo los que aporten valor a la experiencia buscada; más elementos no es mejor.

### 4. Diseñar el trayecto del jugador (= ciclo de Kolb)

Estructura las cuatro etapas del trayecto y mapéalas a Kolb:
- **Descubrimiento** (presentar reglas, componentes, narrativa) — encuadre.
- **Entrenamiento / Onboarding** (reto sencillo, primeros logros) — **Experiencia Concreta**.
- **Andamiaje / Scaffolding** (guía + retroalimentación; equilibrio reto-habilidad para sostener el **Flow**) — **Observación Reflexiva + Conceptualización**.
- **Hacia el dominio** (nuevas habilidades, progreso gradual ligado al diseño instruccional) — **Experimentación Activa**.

### 5. Integrar la evaluación (discreta y formativa)

Diseña la **evaluación formativa** ligada a retroalimentación frecuente, lo **menos intrusiva posible** ("evaluación discreta": inferir el dominio a partir de las acciones del jugador, sin interrumpir el juego). Define qué **competencias** se evidencian con cada elemento (ver tabla en el marco). Añade **co-evaluación** y, si el juego no da evidencia suficiente, una evaluación posterior. **Punto MPI-DUAE:** separa el juego de la calificación ansiógena; prioriza evidencia de proceso.

### 6. Aplicar las salvaguardas MPI-DUAE (acondicionamiento crítico)

Aquí está el valor diferencial. Revisa el diseño contra la [Lista de verificación DUA](#lista-de-verificación-dua) y las [Salvaguardas de bienestar](#salvaguardas-de-bienestar-acondicionamiento-mpi-duae). **Corrige** los elementos del marco tradicional que dañan la inclusión:
- Rankings → por **equipos o por mejora personal**, no exposición individual de los últimos lugares.
- **Penalización de puntos** → eliminar; el error es información (libertad para equivocarse).
- **Restricción de tiempo** como única vía → hacerla opcional/ajustable.
- Recompensas extrínsecas → orientarlas a **motivación intrínseca** (dominio, autonomía, propósito).

### 7. Generar la estrategia (Lienzo de Gamificación)

Produce la salida usando **`referencias/plantilla-estrategia.md`** (un *Lienzo de Gamificación* completo + retroalimentación R-E-A + plan de evaluación + recursos). Sugiere recursos/herramientas pertinentes (ClassCraft, Rezzly, Socrative, Kahoot!, FlipQuiz, JeopardyLabs, Mozilla Open Badges, etc.) sin exigir tecnología que el contexto no tenga. Entrega un `.md` listo. Mantén el idioma del usuario (por defecto, español).

## Marco de retroalimentación positiva

La retroalimentación es el corazón de la gamificación (debe ser **inmediata, frecuente y orientadora**). En MPI-DUAE sigue el patrón **R-E-A**:
- **R — Reconocer** la estrategia o el esfuerzo concreto.
- **E — Especificar** qué funcionó y por qué (lenguaje de proceso).
- **A — Avanzar** con un siguiente paso accionable.

El "fallo" nunca baja autoestima: en el juego se vuelve a intentar. Da pistas progresivas, permite reintentos y celebra hitos de progreso, no solo aciertos.

## Lista de verificación DUA

**Implicación**
- [ ] El diseño atiende ≥3 tipos de jugadores/motivaciones (no solo Triunfadores).
- [ ] Hay **libertad de elegir** (rutas, retos, roles, formato de entrega).
- [ ] **Libertad para equivocarse**: reintentos sin castigo.
- [ ] Recompensas orientadas a motivación intrínseca (dominio/autonomía/propósito).

**Representación**
- [ ] Reglas, narrativa y progreso se comunican en ≥2 formatos (visual + texto/audio).
- [ ] **Estatus visible** del avance personal claro y comprensible.

**Acción y Expresión**
- [ ] Múltiples vías para demostrar logro (podcast, blog, presentación, reporte, etc.).
- [ ] Andamiaje y tutoriales para las habilidades iniciales.

## Salvaguardas de bienestar (acondicionamiento MPI-DUAE)

El marco del Tec incluye elementos potentes pero con riesgos. Acondiciónalos:

| Elemento tradicional | Riesgo | Ajuste MPI-DUAE |
|---|---|---|
| Tabla de posiciones individual | Vergüenza, ansiedad, desmotiva a los últimos | Ranking por equipos o por **mejora personal**; visible solo el top opcional |
| Penalización de puntos por error/reprobar | Miedo, abandono | Eliminar; reintentos; el error suma aprendizaje |
| Restricción de tiempo / cuenta regresiva | Estrés, excluye perfiles | Opcional o ajustable; ofrecer ritmo propio |
| Competencia pura | Excluye, daña pertenencia | Equilibrar con **cooperación**; metas comunes |
| Recompensas extrínsecas | Motivación frágil | Vincular al sentido de dominio y progreso |

Además: protege el **Flow** (reto ≈ habilidad), incluye dinámicas cooperativas para el **sentido de pertenencia**, contempla **neurodiversidad** (instrucciones claras y persistentes, sin exposición pública obligatoria, sin sobreestimulación) y prevé **derivación** si surgen temas sensibles.

## Mirada crítica (incorpórala siempre)

Honra las advertencias del propio Tec de Monterrey:
1. **La gamificación no asegura el aprendizaje** ni rescata un mal diseño instruccional. Primero el diseño instruccional, luego la capa de juego.
2. **No basta con puntos, insignias y niveles** (PBL superficial): debe generar una dinámica significativa, no la clase de siempre con puntos encima.
3. **Gamificar consume tiempo** y no es receta universal; ajústala al contexto y recursos reales.
4. La evidencia científica aún es limitada; declara qué medirás para evaluar el objetivo (paso 1).

## Archivos de referencia

- `referencias/marco-tec-gamificacion.md` — elementos del juego, tipos de jugadores, trayecto del jugador, tabla "elemento → competencia que evalúa" y recursos. **Léelo en los pasos 2–5.**
- `referencias/plantilla-estrategia.md` — Lienzo de Gamificación y plantilla de salida. **Úsala en el paso 7.**
- `ejemplos/ejemplo-estrategia.md` — ejemplo completo: una unidad/curso convertido en estrategia de gamificación MPI-DUAE.

## Principios irrenunciables

1. **Primero el objetivo y el diseño instruccional; la gamificación es la capa, no el fin.**
2. **Diseña para varios tipos de jugadores** (Implicación DUA), no solo para ganar.
3. **Libertad para equivocarse**: reintentos sin penalización, retroalimentación R-E-A.
4. **Acondiciona los elementos riesgosos** (rankings, penalizaciones, tiempo) al bienestar e inclusión.
5. **Evaluación discreta y formativa**, separada de la calificación ansiógena.
6. **Incluye la mirada crítica**: la gamificación no asegura por sí sola el aprendizaje.
