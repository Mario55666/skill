---
name: mpi-duae-resources-agent
description: "Generador de recursos comunicacionales y de apoyo en formato Markdown para unidades didacticas del Modelo Pedagogico Integrado DUA-Experiencial (MPI-DUAE). Produce cheatsheets/guias rapidas, correos y comunicaciones a estudiantes, y certificados/diplomas, todos accesibles e inclusivos. Usar cuando el usuario solicite 'crear recursos', 'hacer una cheatsheet o guia rapida', 'redactar correos para estudiantes', 'generar certificados o diplomas', 'materiales de apoyo' o 'recursos comunicacionales' para una unidad MPI-DUAE en formato .md. Es el segundo pilar del ecosistema: trabaja con las lecciones de mpi-duae-lesson-writer y entrega insumos a mpi-duae-finalizer. NO usar para crear lecciones (eso es mpi-duae-lesson-writer) ni para el empaquetado/cierre final (eso es mpi-duae-finalizer)."
---

# MPI-DUAE Resources Agent

Genera los **recursos comunicacionales y de apoyo** de una unidad didáctica MPI-DUAE: cheatsheets (guías rápidas), correos/comunicaciones a estudiantes y certificados/diplomas. Todos accesibles, inclusivos y coherentes con el modelo. Es el **segundo pilar** del ecosistema, entre la creación de lecciones y el empaquetado final.

## Relación con el ecosistema MPI-DUAE

```
mpi-duae-lesson-writer   →  Genera lecciones (sesiones de aula)
mpi-duae-resources-agent →  Genera recursos (cheatsheets, correos, certificados)  ← ESTE SKILL
mpi-duae-finalizer       →  Genera cierre (README, manifiesto, empaquetado)
                                    ↓
                            Kit completo entregado
```

Los recursos que produce este skill se guardan en la carpeta `02-recursos/` con la nomenclatura que espera el finalizer: `cheatsheet-*.md`, `email-*.md`, `certificado-*.md`.

## Entradas requeridas

Antes de generar, verificar con el usuario (o inferir del contexto):

1. **Unidad didáctica:** nombre, carrera/programa, ciclo, docente responsable.
2. **Recurso(s) solicitado(s):** cheatsheet, correos, certificados, o todos.
3. **Para cheatsheet:** tema/competencia técnica a resumir.
4. **Para correos:** momento del ciclo (bienvenida, recordatorio, ánimo a mitad de ciclo, cierre, derivación/apoyo).
5. **Para certificados:** nombre de la experiencia y logro reconocido.

## Flujo de trabajo

### Paso 1: Cargar plantillas
Leer la plantilla correspondiente en `referencias/`:
- `referencias/cheatsheet-template.md`
- `referencias/email-templates.md`
- `referencias/certificado-template.md`

### Paso 2: Generar el recurso
Completar la plantilla con los datos reales de la unidad, siguiendo las reglas de accesibilidad y tono de cada tipo.

### Paso 3: Verificación de calidad
Validar contra el checklist del tipo de recurso (ver cada sección abajo).

### Paso 4: Entrega
Entregar archivo(s) `.md` con la nomenclatura del finalizer (minúsculas, sin acentos, guiones medios), listos para la carpeta `02-recursos/`.

## Tipos de recurso

### 1. Cheatsheet / guía rápida
Resumen visual y operativo de un tema o procedimiento, de una sola cara, escaneable.
- **Función:** apoyo de memoria y consulta rápida; reduce carga cognitiva.
- **Reglas:** una idea por bloque; lenguaje accesible; pasos numerados; ejemplo contextualizado al Perú; nada depende solo del color.
- **Checklist:** [ ] cabe en 1 cara · [ ] título claro · [ ] pasos/bloques escaneables · [ ] ≥1 ejemplo peruano · [ ] versión texto plano de cualquier diagrama.

### 2. Correos / comunicaciones a estudiantes
Mensajes breves, humanos y orientadores para los distintos momentos del ciclo.
- **Tono:** académico humano (formal pero acogedor); sin alarmismo ni paternalismo.
- **Momentos típicos:** bienvenida, recordatorio de entrega (sin amenaza), ánimo a mitad de ciclo, felicitación de cierre, mensaje de apoyo/derivación a bienestar.
- **Reglas:** asunto claro · una acción principal por correo · plazos con margen razonable · siempre menciona los apoyos disponibles.
- **Checklist:** [ ] asunto explícito · [ ] 1 acción clara · [ ] tono humano · [ ] menciona apoyos · [ ] sin presión ansiógena.

### 3. Certificados / diplomas
Reconocimiento del logro y del **proceso**, no solo del resultado.
- **Función:** valorar el esfuerzo, fortalecer pertenencia y autoestima académica.
- **Reglas:** reconoce el proceso creativo (no solo "aprobó"); lenguaje inclusivo; datos completos (nombre, unidad, fecha, firma); evita jerarquías humillantes (mejor "completó la experiencia" que rankings).
- **Checklist:** [ ] reconoce proceso · [ ] datos completos · [ ] lenguaje inclusivo · [ ] sin comparación humillante.

## Reglas fundamentales

1. **Accesibilidad primero:** todo recurso es legible, escaneable y no depende del color ni de una sola vía de acceso.
2. **Contexto peruano:** los ejemplos de las cheatsheets se anclan a la realidad del estudiante (transporte, mercado, barrio, emprendimiento).
3. **Tono humano, no burocrático ni promocional:** especialmente en correos.
4. **El proceso se reconoce:** los certificados valoran el recorrido creativo, no solo la nota.
5. **Bienestar visible:** los correos siempre dejan claro que existen apoyos y cómo pedirlos sin dar explicaciones.
6. **Nomenclatura del finalizer:** archivos en minúsculas, sin acentos, con guiones, listos para `02-recursos/`.

## Archivos de referencia

- `referencias/cheatsheet-template.md` — plantilla de guía rápida accesible.
- `referencias/email-templates.md` — plantillas de correos por momento del ciclo.
- `referencias/certificado-template.md` — plantilla de certificado/diploma.
- `ejemplos/ejemplo-recursos.md` — ejemplo completo de los tres recursos para una unidad.
