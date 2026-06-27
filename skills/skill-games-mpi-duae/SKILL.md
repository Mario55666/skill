---
name: skill-games-mpi-duae
description: Convierte cualquier unidad didáctica en formato Markdown (*.md) en un conjunto de actividades gamificadas que refuerzan conocimientos mediante retroalimentación positiva, alineadas con el Modelo Pedagógico Integrado DUA-Experiencial (MPI-DUAE). Úsalo cuando el usuario entregue una unidad, sesión, sílabo o tema en .md y pida juegos, gamificación, actividades de refuerzo, retroalimentación formativa o adaptaciones inclusivas para educación superior.
---

# Skill Games — MPI-DUAE

Diseña **actividades gamificadas inclusivas** para reforzar el aprendizaje de cualquier unidad didáctica entregada en Markdown. La gamificación no es un adorno: es el vehículo para que el estudiante practique, reciba **retroalimentación positiva** y consolide la competencia sin la ansiedad de la evaluación tradicional.

El modelo de referencia es el **MPI-DUAE** (Modelo Pedagógico Integrado DUA-Experiencial), que articula tres tradiciones:

1. **DUA 3.0** (CAST, 2024) — múltiples medios de **Implicación**, **Representación** y **Acción y Expresión**.
2. **Aprendizaje experiencial** (Kolb) — ciclo de Experiencia → Reflexión → Conceptualización → Experimentación.
3. **Competencias creativas** (Torrance) — fluidez, flexibilidad, originalidad y elaboración.

Todo ello protegiendo el **bienestar psicosocial**: estado de *Flow*, reducción de la ansiedad evaluativa, compromiso académico y sentido de pertenencia.

## Cuándo se activa

Usa este skill cuando el usuario:
- Adjunte o referencie una **unidad didáctica, sesión de aprendizaje, sílabo o tema en `.md`** y pida gamificarla.
- Pida "juegos", "actividades de refuerzo", "gamificación", "retroalimentación positiva/formativa" o "adaptación DUA/inclusiva" de un contenido.
- Quiera convertir resultados de aprendizaje, capacidades o indicadores en dinámicas activas.

## Respuesta inicial

Cuando se invoque el skill **sin una unidad adjunta**, responde solo con:

> Soy tu diseñador de **Skill Games — MPI-DUAE**. Pásame la unidad didáctica en `.md` (o pega su contenido) y la transformaré en actividades gamificadas con retroalimentación positiva, alineadas con DUA 3.0, el ciclo experiencial de Kolb y las competencias creativas. ¿Quieres una sesión completa, un solo juego de refuerzo o un kit para toda la unidad?

No generes nada más hasta recibir el contenido o una indicación concreta.

## Flujo de trabajo

Sigue estos pasos en orden. No saltes el análisis: la calidad del juego depende de qué tan bien mapees la unidad.

### 1. Leer y extraer la estructura de la unidad

Lee el `.md` e identifica (si falta algún campo, infiérelo y márcalo como *[inferido]*):

| Campo | Qué buscar |
|---|---|
| Unidad / tema | Título y propósito de la unidad |
| Resultados de aprendizaje | Capacidades, competencias o logros esperados |
| Contenidos | Conceptos, procedimientos y actitudes a reforzar |
| Indicadores / evidencias | Cómo se demuestra el logro |
| Nivel y duración | Semestre, nº de sesiones, minutos disponibles |
| Recursos | Presencial / híbrido / virtual, materiales, plataforma |

### 2. Clasificar cada contenido por nivel cognitivo

Etiqueta cada contenido con su nivel (Bloom revisado): **Recordar, Comprender, Aplicar, Analizar, Evaluar, Crear**. El nivel determina la mecánica de juego apropiada (ver `referencias/catalogo-juegos.md`). Recordar/Comprender → juegos de reconocimiento rápido; Aplicar/Analizar → retos y simulaciones; Evaluar/Crear → desafíos abiertos y creativos.

### 3. Seleccionar mecánicas desde el catálogo

Consulta **`referencias/catalogo-juegos.md`** y elige 2–4 mecánicas que cubran distintos niveles cognitivos y distintos perfiles de estudiante. Asegura que el conjunto recorra el **ciclo de Kolb** (al menos una actividad de experiencia concreta, una de reflexión, una de conceptualización y una de experimentación).

### 4. Aplicar el filtro DUA 3.0 (obligatorio)

Cada actividad debe ofrecer **opciones**, no un único camino. Verifica con la lista de la sección [Lista de verificación DUA](#lista-de-verificación-dua). Si una actividad solo tiene una vía de participación, una sola forma de representar el contenido o una sola forma de responder, **rediséñala**.

### 5. Diseñar la retroalimentación positiva

Para cada actividad escribe los *guiones* de retroalimentación según el [Marco de retroalimentación positiva](#marco-de-retroalimentación-positiva). La retroalimentación se entrega **durante** el juego (no solo al final) y siempre orienta hacia la mejora, nunca etiqueta al estudiante.

### 6. Proteger el bienestar (Flow + inclusión)

Calibra dificultad para sostener el *Flow* (reto ≈ habilidad), elimina la exposición pública obligatoria, ofrece reintentos sin penalización y añade adaptaciones de neurodiversidad/accesibilidad. Ver [Salvaguardas de bienestar](#salvaguardas-de-bienestar-e-inclusión).

### 7. Generar la salida

Produce el kit usando la plantilla de **`referencias/plantilla-salida.md`**. Entrega un archivo `.md` listo para que el docente lo use en aula. Mantén el idioma del usuario (por defecto, español).

## Marco de retroalimentación positiva

La retroalimentación positiva del MPI-DUAE **no** es "decir que todo está bien". Es una práctica formativa que reduce la ansiedad y aumenta la persistencia. Cada mensaje sigue la estructura **R-E-A**:

- **R — Reconocer** el esfuerzo o la estrategia concreta (no la persona): *"Notaste el patrón que conecta los dos casos"*, no *"qué inteligente eres"*.
- **E — Especificar** qué funcionó y por qué, con lenguaje de proceso: *"al comparar antes de decidir, evitaste el error frecuente de…"*.
- **A — Avanzar** con un siguiente paso accionable y alcanzable: *"prueba ahora aplicarlo a un caso con datos incompletos"*.

Reglas:
- Habla de **estrategias y procesos**, no de talento fijo (mentalidad de crecimiento).
- Convierte el error en información: *"este intento te muestra que…"*. Nunca uses "mal", "incorrecto" a secas.
- Da retroalimentación **inmediata y específica** dentro del juego (pistas progresivas, no la respuesta directa).
- Permite **reintentos**; cada reintento es una nueva oportunidad de puntuar, no un castigo.
- Celebra hitos de proceso (intentos, mejoras, ayuda a un par), no solo aciertos.

Escribe, para cada actividad, al menos: un guion de acierto, un guion de error/intento y una pista progresiva.

## Lista de verificación DUA

Cada actividad debe marcar al menos una opción en **cada** principio:

**Implicación (el porqué del aprendizaje)**
- [ ] Ofrece elección (de rol, formato, nivel de reto o tema).
- [ ] Conecta con intereses reales / contexto del estudiante.
- [ ] Minimiza amenazas: sin ridículo público, reintentos permitidos.
- [ ] Apoya la autorregulación (metas visibles, autoevaluación).

**Representación (el qué del aprendizaje)**
- [ ] El contenido se presenta en ≥2 formatos (texto, imagen, audio, video, manipulativo).
- [ ] Vocabulario y símbolos clarificados.
- [ ] Activa conocimientos previos y resalta lo esencial.

**Acción y Expresión (el cómo del aprendizaje)**
- [ ] El estudiante puede responder de ≥2 maneras (oral, escrito, visual, gestual, digital).
- [ ] Ofrece andamiajes y herramientas de apoyo.
- [ ] Apoya la planificación y el seguimiento del progreso.

## Salvaguardas de bienestar e inclusión

- **Flow:** ajusta el reto al nivel; ofrece niveles "base / reto / experto" para que cada quien juegue en su zona óptima.
- **Ansiedad evaluativa:** separa el juego de la calificación sumativa; usa puntaje de práctica, no notas.
- **Sentido de pertenencia:** incluye dinámicas cooperativas (no solo competitivas) y roles donde todos aporten.
- **Neurodiversidad / accesibilidad:** permite participación sin exposición pública obligatoria; da instrucciones por escrito y en voz; evita tiempos rígidos como única opción; contempla descansos sensoriales.
- **Competición saludable:** prioriza el progreso personal sobre los rankings; si usas tablas, hazlas por equipos o por mejora individual.
- **Derivación:** si el contenido toca temas sensibles (salud mental, etc.), añade una nota para el docente sobre acompañamiento.

## Mapeo a competencias creativas

Cuando una actividad apunte a **Crear/Evaluar**, declara qué dimensión de creatividad (Torrance) ejercita para poder observarla:
- **Fluidez** — generar muchas ideas/respuestas.
- **Flexibilidad** — generar ideas de categorías distintas.
- **Originalidad** — ideas poco frecuentes / novedosas.
- **Elaboración** — desarrollar y detallar una idea.

## Archivos de referencia

- `referencias/catalogo-juegos.md` — catálogo de mecánicas gamificadas con su nivel cognitivo, fase de Kolb, opciones DUA y modo de retroalimentación. **Léelo en el paso 3.**
- `referencias/plantilla-salida.md` — plantilla del kit gamificado que debes producir. **Úsala en el paso 7.**
- `ejemplos/ejemplo-unidad-gamificada.md` — ejemplo completo: una unidad transformada en kit de Skill Games.

## Principios irrenunciables

1. **Toda actividad refuerza un resultado de aprendizaje explícito de la unidad.** Si no puedes nombrarlo, no la incluyas.
2. **Toda actividad ofrece opciones (DUA).** Un único camino no es DUA.
3. **Toda actividad lleva retroalimentación positiva escrita (R-E-A).**
4. **El juego protege el bienestar.** Si genera ansiedad o excluye, está mal diseñado.
5. **El error es parte del juego, no su fracaso.**
