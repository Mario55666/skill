---
name: skill-lesson-writer-mpi-duae
description: Generador de lecciones pedagogicas en formato Markdown para el Modelo Pedagogico Integrado DUA-Experiencial (MPI-DUAE). Usar cuando el usuario solicite "redactar lecciones", "escribir sesiones de clase", "crear contenido de unidad didactica", "desarrollar lecciones con ejemplos reales", o cualquier tarea que implique generar material educativo para el MPI-DUAE en formato *.md. El skill integra Diseno Universal para el Aprendizaje 3.0 (CAST), aprendizaje experiencial de Kolb, las cuatro dimensiones creativas de Torrance (fluidez, flexibilidad, originalidad, elaboracion), y excelencia inclusiva. Contextualizado para estudiantes de primer semestre de carreras de Diseno del IESP DYC (Lima, Peru), con ejemplos reales del contexto peruano y adaptaciones para vulnerabilidad psicosocial y neurodiversidad. NO usar para otros modelos pedagogicos ni para contextos fuera del MPI-DUAE.
---

# MPI-DUAE Lesson Writer

Genera lecciones pedagogicas completas en Markdown que integren el Diseno Universal para el Aprendizaje, el aprendizaje experiencial de Kolb, y el desarrollo de competencias creativas.

## Entradas requeridas

Antes de generar, verificar con el usuario (o inferir del contexto):

1. **Unidad didactica**: nombre completo de la unidad (ej: "Fundamentos del Diseno Grafico")
2. **Numero de sesiones**: cuantas lecciones generar (default: 1 sesion = 90 minutos)
3. **Contenidos especificos**: temas o competencias tecnicas que la sesion debe cubrir
4. **Nivel de la sesion**: basico (semanas 1-4), intermedio (5-10), o avanzado (11-16)

## Flujo de trabajo

### Paso 1: Cargar marco teorico

Leer `referencias/marco-teorico.md` para activar los principios DUA 3.0, el ciclo de Kolb, las dimensiones creativas y el contexto del IESP DYC.

### Paso 2: Cargar estructura de leccion

Leer `referencias/estructura-leccion.md` para obtener el template exacto de formato Markdown, los tiempos por fase, y las reglas de calidad de redaccion.

### Paso 3: Cargar ejemplos contextuales

Leer `referencias/ejemplos-contexto.md` para seleccionar 2-3 ejemplos reales del contexto peruano relevantes a la tematica de la unidad. Priorizar ejemplos que conecten con la realidad del estudiante (transporte, mercados, emprendimiento, barrio).

### Paso 4: Generar la leccion

Escribir el archivo Markdown siguiendo EXACTAMENTE la estructura de `estructura-leccion.md`:

1. YAML frontmatter con metadatos de la sesion
2. Fase 1: Apertura - Anclaje Emocional (EC)
3. Fase 2: Exploracion - Pensamiento Divergente (OR)
4. Fase 3: Sistematizacion - Pensamiento Convergente (CA)
5. Fase 4: Aplicacion - Pensamiento Critico (EA)
6. Fase 5: Cierre - Proyeccion y Metacognicion
7. Anexos: Ficha para el docente + versiones adaptadas + referencias

### Paso 5: Verificacion de calidad

Antes de entregar, validar que la leccion cumple TODOS los criterios:

- [ ] Cada fase integra una barrera DUA explicita y resuelta
- [ ] Las 4 dimensiones creativas (fluidez, flexibilidad, originalidad, elaboracion) estan activadas
- [ ] Hay al menos 2 ejemplos contextualizados al Peru o al sector diseno peruano
- [ ] Hay una actividad que funcione sin hablar en publico
- [ ] Hay una actividad que funcione sin escribir rapido
- [ ] Hay una actividad que funcione sin trabajo en grupo
- [ ] Los materiales son minimos (papel, lapiz, celular)
- [ ] El lenguaje es accesible para estudiante de primer semestre
- [ ] Los tiempos suman 90 minutos (o la duracion especificada)
- [ ] Los anexos incluyen adaptaciones para TEA, TDHA, discapacidad visual/auditiva, y ansiedad

## Reglas fundamentales

1. **Contexto obligatorio**: Todo ejemplo, caso o problema debe ser contextualizado al Peru. Prohibidos ejemplos genericos de "empresas internacionales" o contextos extranjeros no adaptados.

2. **DUA operativo, no teorico**: No mencionar "DUA" como etiqueta en el texto de la leccion. Las barreras DUA se resuelven mediante diseno pedagogico implicito (la estudiante con ansiedad nunca lee "si tienes ansiedad...", simplemente hay una opcion escrita disponible).

3. **Producto sobre performance**: Cada sesion debe producir un artefacto tangible (boceto, mapa, propuesta, analisis) que el estudiante pueda conservar y valorar. Evitar actividades que solo produzcan "discusion".

4. **Emocion como puerta de entrada**: Cada leccion comienza con una experiencia afectiva o sensorial (no con definicion de concepto). La conexion emocional precede a la cognitiva.

5. **El estudiante es agente**: Formular las actividades en voz activa, con elecciones reales ("elige uno de estos tres retos", "decide que formato usar"). Nunca caminos unicos.

## Variantes de salida

**Formato estandar**: Archivo `.md` autonomo por sesion.
**Formato compacto**: Si el usuario solicita multiples sesiones (4+), generar un solo archivo con separadores `---` entre sesiones y una tabla de contenido inicial.
**Formato docente**: Si el usuario lo solicita explicitamente, generar version minimalista sin anexos pedagogicos (solo la leccion ejecutable).
