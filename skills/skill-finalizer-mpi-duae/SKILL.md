---
name: mpi-duae-finalizer
description: "Finalizador y empaquetador de unidades didacticas del Modelo Pedagogico Integrado DUA-Experiencial (MPI-DUAE). Genera el README profesional, el manifiesto pedagogico, la estructura de carpetas estandarizada, y el reporte de calidad que completan el kit de una unidad didactica. Usar cuando el usuario solicite empaquetar la unidad, generar el README, crear el manifiesto, finalizar el kit, hacer el cierre de la unidad, o cualquier tarea relacionada con la documentacion, validacion y entrega final de una unidad MPI-DUAE en formato md. Este skill CIERRA el ciclo trabajando con las lecciones generadas por mpi-duae-lesson-writer y los recursos de mpi-duae-resources-agent para producir la entrega profesional completa. NO usar para crear lecciones (eso es mpi-duae-lesson-writer), ni para generar recursos comunicacionales (eso es mpi-duae-resources-agent), ni para contextos fuera del MPI-DUAE."
---

# MPI-DUAE Finalizer

Genera los documentos de cierre de una unidad didactica MPI-DUAE: README, manifiesto pedagogico, estructura de carpetas, y reporte de calidad. Es el tercer pilar del ecosistema, responsable de la entrega profesional del kit completo.

## Relacion con el ecosistema MPI-DUAE

```
mpi-duae-lesson-writer  →  Genera lecciones (sesiones de aula)
mpi-duae-resources-agent →  Genera recursos (cheatsheets, emails, certificados)
mpi-duae-finalizer       →  Genera cierre (README, manifiesto, empaquetado)
                                    ↓
                            Kit completo entregado
```

## Entradas requeridas

Antes de finalizar, verificar con el usuario:

1. **Estado de las lecciones**: ¿Estan todas las sesiones generadas? ¿Cuantas sesiones tiene la unidad?
2. **Estado de los recursos**: ¿Se generaron cheatsheets, emails y certificados? ¿Cuales?
3. **Unidad didactica**: Nombre exacto, carrera, ciclo academico, docente responsable
4. **Modo de finalizacion**: Completo (README + manifiesto + empaquetado) o parcial (solo uno)

## Flujo de trabajo

### Paso 1: Inventario de archivos existentes

Verificar que archivos ya fueron generados por otros skills:

| Carpeta | Archivos esperados | Estado |
|---------|-------------------|--------|
| `01-lecciones/` | `sesion-01-*.md` a `sesion-N-*.md` | Verificar existencia |
| `02-recursos/` | `cheatsheet-*.md`, `email-*.md`, `certificado-*.md` | Verificar existencia |
| `03-anexos-pedagogicos/` | `adaptaciones-*.md`, `rubrica-*.md` | Generar si faltan |
| `04-referencias/` | `bibliografia-*.md` | Generar si falta |

Los archivos que NO existan deben ser documentados como "pendientes" en el reporte.

### Paso 2: Generar README.md

Leer `referencias/readme-template.md`. Seguir el template al pie de la letra:

- Completar TODOS los campos entre corchetes `[...]` con datos reales de la unidad
- Incluir la estructura de carpetas real (adaptar el arbol al numero real de archivos)
- Personalizar la seccion de competencias MPI-DUAE segun la tematica de la unidad
- Redactar la presentacion (2-3 parrafos) conectando la unidad con el contexto peruano
- Incluir la tabla de sesiones con datos reales de cada leccion

Reglas de calidad:
- 150-250 lineas renderizadas
- MPI-DUAE mencionado al menos 3 veces
- Nota de contacto para adaptaciones al final
- Sin campos `[...]` sin completar

### Paso 3: Generar MANIFESTO.md

Leer `referencias/manifiesto.md`. Seguir el template al pie de la letra:

- Seccion 1 (Declaracion de Principios): Personalizar con la realidad especifica del IESP DYC
- Seccion 2 (Justificacion): Completar tabla de decisiones de diseno con referencias APA
- Seccion 3 (Compromisos Eticos): Adaptar si la unidad tiene particularidades eticas
- Seccion 4 (Matriz de Trazabilidad): OBLIGATORIO completar con datos reales de cada sesion
- Seccion 5 (Contexto): Actualizar datos sociales al contexto mas reciente disponible
- Seccion 6 (Referencias): Incluir TODAS las referencias citadas en el README y las lecciones

Reglas de calidad:
- 200-350 lineas renderizadas
- Primera persona del plural ("creemos", "hemos decidido")
- Cada afirmacion fuerte con referencia APA
- Matriz de trazabilidad completa (no vacia)
- Cita filosofica al cierre

### Paso 4: Generar estructura de empaquetado

Leer `referencias/empaquetado.md`. Ejecutar:

1. **Crear carpetas**: Generar la estructura de directorios con prefijos numericos (`01-`, `02-`, etc.)
2. **Organizar archivos**: Mover/verificar que cada archivo existente este en su carpeta correspondiente
3. **Generar version.md**: Crear archivo de historial de versiones con datos iniciales
4. **Generar checklist-calidad.md**: Crear lista de verificacion con todos los items marcados segun el estado real
5. **Generar reporte de empaquetado**: Resumen ejecutivo de lo entregado

Reglas de calidad:
- Nombres de archivos en minusculas, sin acentos, guiones medios
- Sin archivos temporales ni datos personales
- Todos los archivos UTF-8, extension `.md`
- Carpetas raiz con sufijo `-mpi-duae`

### Paso 5: Verificacion de calidad final

Validar que el kit completo cumple TODOS los criterios:

#### Completitud del kit
- [ ] README.md completo y personalizado
- [ ] MANIFESTO.md completo con matriz de trazabilidad
- [ ] Carpeta `01-lecciones/` con sesiones numeradas secuencialmente
- [ ] Carpeta `02-recursos/` con cheatsheet + emails + certificados
- [ ] Carpeta `03-anexos-pedagogicos/` con 5 adaptaciones + rubrica
- [ ] Carpeta `04-referencias/` con bibliografia APA
- [ ] `version.md` con datos de version inicial
- [ ] `checklist-calidad.md` completado

#### Calidad MPI-DUAE
- [ ] Las 4 dimensiones creativas (fluidez, flexibilidad, originalidad, elaboracion) aparecen en README y manifiesto
- [ ] Los 3 principios DUA (representacion, accion/expresion, compromiso) estan documentados
- [ ] El ciclo de Kolb (EC, OR, CA, EA) aparece en el mapa de sesiones
- [ ] El bienestar psicosocial es componente visible, no anexo
- [ ] El contexto peruano es explicito en al menos 2 secciones

#### Calidad tecnica
- [ ] Nombres de archivo correctos (minusculas, guiones, sin acentos)
- [ ] Sin campos `[...]` sin completar en ningun documento
- [ ] Jerarquia de headers Markdown correcta en todos los archivos
- [ ] Tablas Markdown bien formadas (headers, separadores, alineacion)
- [ ] Referencias APA 7ma edicion consistentes

#### Accesibilidad
- [ ] Headers descriptivos en todos los documentos
- [ ] Parrafos de maximo 5-6 lineas
- [ ] Uso de negrita para enfasis estructural
- [ ] Versiones texto plano donde el template lo requiere

### Paso 6: Entrega

El skill entrega:
1. **README.md** — Documento de entrada a la unidad
2. **MANIFESTO.md** — Declaracion de principios pedagogicos
3. **Estructura de carpetas** — Organizacion fisica de archivos
4. **version.md** — Control de versiones
5. **checklist-calidad.md** — Verificacion firmada
6. **Reporte de empaquetado** — Resumen ejecutivo con estadisticas

## Reglas fundamentales

1. **Este skill no genera contenido pedagogico nuevo**: No crea lecciones, ni recursos, ni actividades. Documenta, organiza y valida lo que otros skills generaron. Si falta una leccion o un recurso, documentarlo como "pendiente" en el reporte, no inventarlo.

2. **El README es la puerta de entrada**: Debe permitir a un docente nuevo comprender la unidad en 3 minutos. Si el README no logra eso, no esta listo.

3. **El manifiesto es el contrato etico**: Declara los principios que rigen la unidad. No es negociable: si el manifiesto dice "ningun estudiante excluido", la unidad debe demostrarlo en su diseno.

4. **La trazabilidad es obligatoria**: La matriz del manifiesto conecta cada sesion con principios DUA, dimensiones creativas y bienestar psicosocial. No puede quedar vacia ni generica.

5. **El empaquetado es estandarizado**: La estructura de carpetas con prefijos numericos (`01-`, `02-`) garantiza que cualquier unidad MPI-DUAE se reconozca y navegue de la misma forma, sin importar quien la genero.
