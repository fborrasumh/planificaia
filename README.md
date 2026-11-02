# PlanificaIA

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.23091369.svg)](https://doi.org/10.5281/zenodo.23091369)

Aplicación web de un solo fichero para el estudiantado de **Planificación del Entrenamiento Deportivo** (Grado en Ciencias de la Actividad Física y del Deporte, Universidad Miguel Hernández de Elche).

**Usar la app:** https://fborrasumh.github.io/planificaia/

**Idiomas:** español (por defecto), inglés y portugués, con selector en la barra superior (o `?lang=en` / `?lang=pt` en la URL). La rúbrica oficial es la española; las versiones inglesa y portuguesa son traducciones para leerla.

## Qué hace

- El estudiante se encarga de la temporada de un deportista o equipo **sintético** y completa seis entregas guiadas: dossier inicial, plan de temporada, sistema de seguimiento, bitácora de decisiones, evaluación y análisis, y cierre.
- Incluye las herramientas de **Entrenamiento 360** (anamnesis, planificación, monitorización, evaluación y análisis) y añade cálculos de carga: monotonía, strain, ACWR, mapa de ocho semanas, calidad del dato y cambio mínimo detectable (MDC95).
- **Planificación por niveles:** intervalo de la temporada (semanas 1-50), modelo (tradicional, por bloques, deporte colectivo o flexible), sus estructuras (períodos o bloques), mesociclos, microciclos y sesiones, con los tipos propios de cada modelo, un calendario de barras y comprobaciones de que todo cabe y no se solapa. Cada sesión planificada se registra después en Monitorización, que hereda período, mesociclo, microciclo, tipo de sesión y contenido.
- **Exigencia teórica:** cada sesión planificada lleva una exigencia de 1 a 5 limitada por su tipo (desarrollo 3-5, mantenimiento 3, complementaria 2-3, competición 5, evaluación y control 1-5, recuperación 1-2); la app suma la de cada semana, microciclo, mesociclo y período o bloque y la muestra en gráficos de columnas.
- **Desarrollo de las sesiones en Planificación:** desde cada sesión planificada se completa allí mismo su contenido (fuerza, métodos aeróbicos o pruebas); Monitorización queda para el bienestar y el seguimiento de la carga.
- **Sesiones:** contenido de la sesión (resistencia, fuerza, velocidad, flexibilidad, técnico-táctico, test, mixto) separado del objetivo (máx. 30 palabras); ejercicios aeróbicos continuos, MIIT, HIIT, SIT o RST con su pauta; fuerza con kg obligatorios en peso libre o máquina guiada y objetivo de intensidad según el método (%1RM, velocidad de barra 0,1-5 m/s, RIR 1-6 o carácter del esfuerzo 0-20 / 0-20); en las sesiones de test se eligen las pruebas de Evaluación y se pueden anotar sus resultados.
- **Evaluación:** biblioteca de 10 pruebas con protocolo, población, seguridad y evidencia con referencia (CMJ, SJ, sprint 20 m, 505, RSA 6 × 40 m, Yo-Yo IR1, 30-15 IFT, contrarreloj 20 km, 1RM estimada, sit and reach) y pruebas propias.
- **Análisis:** variables de carga externa del trabajo de fuerza (kg, series, repeticiones, velocidad de barra) y todas las pruebas; el estudio sintético de correlación e inferencia incluye deportes individuales, colectivos y de raqueta.
- Un **tutor de IA** pregunta, revisa por criterios de la rúbrica y señala lagunas, pero **no redacta las entregas**. Las citas que usa se comprueban contra el texto del estudiante y las que no aparecen se descartan. Hay un ejemplo de revisión que funciona sin clave.
- Registro de las consultas a la IA y detección de fragmentos de 10 o más palabras copiados de sus respuestas.
- Cuatro **hitos** exportables en JSON (`planificaia/1`) con huella SHA-256 encadenada al hito anterior, diferencias entre hitos y restauración desde un hito. Desde la v1.1 el fichero incluye también la planificación y las pruebas propias.
- El plan de temporada se descarga en Word, y cada apartado (anamnesis, planificación, monitorización, evaluación y análisis) o un informe completo se imprimen o guardan en PDF desde el navegador.

## Cómo se usa la IA

Con la propia clave de OpenAI, Google Gemini o Anthropic Claude; se elige el modelo de un desplegable con los modelos de esa clave. La clave se guarda solo en el navegador. No hace falta servidor.

## Privacidad

Todo se guarda en el navegador. Solo el texto que se consulta al tutor viaja al proveedor de IA elegido, con el nombre del estudiante, correos y teléfonos enmascarados, y antes del primer envío de cada sesión se muestra lo que sale. Trabaja siempre con datos sintéticos: nunca introduzcas datos reales de deportistas.

## Límites

- La huella de integridad detecta ediciones burdas del fichero; no impide un fraude deliberado.
- Las fechas de recepción de incidencias las escribe el estudiante.
- El enmascarado no reconoce todos los datos personales posibles (por ejemplo, nombres de terceros escritos en el texto).
- Las traducciones al inglés y al portugués (europeo) deben revisarlas hablantes de esas lenguas antes de usarlas en docencia.
- Las comprobaciones de las entregas indican si un contenido está, no su calidad; la valoración es del profesorado.
- Probada con IA simulada para los tres proveedores; no con claves reales.

## Novedades de la versión 1.2.0

Propuestas de Manuel Moya Ramón: pruebas radiológicas entre las valoraciones médicas, exigencia teórica (1-5) por sesión con sus sumas por semana, microciclo, mesociclo y período y gráficos de columnas, desarrollo completo de la sesión desde Planificación (Monitorización solo para bienestar y seguimiento) e impresión en PDF por apartados o como informe completo.

## Novedades de la versión 1.1.0

Propuestas de Manuel Moya Ramón: edad calculada desde la fecha de nacimiento, sexo en desplegable, estatura hasta 230 cm, disponibilidad en días por semana, volumen habitual de 1 a 20 h/semana, modalidades, métodos y periodizaciones previas por separado, tipos de valoración médica en desplegable, lesiones por zona, articulación y musculatura (y arreglo del guardado de lesiones), planificación por niveles, monitorización vinculada al plan, 10 pruebas de evaluación, nuevas variables de análisis y más deportes en el estudio. Además: tres idiomas, tres proveedores de IA, aviso previo al envío y estructura de proyecto Forja. Los datos de la v1.0 guardados en el navegador se abren sin pérdida (los modelos «ondulante» y «microciclo competitivo» pasan a «tradicional» y «deporte colectivo»).

## Autoría y atribución

Realizada entre **Fernando Borrás Rocher** ([ORCID 0000-0002-5519-4573](https://orcid.org/0000-0002-5519-4573)) y **Manuel Moya Ramón** ([ORCID 0000-0002-2291-5899](https://orcid.org/0000-0002-2291-5899)), Universidad Miguel Hernández de Elche. Se apoya en el código de **Entrenamiento 360**, obra de Manuel Moya Ramón, publicada aquí bajo licencia MIT.

Herramienta complementaria para el profesorado: [PlanificaIA Docente](https://github.com/fborrasumh/planificaia-docente).

## Desarrollo

El `index.html` se monta con `python3 build.py` a partir de `src/` (código de la app) y `forja/` (módulos comunes). Pruebas: `python3 tests/full_test.py` y `python3 tests/migracion_test.py` (Playwright, IA simulada).

## Cómo citar

Borrás Rocher, F. y Moya Ramón, M. (2026). *PlanificaIA* (v1.2.0) [Software]. Universidad Miguel Hernández de Elche. DOI: [10.5281/zenodo.23091369](https://doi.org/10.5281/zenodo.23091369)

## Licencia

MIT. Véase [LICENSE](LICENSE).
