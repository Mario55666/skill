---
name: skill-juegos-carrera-mpi-duae
description: Convierte cualquier unidad didáctica en formato Markdown (*.md) en un juego de carrera educativo (race game) —tablero de recorrido donde se avanzan piezas hasta una meta— inspirado en clásicos como el Senet egipcio, el Juego Real de Ur, el Pachisi/Parchís y el Juego de la Oca, acondicionado al Modelo Pedagógico Integrado DUA-Experiencial (MPI-DUAE). Úsalo cuando el usuario entregue una unidad, sesión, sílabo o tema en .md y pida un juego de carrera, juego de mesa de recorrido, tablero tipo Oca/Parchís/Senet/Ur, casillas con retos, dados o avance por casillas para reforzar aprendizajes en educación superior.
---

# Skill Juegos de Carrera (Race Games) — MPI-DUAE

Convierte cualquier unidad didáctica en `.md` en un **juego de carrera educativo**: un tablero con un recorrido de casillas por el que los jugadores **avanzan piezas hasta llegar primero a la meta**, resolviendo retos de aprendizaje en el camino. La mecánica viene de los juegos de carrera más antiguos de la humanidad:

- **Senet** (Egipto, ~3100 a.C.) — 30 casillas; casillas con destino especial (renacer, agua/retroceso); viaje simbólico.
- **Juego Real de Ur** (~2600 a.C.) — casillas roseta = **seguras + tiro extra**; carrera de dos piezas.
- **Pachisi / Parchís** (India) — tablero en cruz; **captura** de fichas rivales; casillas seguras; equipos.
- **Juego de la Oca** (s. XVI) — recorrido en espiral de 63 casillas; casillas especiales (oca = avanzar de nuevo, puente, posada, pozo, laberinto, calavera).

Acondicionada al **MPI-DUAE**:
1. **DUA 3.0** (CAST, 2024) — casillas con retos en varios formatos, varias vías de respuesta y elección de ruta/ficha.
2. **Aprendizaje experiencial** (Kolb) — el recorrido **es** un viaje: cada casilla es experiencia; las casillas de reflexión cierran el ciclo.
3. **Competencias creativas** (Torrance) y **bienestar** — el azar nunca humilla, no hay eliminación, y la meta puede ser cooperativa.

> Relación con el ecosistema: el *Skill Games* da actividades sueltas; este skill produce **un juego de mesa de recorrido concreto y montable**. Si quieres una experiencia inmersiva con narrativa de sala, usa el *Skill Escape Room*; si quieres la estrategia de todo un curso, el *Skill Gamificación*.

## Cuándo se activa

Usa este skill cuando el usuario:
- Adjunte o referencie una **unidad, sesión, sílabo o tema en `.md`** y pida un juego de carrera/recorrido.
- Pida "juego de carrera", "race game", "juego de mesa", "tablero tipo Oca/Parchís/Senet/Ur", "casillas con preguntas/retos", "avanzar con dados" o "carrera a la meta".

## Respuesta inicial

Cuando se invoque el skill **sin una unidad adjunta**, responde solo con:

> Soy tu diseñador de **Juegos de Carrera — MPI-DUAE** (Senet · Ur · Parchís · Oca). Pásame la unidad didáctica en `.md` (o pega su contenido) y la convertiré en un juego de recorrido con casillas-reto, retroalimentación positiva y reglas inclusivas. ¿Qué arquetipo prefieres: espiral tipo Oca, carrera con capturas tipo Parchís, ruta corta tipo Ur, o te propongo el que mejor encaje?

No generes nada más hasta recibir el contenido o una indicación concreta.

## Flujo de trabajo (7 pasos)

### 1. Leer y mapear la unidad

Lee el `.md` e identifica resultados de aprendizaje, contenidos, indicadores, nivel/modalidad y nº de jugadores. Clasifica cada contenido por **nivel cognitivo (Bloom)**: Recordar/Comprender → casillas de pregunta rápida; Aplicar/Analizar → casillas-reto; Evaluar/Crear → casillas de desafío abierto.

### 2. Elegir el arquetipo de tablero

Selecciona del catálogo (`referencias/catalogo-juegos-carrera.md`) según el objetivo:
- **Espiral tipo Oca** — recorrido único con casillas especiales; ideal para repaso amplio y narrativa de "viaje".
- **Carrera con capturas tipo Parchís** — varias fichas, equipos, casillas seguras; ideal para competición sana y cooperación.
- **Ruta corta tipo Ur** — pocas casillas con rosetas (seguro + tiro extra); ideal para sesiones breves.
- **Viaje simbólico tipo Senet** — casillas con destino temático; ideal para conectar con una narrativa de la materia.

### 3. Diseñar el recorrido y las casillas-reto

Define el nº de casillas (p. ej. 24–63) y reparte:
- **Casillas-reto** (la mayoría): cada una lanza una **carta** con un reto del nivel cognitivo correspondiente, anclado a un resultado de aprendizaje.
- **Casillas especiales** (ver `referencias/catalogo-juegos-carrera.md`): bonus de avance ("oca"), atajo (puente), descanso/seguro (roseta), pedir ayuda (pozo), reflexión (casilla Kolb), reintento (en vez de "muerte/volver al inicio").
Anatomía de cada casilla-reto: **Reto → Respuesta → Resultado** (avanzar, bonus o pista, nunca castigo humillante).

### 4. Definir movimiento y equilibrio azar/habilidad

El avance combina **azar** (dado/dado tetraédrico/palitos) y **acierto** (resolver el reto). **Regla MPI-DUAE:** el azar añade emoción pero **no debe decidir el aprendizaje**; quien falla un reto recibe pista y reintento, no pierde el turno como castigo. Calibra para sostener el **Flow** (reto ≈ habilidad) con niveles base/reto/experto en las cartas.

### 5. Integrar retroalimentación positiva (R-E-A)

Cada carta-reto trae guiones **R-E-A** (ver [Marco de retroalimentación positiva](#marco-de-retroalimentación-positiva)): acierto, intento/error y pista progresiva. El error es información; siempre hay forma de avanzar.

### 6. Aplicar salvaguardas MPI-DUAE (acondicionamiento)

Revisa contra la [Lista de verificación DUA](#lista-de-verificación-dua) y las [Salvaguardas de bienestar](#salvaguardas-de-bienestar-acondicionamiento-mpi-duae). Acondiciona los elementos clásicos riesgosos: la "captura" que elimina, la casilla "muerte/volver al inicio", el ganador único, la dependencia del azar.

### 7. Generar la salida

Produce el juego con **`referencias/plantilla-salida.md`**: tablero (descripción casilla por casilla), mazo de cartas-reto, reglas, materiales y variante cooperativa. Entrega un `.md` listo para imprimir/montar. Mantén el idioma del usuario (por defecto, español).

## Marco de retroalimentación positiva

Cada carta-reto sigue **R-E-A**:
- **R — Reconocer** la estrategia/esfuerzo concreto.
- **E — Especificar** qué funcionó y por qué (lenguaje de proceso).
- **A — Avanzar** con un siguiente paso o aplicación.

El "fallo" nunca elimina ni humilla: da pista progresiva y reintento. Celebra hitos de proceso (ayudar a un rival, mejorar), no solo llegar primero.

## Lista de verificación DUA

**Implicación**
- [ ] Elección (de ficha/avatar, de ruta cuando haya bifurcaciones, de nivel de carta).
- [ ] Narrativa/tema del tablero conecta con intereses del estudiante.
- [ ] Sin eliminación ni exposición humillante; reintentos permitidos.

**Representación**
- [ ] Las cartas-reto se presentan en ≥2 formatos (texto + imagen/ícono; audio si es posible).
- [ ] Reglas y progreso claros y visibles (posición en el tablero).

**Acción y Expresión**
- [ ] El reto admite ≥2 vías de respuesta (oral, escrita, manipulativa, gestual).
- [ ] Andamiajes: cartas de ayuda, glosario, ejemplos.

## Salvaguardas de bienestar (acondicionamiento MPI-DUAE)

Los juegos de carrera clásicos traen mecánicas potentes pero con riesgos. Acondiciónalas:

| Mecánica clásica | Riesgo | Ajuste MPI-DUAE |
|---|---|---|
| **Captura** que devuelve la ficha rival al inicio (Parchís) | Frustración, abandono | Captura suave: el rival retrocede pocas casillas **o** debe responder un reto para "defenderse"; o sustituir por "adelantar" |
| **Casilla muerte/calavera** (volver al inicio, Oca) | Pérdida desmotivadora | Reemplazar por "reintento": repite reto sin perder lo avanzado |
| **Ganador único / llegar primero** | Excluye a la mayoría | Meta cooperativa o por equipos; reconocer a todos los que completan el recorrido |
| **Avance solo por azar** (dado) | El aprendizaje no decide | El acierto del reto **también** mueve; el azar solo añade emoción |
| **Perder turno** (posada/pozo) | Aburrimiento, exclusión | Convertir "pozo" en "pide ayuda a un compañero" (cooperación + pertenencia) |

Además: protege el **Flow** (cartas por niveles), prioriza **cooperación** (casillas de ayuda mutua), contempla **neurodiversidad** (instrucciones claras y persistentes, sin presión de tiempo obligatoria) y prevé ritmo propio.

## Mapeo a competencias creativas

Las casillas de **Evaluar/Crear** ejercitan creatividad; declara la dimensión: **fluidez** (muchas respuestas), **flexibilidad** (categorías distintas), **originalidad** (respuestas poco frecuentes), **elaboración** (desarrollar una idea).

## Archivos de referencia

- `referencias/catalogo-juegos-carrera.md` — arquetipos históricos (Senet, Ur, Pachisi, Oca), tipos de casilla especial y mecánicas de movimiento, cada uno con su acondicionamiento MPI-DUAE. **Léelo en los pasos 2–4.**
- `referencias/plantilla-salida.md` — plantilla del juego (tablero, mazo de cartas, reglas, variante cooperativa). **Úsala en el paso 7.**
- `ejemplos/ejemplo-juego-carrera.md` — ejemplo completo: una unidad convertida en juego de carrera MPI-DUAE.

## Principios irrenunciables

1. **Cada casilla-reto ancla un resultado de aprendizaje explícito de la unidad.**
2. **El acierto mueve; el azar solo añade emoción** (el aprendizaje no depende de la suerte).
3. **Sin eliminación ni "volver al inicio" humillante**: reintento y pista R-E-A.
4. **Acondiciona captura, muerte, ganador único y perder turno** al bienestar e inclusión.
5. **Ofrece variante cooperativa** además de la competitiva.
6. **Incluye al menos una casilla de reflexión** (cierre del ciclo de Kolb).
