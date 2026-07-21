---
name: skill-bazas-mpi-duae
description: Convierte cualquier unidad didáctica en formato Markdown (*.md) en un juego de cartas educativo basado en la mecánica de bazas (trick-taking) —jugar turnos sucesivos para llevarse el grupo de cartas de la mesa, con palos, triunfos y predicción de bazas—, acondicionado al Modelo Pedagógico Integrado DUA-Experiencial (MPI-DUAE). Úsalo cuando el usuario entregue una unidad, sesión, sílabo o tema en .md y pida un juego de cartas, naipes, bazas, comparar/jerarquizar conceptos, clasificar por categorías, argumentar cuál "gana" o trabajo en parejas para educación superior.
---

# Skill Bazas (Trick-taking) — MPI-DUAE

Convierte cualquier unidad didáctica en `.md` en un **juego de cartas de bazas**: los jugadores juegan por turnos una carta sobre la mesa y alguien se lleva la **baza** (el grupo de cartas jugado) según reglas de palo, **triunfo** y jerarquía. Educativamente, cada carta es un **concepto** con un valor/rango; ganar una baza significa **comparar, jerarquizar o relacionar conceptos correctamente y justificarlo**. Es ideal para clasificar (palos = categorías), priorizar (triunfos = excepciones/criterios) y argumentar.

Acondicionada al **MPI-DUAE**:
1. **DUA 3.0** — cartas con texto + imagen; varias vías de justificar; elección de qué carta jugar.
2. **Aprendizaje experiencial** (Kolb) — predecir bazas (EA), jugarlas (EC), revisar por qué se ganó (OR), formular el criterio (CA).
3. **Competencias creativas** y **argumentación** (Evaluar de Bloom: justificar por qué una carta "gana").
4. **Bienestar e inclusión** — juego en **parejas/cooperativo** (pertenencia), sin eliminación; gana el **razonamiento**, no la suerte del reparto.

> Relación con el ecosistema: aquí la mecánica es de **cartas/comparación**. Si quieres un tablero de recorrido usa *Juegos de Carrera*; para azar puro, *Dados / Azar*.

## Cuándo se activa

Usa este skill cuando el usuario adjunte una **unidad en `.md`** y pida un juego de cartas/naipes, bazas, comparar/jerarquizar conceptos, clasificar por categorías, argumentar cuál "gana" o trabajo en parejas.

## Respuesta inicial

Cuando se invoque el skill **sin una unidad adjunta**, responde solo con:

> Soy tu diseñador de **Bazas / Trick-taking — MPI-DUAE**. Pásame la unidad didáctica en `.md` (o pega su contenido) y la convertiré en un juego de cartas donde cada carta es un concepto y se gana la baza **razonando** por qué tu carta es la más pertinente, con retroalimentación positiva y juego en parejas. ¿Quieres trabajar clasificación, jerarquía/priorización o argumentación?

No generes nada más hasta recibir el contenido.

## Flujo de trabajo

1. **Mapear la unidad** — resultados de aprendizaje, contenidos por nivel de Bloom, nivel/modalidad.
2. **Diseñar la baraja** (ver `referencias/catalogo-bazas.md`): **palos = categorías** del tema; **valores/rango = criterio** (importancia, cronología, magnitud…); **triunfo = excepción o criterio prioritario**.
3. **Definir cómo se gana la baza** — no solo por la carta más alta, sino **justificando** por qué esa carta es la más pertinente para la consigna de la ronda (reto de Evaluar).
4. **Añadir la predicción (bidding)** opcional — cada jugador predice cuántas bazas ganará: metacognición/autorregulación.
5. **Retroalimentación positiva (R-E-A)** en cada baza (acierto del razonamiento, intento, pista).
6. **Salvaguardas MPI-DUAE** — parejas/cooperativo, sin eliminación, el reparto no decide el aprendizaje.
7. **Generar la salida** con `referencias/plantilla-salida.md`.

## Marco de retroalimentación positiva

Cada baza sigue **R-E-A**: **R**econocer el criterio usado · **E**specificar por qué esa carta gana según la consigna · **A**vanzar. Perder una baza es información ("tu carta era válida en otra categoría"); pista progresiva + reintento.

## Lista de verificación DUA

- [ ] **Implicación:** elección de qué carta jugar y cómo justificar; juego en parejas; sin eliminación.
- [ ] **Representación:** cartas con texto + ícono/imagen; palos y triunfo claros; reglas graduales.
- [ ] **Acción y Expresión:** la justificación se admite oral, escrita o mostrando; andamiajes (carta de criterios).

## Salvaguardas de bienestar (acondicionamiento MPI-DUAE)

| Mecánica clásica | Riesgo | Ajuste MPI-DUAE |
|---|---|---|
| Gana la carta más alta (suerte del reparto) | El azar decide, no el saber | Se gana **justificando** la pertinencia; el reparto solo da las opciones |
| Eliminación / "quedarse sin cartas y perder" | Exclusión | Sin eliminación; todos juegan todas las rondas |
| Competición individual fuerte | Daña pertenencia | Juego en **parejas** (tipo Bridge) o cooperativo |
| Reglas complejas (triunfos, fallar) | Sobrecarga | Empieza simple: un solo palo de triunfo, sin obligación de asistir |
| Ganar = acumular más bazas | Excluye al que va detrás | Puntuar también la **calidad de la justificación**, no solo el nº de bazas |

Además: la **predicción de bazas** entrena autorregulación (calibrar confianza); el formato **parejas** fortalece la pertenencia; protege el **Flow** con consignas de dificultad creciente.

## Mapeo a competencias creativas

Argumentar por qué una carta gana en una categoría inesperada ejercita **flexibilidad** y **originalidad**; desarrollar la justificación, **elaboración**.

## Archivos de referencia

- `referencias/catalogo-bazas.md` — anatomía de la baraja (palos/valores/triunfo), formas de ganar la baza, predicción y usos educativos, con acondicionamiento. **Pasos 2–4.**
- `referencias/plantilla-salida.md` — plantilla del juego. **Paso 7.**
- `ejemplos/ejemplo-bazas.md` — ejemplo completo.

## Principios irrenunciables

1. **Se gana la baza razonando la pertinencia, no por la suerte del reparto.**
2. **Palos = categorías; triunfo = criterio prioritario; valores = criterio de orden.**
3. **Juego en parejas/cooperativo; sin eliminación.**
4. **Puntúa la calidad de la justificación, no solo el nº de bazas.**
5. **Empieza con reglas simples y sube complejidad solo si aporta.**
6. **Cada baza lleva R-E-A; cierra con reflexión (Kolb).**
