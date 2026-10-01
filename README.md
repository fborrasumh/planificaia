# PlanificaIA

Aplicación web de un solo fichero para el estudiantado de **Planificación del Entrenamiento Deportivo** (Grado en Ciencias de la Actividad Física y del Deporte, Universidad Miguel Hernández de Elche).

**Usar la app:** https://fborrasumh.github.io/planificaia/

## Qué hace

- El estudiante se encarga de la temporada de un deportista o equipo **sintético** y completa seis entregas guiadas: dossier inicial, plan de temporada, sistema de seguimiento, bitácora de decisiones, evaluación y análisis, y cierre.
- Incluye las herramientas de **Entrenamiento 360** (anamnesis, planificación, monitorización de la carga, evaluación y análisis) y añade cálculos de carga: monotonía, strain, ACWR, mapa de ocho semanas, calidad del dato y cambio mínimo detectable (MDC95).
- Un **tutor de IA** pregunta, revisa por criterios de la rúbrica y señala lagunas, pero **no redacta las entregas**. Las citas que usa se comprueban contra el texto del estudiante.
- Registro de las consultas a la IA y detección de fragmentos de 10 o más palabras copiados de sus respuestas.
- Cuatro **hitos** exportables en JSON (`planificaia/1`) con huella SHA-256 encadenada al hito anterior, diferencias entre hitos y restauración desde un hito.

## Privacidad

Todo se guarda en el navegador. Solo el texto que consultas al tutor viaja a OpenAI, con tu propia clave. Trabaja siempre con datos sintéticos: nunca introduzcas datos reales de deportistas.

## Límites

- La huella de integridad detecta ediciones burdas del fichero; no impide un fraude deliberado.
- Las fechas de recepción de incidencias las escribe el estudiante.
- Las partes nuevas de la interfaz están solo en español.

## Autoría y atribución

Realizada entre **Fernando Borrás Rocher** y **Manuel Moya Ramón** (Universidad Miguel Hernández de Elche). Se apoya en el código de **Entrenamiento 360**, obra de Manuel Moya Ramón, publicada aquí bajo licencia MIT.

Herramienta complementaria para el profesorado: [PlanificaIA Docente](https://github.com/fborrasumh/planificaia-docente).

## Cómo citar

Borrás Rocher, F. y Moya Ramón, M. (2026). *PlanificaIA* (v1.0.0) [Software]. Universidad Miguel Hernández de Elche. (DOI en trámite)

## Licencia

MIT. Véase [LICENSE](LICENSE).
