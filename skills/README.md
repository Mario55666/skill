# Ecosistema de Skills MPI-DUAE

Conjunto de skills para el **Modelo Pedagógico Integrado DUA-Experiencial (MPI-DUAE)**: cada uno convierte una **unidad didáctica en formato `.md`** en un recurso pedagógico concreto, alineado con **DUA 3.0** (CAST, 2024), el **ciclo experiencial de Kolb**, las **competencias creativas** (Torrance) y el **bienestar e inclusión** (reducción de ansiedad, sentido de pertenencia, neurodiversidad).

Contexto de referencia: primer semestre de carreras de Diseño del IESP "Diseño y Comunicación" (Lima, Perú), 2026–2027.

---

## A. Skills de mecánicas de juego (gamificación del aprendizaje)

Convierten una unidad en una experiencia lúdica de refuerzo. Patrón común MPI-DUAE: **el conocimiento decide el resultado (no el azar ni la fuerza), sin eliminación, con retroalimentación positiva R-E-A y variante cooperativa.**

| Skill | Mecánica | Produce |
|---|---|---|
| `skill-games-mpi-duae` | Gamificación general (actividades) | Kit de actividades gamificadas de refuerzo |
| `skill-gamificacion-mpi-duae` | Estrategia (marco Tec de Monterrey) | Sistema/estrategia de gamificación de un curso |
| `skill-escape-room-mpi-duae` | Escape room (método EduEscapeRoom) | Experiencia inmersiva con retos y debriefing |
| `skill-juegos-carrera-mpi-duae` | Juegos de carrera (Senet, Ur, Parchís, Oca) | Juego de tablero de recorrido |
| `skill-dados-azar-mpi-duae` | Dados / azar (dados, tabas, cauris) | Dinámica con azar (equidad) + acierto |
| `skill-mancala-mpi-duae` | Siembra "contar y capturar" (Oware, Bao) | Juego de siembra / cosechar conocimiento |
| `skill-batalla-captura-mpi-duae` | Estrategia (Chaturanga, Ajedrez, Latrunculi, Tafl) | Juego de estrategia/resolución en cuadrícula |
| `skill-bazas-mpi-duae` | Bazas / trick-taking (naipes) | Juego de cartas por razonamiento |
| `skill-estilos-visuales-mpi-duae` | Estilos visuales | Material de corrientes artísticas/tecnológicas/de diseño |
| `skill-animaciones-mpi-duae` | Animaciones interactivas | Recursos HTML/CSS/JS accesibles |

## B. Skills pedagógicos / de orquestación (ciclo de la unidad)

Diseñan, redactan, comunican y empaquetan la unidad a lo largo del ciclo de 16 semanas.

| Skill | Función | Fase / momento |
|---|---|---|
| `skill-f1-activacion-mpi-duae` | Orquesta la activación y representación | F1 · Semanas 1–3 (EC) |
| `skill-f2f3f4-curricula-mpi-duae` | Orquesta la fase de contenido | F2–F4 · Semanas 4–14 (OR→CA→EA) |
| `skill-lesson-writer-mpi-duae` | Redacta lecciones/sesiones de aula | Transversal (genera contenido) |
| `skill-resources-agent-mpi-duae` | Genera recursos (cheatsheets, correos, certificados) | Transversal (apoyo) |
| `skill-landing-pages-mpi-duae` | Comunica la unidad (landing page) | Difusión / captación |
| `skill-finalizer-mpi-duae` | Empaqueta y cierra el kit (README, manifiesto) | Cierre / entrega |

### Cadena del ciclo pedagógico
```
lesson-writer  →  resources-agent  →  finalizer
(lecciones)        (recursos)          (README + manifiesto + empaquetado)
                                              ↓
                                       Kit completo entregado
```
Las fases F1 y F2-F4 orquestan la secuencia didáctica; landing-pages comunica la unidad hacia afuera.

---

## Estructura de cada skill

```
skill-<nombre>-mpi-duae/
├── SKILL.md            ← el skill (frontmatter name/description + instrucciones)
├── referencias/        ← catálogos, plantillas y marcos de apoyo
└── ejemplos/           ← ejemplo(s) completo(s) de uso
```
Los skills de mecánicas de juego incluyen además un archivo `Skill-*-MPI-DUAE.md` con todo empaquetado en un solo documento.

## Principios compartidos (ADN MPI-DUAE)
1. Toda salida ancla un **resultado de aprendizaje** explícito de la unidad.
2. **DUA 3.0:** múltiples medios de representación, acción/expresión e implicación.
3. **Ciclo de Kolb:** experiencia → reflexión → conceptualización → experimentación.
4. **Retroalimentación positiva R-E-A** (Reconocer · Especificar · Avanzar); el error es información.
5. **Bienestar e inclusión:** sin exposición humillante, reintentos, neurodiversidad y variantes cooperativas.

---

> Nota: `emil-design-eng/` es un skill preexistente del repositorio, ajeno al ecosistema MPI-DUAE.
