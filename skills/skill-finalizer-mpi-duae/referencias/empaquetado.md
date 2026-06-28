# Empaquetado de Unidad Didactica MPI-DUAE

## Proposito del Empaquetado

El empaquetado es el proceso de organizar, validar y entregar el kit completo de una unidad didactica MPI-DUAE en una estructura de carpetas estandarizada, lista para distribucion al docente, subida a plataforma institucional, o entrega a evaluacion de calidad.

---

## Estructura de Carpetas Obligatoria

Cada unidad MPI-DUAE debe entregarse con esta estructura exacta:

```
[nombre-unidad]-mpi-duae/
|
|-- README.md                           # (OBLIGATORIO) Documento de entrada
|-- MANIFESTO.md                        # (OBLIGATORIO) Declaracion de principios
|
|-- 01-lecciones/                       # (OBLIGATORIO) Carpeta de lecciones
|   |-- sesion-01-[titulo-corto].md     # Leccion 1 (EC)
|   |-- sesion-02-[titulo-corto].md     # Leccion 2 (OR)
|   |-- sesion-03-[titulo-corto].md     # Leccion 3 (CA)
|   |-- sesion-04-[titulo-corto].md     # Leccion 4 (EA)
|   |-- sesion-05-[titulo-corto].md     # Leccion 5 (Proyeccion)
|   |-- ...                             # Sesiones adicionales segun unidad
|
|-- 02-recursos/                        # (OBLIGATORIO) Recursos de comunicacion
|   |-- cheatsheet-[unidad].md          # Hoja de referencia rapida
|   |-- email-bienvenida.md             # Email semana 1
|   |-- email-motivacion-s04.md         # Email semana 4
|   |-- email-motivacion-s08.md         # Email semana 8
|   |-- email-motivacion-s12.md         # Email semana 12
|   |-- email-retroalimentacion.md      # Email post-evaluacion
|   |-- certificado-participacion.md    # Plantilla certificado
|   |-- reconocimiento-[categoria].md   # Plantillas reconocimiento (N archivos)
|
|-- 03-anexos-pedagogicos/              # (OBLIGATORIO) Adaptaciones y evaluacion
|   |-- adaptaciones-tea.md             # Adaptaciones TEA
|   |-- adaptaciones-tdha.md            # Adaptaciones TDHA
|   |-- adaptaciones-visual.md          # Adaptaciones discapacidad visual
|   |-- adaptaciones-auditiva.md        # Adaptaciones discapacidad auditiva
|   |-- adaptaciones-ansiedad.md        # Adaptaciones alta ansiedad
|   |-- rubrica-evaluacion.md           # Rubrica formativa completa
|   |-- protocolo-derivacion.md         # Protocolo de derivacion a salud mental
|
|-- 04-referencias/                     # (OBLIGATORIO) Bibliografia y evidencia
|   |-- bibliografia-completa.md        # Referencias APA de toda la unidad
|   |-- instrumentos-medicion.md        # Descripcion de instrumentos psicometricos usados
|   |-- evidencia-empirica.md           # Antecedentes que respaldan el diseno
|
|-- 05-docente/                         # (OPCIONAL) Material de apoyo al docente
|   |-- guia-implementacion.md          # Pasos para implementar la unidad
|   |-- calendario-sugerido.md          # Distribucion semana a semana
|   |-- notas-clase.md                  # Apuntes o guiones para el docente
|   |-- preguntas-frecuentes.md         # FAQ de implementacion
|
|-- version.md                          # (OBLIGATORIO) Historial de versiones
|-- checklist-calidad.md                # (OBLIGATORIO) Lista de verificacion firmada
```

## Convenciones de Nomenclatura

### Carpetas
- Prefijo numerado (`01-`, `02-`) para orden de prioridad/lectura
- Nombre en minusculas, sin acentos, guiones como separadores
- Sufijo `-mpi-duae` en la carpeta raiz para identificacion del modelo

### Archivos
- Todo en minusculas, sin acentos, sin espacios
- Guiones medios (`-`) como separadores
- Prefijo de tipo (`sesion-`, `email-`, `certificado-`, `adaptaciones-`)
- Sufijo numerico para orden (`-s01`, `-s04`, `-s08`)

### Ejemplos correctos
```
sesion-01-teoria-del-color.md
email-motivacion-s04.md
certificado-participacion.md
adaptaciones-tea.md
cheatsheet-teoria-color-2026-1.md
```

### Ejemplos incorrectos
```
Sesion 1 Teoria del Color.md      # Mayusculas, espacios
email_motivacion.md               # Guion bajo en vez de guion medio
adaptacionesTEA.md                # Sin separador
```

---

## Checklist de Empaquetado

### Paso 1: Verificacion de completitud

- [ ] README.md existe y esta completo (sin campos `[...]` sin rellenar)
- [ ] MANIFESTO.md existe y esta completo
- [ ] Carpeta `01-lecciones/` tiene al menos 4 archivos `.md`
- [ ] Carpeta `02-recursos/` tiene al menos cheatsheet + 1 email + 1 certificado
- [ ] Carpeta `03-anexos-pedagogicos/` tiene las 5 adaptaciones + rubrica
- [ ] Carpeta `04-referencias/` tiene bibliografia + instrumentos
- [ ] `version.md` existe con historial de cambios
- [ ] `checklist-calidad.md` existe y esta completado

### Paso 2: Verificacion de calidad MPI-DUAE

- [ ] Cada leccion tiene las 5 fases Kolbianas (EC, OR, CA, EA, Proyeccion)
- [ ] Cada leccion activa al menos 2 dimensiones creativas de Torrance
- [ ] Cada leccion resuelve al menos 1 barrera DUA explicitamente
- [ ] Al menos 2 ejemplos por leccion son del contexto peruano
- [ ] Cada leccion produce un artefacto tangible
- [ ] Hay al menos una actividad no verbal, una no escrita, y una no grupal por leccion
- [ ] Los cheatsheets tienen las 6 secciones obligatorias
- [ ] Los emails tienen footer con Linea 113 + servicio interno
- [ ] Los certificados tienen version texto plano
- [ ] El README tiene seccion de adaptaciones inclusivas completa
- [ ] El manifiesto tiene matriz de trazabilidad completa

### Paso 3: Verificacion tecnica

- [ ] Todos los archivos usan codificacion UTF-8
- [ ] Todos los archivos tienen extension `.md`
- [ ] No hay archivos con nombres duplicados
- [ ] No hay archivos temporales (`.tmp`, `.bak`, `~`)
- [ ] No hay datos personales de estudiantes reales
- [ ] Las tablas Markdown estan bien formadas (sintaxis correcta)
- [ ] Los enlaces internos (si existen) son relativos, no absolutos
- [ ] Las imagenes referenciadas (si existen) estan en carpeta `assets/` adjunta

### Paso 4: Verificacion de accesibilidad

- [ ] Todos los documentos usan jerarquia de headers correcta (h1 > h2 > h3)
- [ ] Las tablas tienen headers descriptivos
- [ ] No hay paredes de texto (parrafos de maximo 5-6 lineas)
- [ ] Se usa negrita para enfasis estructural, no decorativo
- [ ] Las listas se usan para contenido enumerado
- [ ] Se incluyen descripciones alternativas para cualquier elemento visual

### Paso 5: Documentacion final

- [ ] `version.md` incluye:
  - Numero de version (SemVer: X.Y.Z)
  - Fecha de creacion
  - Fecha de ultima modificacion
  - Autor original
  - Colaboradores (si aplica)
  - Cambios de esta version
- [ ] `checklist-calidad.md` esta firmado/digitalmente confirmado por el responsable

---

## Formato del Archivo version.md

```markdown
# Historial de Versiones

## [X.Y.Z] — [YYYY-MM-DD]

- Autor: [Nombre completo]
- Rol: [Docente / Coordinador / Investigador]
- Institucion: IESP DYC

### Cambios en esta version
- [Cambio 1: descripcion breve]
- [Cambio 2: descripcion breve]

### Estado
- [ ] Borrador
- [ ] En revision
- [x] Aprobado para implementacion
- [ ] Archivado

### Proximos pasos
- [Tarea pendiente o mejora identificada]

---

## [X.Y.Z-1] — [YYYY-MM-DD]

[Cronologia de versiones anteriores...]
```

## Formato del Archivo checklist-calidad.md

```markdown
# Checklist de Calidad MPI-DUAE

**Unidad**: [Nombre completo]
**Version**: [X.Y.Z]
**Fecha de verificacion**: [YYYY-MM-DD]
**Verificado por**: [Nombre y rol]

## Completitud
- [ ] README.md completo
- [ ] MANIFESTO.md completo
- [ ] Lecciones (minimo 4 sesiones)
- [ ] Recursos (cheatsheet + emails + certificados)
- [ ] Anexos pedagogicos (5 adaptaciones + rubrica)
- [ ] Referencias bibliograficas

## Calidad MPI-DUAE
- [ ] Fases Kolbianas en cada sesion
- [ ] Dimensiones creativas activadas
- [ ] Barreras DUA resueltas
- [ ] Contexto peruano presente
- [ ] Artefactos tangibles por sesion
- [ ] Adaptaciones multiples por sesion

## Tecnico
- [ ] UTF-8, .md, nombres correctos
- [ ] Sin datos personales
- [ ] Tablas bien formadas
- [ ] Jerarquia de headers correcta

## Accesibilidad
- [ ] Headers descriptivos
- [ ] Parrafos cortos
- [ ] Negrita estructural
- [ ] Versiones texto plano donde aplica

---

**RESULTADO**: [APROBADO / APROBADO CON OBSERVACIONES / NO APROBADO]

**Observaciones**:
[Espacio para comentarios si hay observaciones]

**Firma**: ___________________
```

---

## Entregables del Proceso de Empaquetado

Al completar el empaquetado, el agente entrega:

1. **Estructura de carpetas validada**: La jerarquia exacta creada en el filesystem
2. **README.md**: Documento de entrada completo y personalizado
3. **MANIFESTO.md**: Declaracion de principios completa y referenciada
4. **version.md**: Historial de versiones inicial
5. **checklist-calidad.md**: Lista de verificacion completada y firmada
6. **Reporte de empaquetado**: Resumen de lo que se genero, con estadisticas

### Formato del Reporte de Empaquetado

```markdown
# Reporte de Empaquetado MPI-DUAE

**Unidad**: [Nombre]
**Fecha**: [YYYY-MM-DD]
**Version**: [X.Y.Z]

## Resumen

| Categoria | Archivos | Estado |
|-----------|----------|--------|
| Documentos base | 4 (README, MANIFESTO, version, checklist) | [OK/Pendiente] |
| Lecciones | [N] sesiones | [OK/Pendiente] |
| Recursos | [N] archivos | [OK/Pendiente] |
| Anexos pedagogicos | [N] archivos | [OK/Pendiente] |
| Referencias | [N] archivos | [OK/Pendiente] |
| **Total** | **[N] archivos** | **[OK/Pendiente]** |

## Verificacion MPI-DUAE

- [x] Fases Kolbianas completas
- [x] Dimensiones creativas activadas
- [x] Barreras DUA resueltas
- [x] Contexto peruano presente
- [x] Adaptaciones inclusivas documentadas

## Observaciones

[Si hay elementos pendientes, limitaciones conocidas, o recomendaciones de mejora]

---

*Reporte generado automaticamente por el MPI-DUAE Finalizer*
```
