# ALC-05 — Registro metodológico completo

---

## 1. Identificación de la pregunta

| Campo                  | Valor                                                                                                                                        |
| ---------------------- | -------------------------------------------------------------------------------------------------------------------------------------------- |
| **ID**                 | ALC-05                                                                                                                                       |
| **Nivel metodológico** | Ontológico-arquitectural (separación de capas conceptuales)                                                                                  |
| **Tema**               | Separación ontológica de capas: equipo físico, proceso biológico, sistema de control, variables medidas y datos generados                    |
| **Pregunta**           | ¿Cómo se separan ontológicamente el equipo físico, el proceso biológico, el sistema de control, las variables medidas y los datos generados? |

---

## 2. Propósito de la pregunta

Esta pregunta es arquitecturalmente fundamental: define cuántas capas o módulos tendrá la ontología de biorreactores y qué tipo de entidad OWL representa cada capa. Sin esta separación, clases como `Sensor`, `Observation`, `BiologicalProcess` y `MeasuredValue` colapsarían en una jerarquía plana e inconsistente, impidiendo la reutilización, el razonamiento automático y la interoperabilidad con ontologías estándar (BFO, SSN/SOSA, IOF).

La respuesta a ALC-05 establece el **esqueleto de módulos** de la ontología BioLector XT / Sartorius y define qué ontologías externas deben importarse (BFO, SSN/SOSA, IOF Core), qué clases heredan de ellas y qué relaciones cruzan capas.

---

## 3. Plan de búsqueda documental

### Información técnica requerida

- Marcos de referencia para separar equipo físico de proceso y de control en ontologías industriales
- Ontologías de sensores, observaciones y datos (SSN/SOSA, W3C)
- Ontologías fundacionales para entidades físicas vs. procesos vs. información (BFO)
- Aplicaciones de estos marcos a biorreactores o bioprocesos
- Estándares industriales de control por lotes (ISA-88, ISA-95) y su formalización OWL

### Tipos de documentos necesarios

- Especificaciones técnicas W3C/OGC (SSN, SOSA)
- Artículos científicos revisados por pares sobre ontologías de bioprocesos
- Documentación técnica de ontologías fundacionales (BFO, IOF Core)
- Estándares industriales ISA-88 / ISA-95

### Repositorios y bases de datos sugeridos

- W3C TR (w3.org/TR/vocab-ssn)
- OGC Standards (ogc.org)
- PubMed / PMC
- bioRxiv
- NIST Publications (nist.gov/publications)
- GitHub: BFO-ontology, IOF, lewiscelllabs/mcbo

### Términos de búsqueda

| Español                                           | Inglés                                              |
| ------------------------------------------------- | --------------------------------------------------- |
| Separación ontológica equipo proceso control      | Ontological separation equipment process control    |
| Ontología bioprocesos biorreactor OWL             | Bioprocess ontology bioreactor OWL                  |
| BFO continuant occurrent proceso entidad material | BFO continuant occurrent process material entity    |
| SSN SOSA sensor observación dato                  | SSN SOSA sensor observation data                    |
| ISA-88 ISA-95 modelo físico control OWL           | ISA-88 ISA-95 physical model procedural control OWL |

### Ecuaciones de búsqueda sugeridas

- `OWL ontology bioreactor equipment process control separation SSN SOSA`
- `BFO Basic Formal Ontology continuant occurrent material entity process data item OWL`
- `NIST IOF biomanufacturing ontology BFO physical equipment process control data`
- `ISA-88 ISA-95 ontology equipment physical model process control separation OWL bioreactor`
- `MCBO mammalian cell bioprocessing ontology bioreactor sensor observation data 2025 2026`

---

## 4. Documentos candidatos encontrados

| ID doc | Título                                                                                                 | Entidad autora                       | Año  | Tipo                                         | URL/DOI verificable                                                                                                     | Relación con la pregunta                                                                         | Decisión  |
| ------ | ------------------------------------------------------------------------------------------------------ | ------------------------------------ | ---- | -------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------ | --------- |
| D01    | Semantic Sensor Network Ontology (SSN/SOSA 2017)                                                       | W3C / OGC                            | 2017 | Especificación técnica W3C                   | https://www.w3.org/TR/vocab-ssn/                                                                                        | Define separación entre sensor, observación, resultado, feature of interest y actuador           | Include   |
| D02    | SSN 2023 Edition (Draft)                                                                               | W3C / OGC SDW WG                     | 2023 | Especificación técnica W3C (Draft)           | https://w3c.github.io/sdw-sosa-ssn/ssn/                                                                                 | Versión actualizada; introduce colecciones de observación y jerarquía de procedimientos          | Include   |
| D03    | The modular SSN ontology: A joint W3C and OGC standard (Semantic Web Journal)                          | Haller et al.                        | 2019 | Artículo científico revisado por pares       | https://dl.acm.org/doi/abs/10.3233/SW-180320                                                                            | Descripción formal de la arquitectura SSN/SOSA, separación sensor-observación-muestra            | Include   |
| D04    | MCBO: Mammalian Cell Bioprocessing Ontology (bioRxiv preprint)                                         | Robasky et al.                       | 2026 | Preprint (no peer-reviewed aún)              | https://doi.org/10.64898/2026.01.05.697007                                                                              | Aplica BFO + IOF a bioprocesos con biorreactores; separa proceso de cultivo, condiciones y datos | Include   |
| D05    | Towards Ontologizing a Digital Twin Framework for Manufacturing (NIST)                                 | Drobnjaković et al.                  | 2023 | Artículo técnico NIST (conferencia ASME CIE) | https://tsapps.nist.gov/publication/get_pdf.cfm?pub_id=936637                                                           | Ilustra separación entre equipo físico (OME), sistema de control y datos via BFO/IOF             | Include   |
| D06    | A BFO-Based Ontological Modeling for Plan and Occurrence: Biomanufacturing Process Verification (NIST) | Šormaz, Kulvatunyou et al.           | 2024 | Artículo técnico NIST (conferencia ASME CIE) | https://www.nist.gov/publications/basic-formal-ontology-based-ontological-modeling-plan-and-occurrence-biomanufacturing | Aplica BFO a separación plan/proceso/ocurrencia en biorreactor fed-batch                         | Include   |
| D07    | Basic Formal Ontology (BFO) — Wikipedia / ISO 21838-2:2021                                             | Smith et al. / ISO                   | 2021 | Estándar internacional ISO (referenciado)    | https://en.wikipedia.org/wiki/Basic_Formal_Ontology (referencia al ISO/IEC 21838-2:2021)                                | Marco fundacional para separar continuants (equipo, datos) de occurrents (procesos)              | Include   |
| D08    | ISA-88 Formalization: A Step Towards Integration with ISA-95                                           | Esteras-Chópite et al.               | 2014 | Artículo científico (taller FOMI, CEUR)      | https://ceur-ws.org/Vol-1333/fomi2014_4.pdf                                                                             | Formalización OWL de ISA-88; separación modelo físico / modelo procedimental                     | Include   |
| D09    | Data Infrastructure for Biomanufacturing Process Control (NIST)                                        | NIST                                 | 2025 | Página de proyecto institucional NIST        | https://www.nist.gov/programs-projects/data-infrastructure-biomanufacturing-process-control                             | Describe arquitectura hub-and-spoke BFO+IOF para bioprocesos; referencia a ISA-88/95             | Include   |
| D10    | NyctiDB: A non-relational bioprocesses modeling database supported by an ontology (Frontiers)          | Guedas et al.                        | 2022 | Artículo científico revisado por pares       | https://www.frontiersin.org/articles/10.3389/fceng.2022.1036867/full                                                    | Ontología de componentes de bioprocesos (variables, modelos, condiciones)                        | Uncertain |
| D11    | ISA-88 — Wikipedia                                                                                     | Wikipedia / referencia a ANSI/ISA-88 | 2024 | Referencia enciclopédica (fuente secundaria) | https://en.wikipedia.org/wiki/ISA-88                                                                                    | Descripción del modelo físico y procedimental ISA-88                                             | Uncertain |
| D12    | Building Ontologies with Basic Formal Ontology (libro MIT Press)                                       | Arp, Smith, Spear                    | 2015 | Libro académico (MIT Press)                  | ISBN: 978-0-262-52781-1 (no acceso directo en línea)                                                                    | Capítulo sobre continuants/occurrents/generically dependent continuants relevante para datos     | Uncertain |

---

## 5. Evaluación de documentos candidatos

| ID doc | Relevancia | Autoridad                                       | Trazabilidad                             | Cobertura                                                               | Evidencia localizable                              | Justificación                                                                                           |
| ------ | ---------- | ----------------------------------------------- | ---------------------------------------- | ----------------------------------------------------------------------- | -------------------------------------------------- | ------------------------------------------------------------------------------------------------------- |
| D01    | Alta       | Alta (W3C/OGC, estándar internacional)          | Alta (URL estable, namespace permanente) | Alta — cubre separación sensor/observación/dato/actuador                | Alta — texto completo accesible                    | Estándar de referencia; directamente aplicable a separación de capas de control y datos                 |
| D02    | Alta       | Alta (W3C/OGC SDW WG)                           | Media (draft público, puede cambiar)     | Alta — versión 2023 con extensiones relevantes                          | Alta — URL pública draft                           | Actualización importante que introduce `ObservationCollection`; relevante para datos generados          |
| D03    | Alta       | Alta (Semantic Web Journal, revisado por pares) | Alta (DOI verificable)                   | Alta — describe formalmente la arquitectura modular SSN/SOSA            | Alta — PDF disponible                              | Descripción académica completa de la separación SSN/SOSA                                                |
| D04    | Alta       | Media-Alta (preprint bioRxiv, no peer-reviewed) | Alta (DOI verificable)                   | Alta — aplica BFO+IOF a biorreactores con separación de capas           | Alta — PDF completo disponible                     | Caso de uso directamente en bioprocesos; distingue proceso biológico, condiciones y datos               |
| D05    | Alta       | Alta (NIST, revisado institucionalmente)        | Alta (URL NIST estable)                  | Alta — figura de separación equipo/control/datos en biorreactor         | Alta — PDF disponible                              | Contiene figuras explícitas de separación ontológica para biorreactor                                   |
| D06    | Alta       | Alta (NIST/ASME CIE, revisado)                  | Alta (URL NIST estable)                  | Alta — BFO plan vs. occurrencia en biofabricación                       | Alta — disponible en NIST                          | Directamente aplicable a separación proceso planeado vs. ocurrencia real vs. equipo                     |
| D07    | Alta       | Alta (ISO 21838-2:2021, standard internacional) | Alta (referencia ISO verificable)        | Alta — base fundacional de todo el esquema de capas                     | Media — Wikipedia como proxy; texto ISO no abierto | BFO es el marco fundacional indispensable; la página Wikipedia es verificable con referencias primarias |
| D08    | Media      | Media (taller FOMI, no revista top)             | Alta (CEUR-WS, URL estable)              | Media — formalización OWL de ISA-88, no directamente biorreactor        | Alta — PDF disponible en CEUR-WS                   | Útil para separación modelo físico / procedimental ISA-88 en OWL                                        |
| D09    | Alta       | Alta (NIST, proyecto institucional)             | Alta (URL NIST estable)                  | Media — descripción del proyecto, no artículo técnico completo          | Media — descripción de proyecto, no artículo       | Contextualiza la arquitectura IOF para bioprocesos; señala ISA-88/95 como base                          |
| D10    | Media      | Media (Frontiers, revisado por pares)           | Alta (URL Frontiers estable)             | Media — ontología de componentes de bioprocesos, no de control o equipo | Alta — acceso abierto                              | Relevante para componentes de procesos y datos; menos relevante para separación de capas de control     |
| D11    | Baja       | Baja (fuente secundaria)                        | Media                                    | Baja — descripción general de ISA-88                                    | Alta — URL estable                                 | Útil solo como referencia de definición; se prefieren fuentes primarias                                 |

---

## 6. Corpus documental seleccionado

| ID doc | Documento seleccionado                                               | Pregunta asociada | Secciones/fragmentos relevantes                                                                                                                             | Estado                                                   |
| ------ | -------------------------------------------------------------------- | ----------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------- |
| D01    | W3C SSN/SOSA Ontology (2017)                                         | ALC-05            | Secciones: SOSA core; ssn:System; sosa:Sensor; sosa:Observation; sosa:ObservableProperty; sosa:FeatureOfInterest; sosa:Result; sosa:Actuator                | Verificado, accesible                                    |
| D02    | W3C/OGC SSN 2023 Edition                                             | ALC-05            | Nuevas clases: `ObservationCollection`; `ActuatingProcedure`; `ObservingProcedure`; deprecación de `ssn:Input/Output/Result`                                | Verificado, accesible (draft público)                    |
| D03    | Haller et al. (2019) — Semantic Web Journal                          | ALC-05            | Tablas de clases y relaciones SOSA/SSN; discusión de separación sensor–observación–muestra–resultado                                                        | Verificado, accesible                                    |
| D04    | Robasky et al. (2026) — MCBO bioRxiv                                 | ALC-05            | Definición de `MammalianCellCultureProcess` como intersección de clases BFO/IOF; separación condiciones de cultivo (cualidades BFO) vs. proceso vs. datos   | Verificado, accesible (preprint)                         |
| D05    | Drobnjaković et al. (2023) — NIST/ASME                               | ALC-05            | Figuras 5, 6, 7, 8: separación OME (equipo físico), colección de datos, sistema de control, digital twin; relaciones BFO/IOF aplicadas a biorreactor        | Verificado, accesible                                    |
| D06    | Šormaz & Kulvatunyou et al. (2024) — NIST/ASME                       | ALC-05            | Separación `Plan` vs. `Occurrence` en biofabricación; variables controladas y no controlables; representación de artefactos digitales vs. entidades físicas | Verificado, accesible                                    |
| D07    | BFO (ISO/IEC 21838-2:2021) — referenciado vía Wikipedia y literatura | ALC-05            | División `Continuant` vs. `Occurrent`; subclases: `MaterialEntity`, `GenericallyDependentContinuant`, `Process`, `Quality`                                  | Verificado vía fuentes secundarias; texto ISO no abierto |
| D08    | Esteras-Chópite et al. (2014) — FOMI/CEUR                            | ALC-05            | Formalización en OWL 2 del `PhysicalModel` y `ProceduralControlModel` de ISA-88; módulos ontológicos separados                                              | Verificado, accesible                                    |
| D09    | NIST Data Infrastructure for Biomanufacturing Process Control        | ALC-05            | Descripción de arquitectura hub-and-spoke BFO+IOF; mención explícita de ISA-88/95                                                                           | Verificado, accesible                                    |

---

## 7. Respuesta basada en evidencia

La separación ontológica de las cinco capas que menciona ALC-05 se fundamenta en tres marcos complementarios: **BFO** (marco fundacional), **SSN/SOSA** (capa de sensores, observaciones y datos), y **ISA-88 / IOF Core** (capa de equipo físico y control de proceso). A continuación, la respuesta por capa:

---

### Capa 1 — Equipo físico (_Physical Equipment_)

**Evidencia explícita:**

La estructura de BFO se basa en una división de entidades en dos categorías disjuntas: _continuant_ y _occurrent_. Los continuants consisten en objetos y regiones espaciales, y pueden permanecer a través del tiempo. El biorreactor físico (BioLector XT, Sartorius 5L, Sartorius 10L) es un **`bfo:MaterialEntity`** y más específicamente un **`bfo:Object`**, es decir, un _independent continuant_ que persiste en el tiempo.

En SSN, un `ssn:System` es una abstracción para un dispositivo físico que puede contener otros sistemas. Un sistema se describe en términos de un conjunto de `ssn-system:SystemCapability`, que es una subclase de `ssn:Property` y describe sus capacidades en diversas `ssn-system:Conditions`.

Como ejemplo de ontología de nivel de aplicación para biofabricación, considérese un biorreactor (equipo esencial en biofabricación). Los datos recolectados desde los sensores conectados al biorreactor se usan para actualizar el gemelo digital del biorreactor. La otra dirección representa cómo los resultados de simulación del gemelo digital del biorreactor se usan para controlar los parámetros de los actuadores del biorreactor.

**Inferencia razonable:** El modelo físico de ISA-88 (Process Cell → Unit → Equipment Module → Control Module) se mapea sobre esta capa, siendo cada nivel una subclase de `ssn:System` o `bfo:Object`.

---

### Capa 2 — Proceso biológico (_Biological Process_)

**Evidencia explícita:**

Los continuants son entidades que persisten en el tiempo y pueden someterse a cambios, mientras que los occurrents son entidades que se despliegan en el tiempo y pueden ser cambios de los continuants. Ejemplos paradigmáticos de occurrents se agrupan bajo el término "proceso" o "evento".

El proceso biológico (fermentación, cultivo celular) es un **`bfo:Process`** — un _occurrent_ — que ocurre sobre un intervalo temporal y depende de los participantes materiales (células, biorreactor, medios).

En MCBO, `MammalianCellCultureProcess` se define como la intersección de `CellCultureProcess` con una restricción de participante que requiere al menos una célula mamífera. Esto soporta la clasificación automatizada y evita que las plantillas genéricas de bioprocesamiento se confundan con lógica específica de mamíferos. Para mantener consistencia con BFO, las condiciones ambientales del cultivo se modelan como cualidades (_qualities_) del sistema de cultivo celular material, en consonancia con los principios BFO.

**Inferencia razonable:** Las fases del proceso biológico (inoculación, fase exponencial, cosecha) son `bfo:ProcessualPart` del proceso principal de cultivo.

---

### Capa 3 — Sistema de control (_Control System_)

**Evidencia explícita:**

Con ISA-88, un proceso se considera en términos de módulos, con lógica de control dedicada para cada uno. Cada módulo y su código de control asociado realizan tareas de proceso, pero estas no son específicas del producto. ISA-88 ayuda a entender cómo los pasos involucrados en hacer un producto pueden separarse y convertirse en módulos abstractos. Uno de los primeros pasos es separar la receta del equipo.

SSN/SOSA va más allá de la representación de equipos y también abarca dispositivos de control. Los sistemas pueden implementar procedimientos que ejecutan acciones basadas en entradas de observación. La clase núcleo `ssn:Sensor` y `sosa:Actuator` en SSN/SOSA son vitales para modelar los dispositivos de sensores y actuadores. `sosa:Actuator` son dispositivos que implementan procedimientos SOSA para alterar el estado del entorno. En SOSA, se introduce `sosa:ActuatableProperty` para ayudar a los modeladores a caracterizar qué aspectos de un `sosa:FeatureOfInterest` pueden ser actuados.

El sistema de control se representa mediante la clase `sosa:Actuator` (dispositivos físicos de actuación) junto con `sosa:Actuation` (la ocurrencia de actuación) y los procedimientos de control que implementan. Ontológicamente, el _controlador_ es un continuant (equipo), mientras que _el acto de controlar_ es un occurrent (actuation).

---

### Capa 4 — Variables medidas (_Measured Variables / Observable Properties_)

**Evidencia explícita:**

Las clases núcleo de SSN y SOSA para representación estructurada de datos de sensores incluyen: `Sensor` (dispositivos que realizan observaciones), `Observation` (fenómenos medidos), `Feature of Interest` (entidades del mundo real como frecuencia cardíaca), `ObservableProperty` (características como niveles de oxígeno en sangre), `Stimulus` (que desencadena respuestas del sensor) y `Result` (datos generados como salida).

La ontología SSN describe sensores y sus observaciones, los procedimientos involucrados, los features of interest estudiados, las muestras usadas para hacerlo y las propiedades observadas, así como los actuadores.

Las variables medidas (pH, DO, temperatura, OD) son **`sosa:ObservableProperty`** — propiedades de un `sosa:FeatureOfInterest` (el cultivo o el biorreactor). Son _specifically dependent continuants_ en BFO: cualidades que inhieren en la entidad que las porta.

---

### Capa 5 — Datos generados (_Generated Data_)

**Evidencia explícita:**

Representar el conocimiento del proceso de biofabricación, los modelos de control y las ocurrencias reales en ontologías coherentes podría ayudar tanto a humanos como a computadores a lidiar con la complejidad. Existe una falta de ontologías coherentes para esto. Si bien la ontología IOF Core ha proporcionado una base para tales requisitos ontológicos, aún existen construcciones insuficientes y orientación clara sobre la representación de artefactos digitales y sus correspondencias con las contrapartes físicas.

Los datos generados son **`bfo:GenericallyDependentContinuant`** (artefactos de información), distintos de las propiedades observadas (que son cualidades de entidades físicas). En SSN/SOSA, el resultado de una observación (`sosa:hasResult`) produce un valor que es el dato registrado.

En la edición SSN 2023 se agrega `ObservationCollection`, `ActuationCollection`, `SamplingCollection` y se introducen especializaciones `ActuatingProcedure`, `ObservingProcedure`, `SamplingProcedure` para cada tipo de ejecución.

**Información no establecida en el corpus:** No se localizaron documentos que describan explícitamente cómo los datos generados por BioLector XT o Sartorius se representan en formatos RDF/OWL específicos del fabricante. Esta capa requerirá mapeo manual de los formatos de exportación de datos (CSV, software propietario) a la estructura `sosa:Observation → sosa:hasResult → xsd:double`.

---

## 8. Tabla de afirmaciones y evidencia

| ID evidencia | Afirmación                                                                                                                  | Tipo      | Documento                                           | Sección/página                                                                                                                                                | Resumen fiel                                                                                                                                                                                            | Confianza | Validación experta                                                                     |
| ------------ | --------------------------------------------------------------------------------------------------------------------------- | --------- | --------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------- | -------------------------------------------------------------------------------------- |
| E01          | El biorreactor físico es un `bfo:MaterialEntity` / `bfo:Object` (continuant independiente)                                  | Explícita | D07 (BFO ISO 21838-2)                               | Capítulo 2 (clases BFO); Wikipedia sección "Structure"                                                                                                        | BFO divide entidades en continuants (objetos, cualidades) y occurrents (procesos); el equipo físico es un `MaterialEntity`                                                                              | Alta      | Confirmar con ontólogo BFO                                                             |
| E02          | El proceso biológico de cultivo es un `bfo:Process` (occurrent)                                                             | Explícita | D07 (BFO) + D04 (MCBO)                              | BFO: definición de Process; MCBO: definición de `CellCultureProcess`                                                                                          | MCBO modela `MammalianCellCultureProcess` como subclase de `CellCultureProcess`, un occurrent BFO                                                                                                       | Alta      | Confirmar con experto bioprocesos                                                      |
| E03          | Las condiciones de cultivo (pH, DO, temperatura) son `bfo:Quality` que inhieren en la entidad de cultivo                    | Explícita | D04 (MCBO)                                          | Párrafo de diseño ontológico: "culture environmental conditions are modeled as qualities of the material cell culture system, consistent with BFO principles" | MCBO afirma explícitamente que las condiciones se modelan como cualidades BFO                                                                                                                           | Alta      | Confirmar si `ObservableProperty` SOSA es equivalente o complementaria                 |
| E04          | El sensor es un `ssn:System` / `sosa:Sensor`; el actuador es `sosa:Actuator`                                                | Explícita | D01 (SSN/SOSA), D03                                 | Sección SOSA core: definiciones de Sensor y Actuator                                                                                                          | SSN/SOSA define estas clases con sus propiedades de observación y actuación                                                                                                                             | Alta      | Estándar W3C; sin necesidad de validación adicional                                    |
| E05          | La observación (acto de medir) es `sosa:Observation` (occurrent); la propiedad medida es `sosa:ObservableProperty`          | Explícita | D01 (SSN/SOSA)                                      | SOSA core: clases Observation y ObservableProperty                                                                                                            | SOSA separa el acto de observar de la propiedad observada y del resultado                                                                                                                               | Alta      | Estándar W3C                                                                           |
| E06          | El resultado numérico de la medición es `sosa:hasResult` → valor tipado XSD                                                 | Explícita | D01, D02                                            | SSN/SOSA: relación hasResult; SSN 2023: deprecated `sosa:Result` como clase, se usa valor literal                                                             | Los datos generados son literales o individuos conectados por `hasResult`                                                                                                                               | Alta      | Verificar si el proyecto usa Result como clase o literal                               |
| E07          | El sistema de control se modela con `sosa:Actuator` y `sosa:Actuation`; ISA-88 separa modelo físico de modelo procedimental | Explícita | D08 (ISA-88 OWL), D01 (SOSA)                        | CEUR-WS: módulo procedimental ISA-88 en OWL; SOSA: Actuator/Actuation                                                                                         | ISA-88 separa modelo físico (equipo) de modelo procedimental (control) en módulos OWL separados                                                                                                         | Alta      | Requiere validación con ingeniero de control del proyecto                              |
| E08          | Los datos generados son `bfo:GenericallyDependentContinuant` (artefactos de información)                                    | Inferida  | D05 (NIST Digital Twin), D06 (NIST Plan/Occurrence) | Fig. 5 y 7 D05: "data collection connected to OME and its digital twin"; D06: representación de artefactos digitales                                          | La separación entre entidad física y su gemelo/artefacto digital se basa en `GenericallyDependentContinuant` en BFO; los autores identifican esta distinción como un vacío aún no cubierto por IOF Core | Media     | Requiere validación experta; IOF Core aún desarrolla este aspecto                      |
| E09          | El biorreactor como plataforma SSN puede contener sensores deployados en él                                                 | Explícita | D01 (SSN/SOSA)                                      | Sección `sosa:Platform`: sistema que aloja sensores                                                                                                           | SSN define `sosa:Platform` como entidad que aloja o porta sensores; el biorreactor actuaría como plataforma                                                                                             | Alta      | Confirmar si el biorreactor se modela como Platform o como FeatureOfInterest (o ambos) |
| E10          | ISA-95 separa ERP, MES y control; ISA-88 separa receta de equipo                                                            | Explícita | D08, referencias D09                                | ISA-88: separación receta/equipo; ISA-95: jerarquía funcional                                                                                                 | Ambos estándares son referenciados como base para ontologías de bioprocesos en NIST                                                                                                                     | Alta      | Verificar cuáles niveles de ISA-95 aplican a la escala BioLector/Sartorius             |

---

## 9. Conceptos ontológicos candidatos

| Concepto candidato              | Tipo sugerido                                    | Definición basada en evidencia                                                                                                   | Fuente                | Estado                                     |
| ------------------------------- | ------------------------------------------------ | -------------------------------------------------------------------------------------------------------------------------------- | --------------------- | ------------------------------------------ |
| `PhysicalBioreactor`            | Clase                                            | Entidad material independiente (bfo:Object) que constituye el sistema de biorreactor en una escala dada                          | D07 (BFO), D05 (NIST) | Candidato — requiere validación            |
| `BiologicalCultivationProcess`  | Clase                                            | Proceso occurrent (bfo:Process) que representa el cultivo celular o fermentación dentro del biorreactor                          | D07 (BFO), D04 (MCBO) | Candidato — requiere validación            |
| `ControlSystem`                 | Clase / Subclase de `ssn:System`                 | Sistema físico (continuant) que implementa la lógica de control del biorreactor; contiene sensores y actuadores                  | D01, D08              | Candidato                                  |
| `BioreactorSensor`              | Subclase de `sosa:Sensor`                        | Sensor físico instalado en el biorreactor que realiza observaciones de propiedades del cultivo                                   | D01, D03              | Candidato                                  |
| `BioreactorActuator`            | Subclase de `sosa:Actuator`                      | Dispositivo físico que altera propiedades del entorno de cultivo (agitador, válvula de gas, bomba)                               | D01, D05              | Candidato                                  |
| `CultivationObservableProperty` | Subclase de `sosa:ObservableProperty`            | Propiedad observable del cultivo (pH, DO, temperatura, biomasa, OD) modelada como cualidad BFO de la entidad de cultivo          | D01, D04              | Candidato                                  |
| `CultivationObservation`        | Subclase de `sosa:Observation`                   | Acto singular de medición de una propiedad observable del cultivo en un instante temporal                                        | D01, D02, D03         | Candidato                                  |
| `MeasuredDataRecord`            | Subclase de `bfo:GenericallyDependentContinuant` | Artefacto de información (dato numérico con unidad, timestamp y referencia al sensor) generado como resultado de una observación | D05, D06, D07         | Candidato — definición aún debatida en IOF |
| `ObservationResult`             | Propiedad de dato                                | Valor numérico (xsd:double) con unidad de medida, resultado de una `CultivationObservation`                                      | D01, D02              | Candidato                                  |
| `ControlAction` / `Actuation`   | Subclase de `sosa:Actuation`                     | Acto occurrent mediante el cual un actuador modifica una propiedad actable del entorno de cultivo                                | D01, D05              | Candidato                                  |
| `BioreactorPhysicalModel`       | Concepto auxiliar                                | Módulo ontológico que agrupa todas las entidades físicas del biorreactor (ISA-88 Physical Model)                                 | D08, D09              | Concepto auxiliar                          |
| `CultivationControlModule`      | Concepto auxiliar                                | Módulo ontológico que agrupa los módulos de control de ISA-88 formalizados en OWL                                                | D08                   | Concepto auxiliar                          |

---

## 10. Relaciones ontológicas candidatas

| Relación candidata                 | Dominio sugerido              | Rango sugerido                            | Significado                                                                     | Evidencia                                      | Estado                                   |
| ---------------------------------- | ----------------------------- | ----------------------------------------- | ------------------------------------------------------------------------------- | ---------------------------------------------- | ---------------------------------------- |
| `hostsSystem` / `sosa:hosts`       | `PhysicalBioreactor`          | `BioreactorSensor`, `BioreactorActuator`  | El biorreactor físico aloja (es plataforma de) sensores y actuadores            | D01 (sosa:Platform → sosa:hosts)               | Candidato — posible uso directo de SOSA  |
| `implementsControlSystem`          | `PhysicalBioreactor`          | `ControlSystem`                           | El biorreactor implementa o está gobernado por un sistema de control específico | D05, D08                                       | Candidato — requiere validación          |
| `supportsProcess`                  | `PhysicalBioreactor`          | `BiologicalCultivationProcess`            | El equipo físico soporta (es el sustrato material de) el proceso biológico      | D07 (BFO: proceso depende de entidad material) | Candidato inferido                       |
| `sosa:observes`                    | `BioreactorSensor`            | `CultivationObservableProperty`           | El sensor observa una propiedad específica del cultivo                          | D01 (sosa:Sensor → sosa:observes)              | Soportado directamente por SOSA          |
| `sosa:madeObservation`             | `BioreactorSensor`            | `CultivationObservation`                  | El sensor realizó una observación concreta                                      | D01 (sosa:Sensor → sosa:madeObservation)       | Soportado directamente por SOSA          |
| `sosa:hasFeatureOfInterest`        | `CultivationObservation`      | `PhysicalBioreactor` o entidad de cultivo | La observación tiene como sujeto al biorreactor o al cultivo                    | D01                                            | Soportado directamente por SOSA          |
| `sosa:hasResult` (valor)           | `CultivationObservation`      | `ObservationResult` (literal XSD)         | La observación produce un resultado numérico con unidad                         | D01, D02                                       | Soportado directamente                   |
| `generatesDataRecord`              | `CultivationObservation`      | `MeasuredDataRecord`                      | La observación genera un artefacto de información persistente                   | D05, D06 (inferido)                            | Candidato inferido — requiere validación |
| `sosa:actsOnProperty`              | `ControlAction` / `Actuation` | `sosa:ActuatableProperty`                 | La acción de control modifica una propiedad actable del entorno de cultivo      | D01 (SOSA: Actuation)                          | Soportado directamente por SOSA          |
| `ioc:hasPart` / `ssn:hasSubSystem` | `ControlSystem`               | `BioreactorSensor`, `BioreactorActuator`  | El sistema de control contiene sensores y actuadores como subsistemas           | D01 (ssn:System → ssn:hasSubSystem)            | Soportado por SSN                        |

---

## 11. Triadas RDF candidatas

```
# CAPA 1 — EQUIPO FÍSICO
ex:BioLectorXT_unit01 rdf:type ex:PhysicalBioreactor
    → Documento: D05 (NIST) + D07 (BFO)
    → Estado: requiere validación experta (nomenclatura de individuos)

ex:PhysicalBioreactor rdfs:subClassOf ssn:System
    → Documento: D01 (SSN/SOSA spec)
    → Estado: soportada

ex:PhysicalBioreactor rdfs:subClassOf bfo:MaterialEntity
    → Documento: D07 (BFO ISO 21838-2)
    → Estado: soportada (BFO como top-level)

# CAPA 2 — PROCESO BIOLÓGICO
ex:BiologicalCultivationProcess rdfs:subClassOf bfo:Process
    → Documento: D07 (BFO) + D04 (MCBO: CellCultureProcess → bfo:Process)
    → Estado: soportada

ex:CultivationRun_20240115 rdf:type ex:BiologicalCultivationProcess
    → Documento: D04 (MCBO pattern)
    → Estado: parcialmente soportada (inferida de MCBO)

ex:BiologicalCultivationProcess ex:supportsedBy ex:PhysicalBioreactor
    → Documento: D07 (BFO: proceso depende de material entity)
    → Estado: requiere validación experta (relación BFO exacta)

# CAPA 3 — SISTEMA DE CONTROL
ex:ControlSystem rdfs:subClassOf ssn:System
    → Documento: D01 (SSN), D08 (ISA-88 OWL)
    → Estado: soportada

ex:pH_Controller rdf:type sosa:Actuator
    → Documento: D01 (SOSA: Actuator)
    → Estado: soportada

ex:CO2_Valve_actuation01 rdf:type sosa:Actuation
    → Documento: D01 (SOSA: Actuation)
    → Estado: soportada

ex:CO2_Valve_actuation01 sosa:actsOnProperty ex:CO2SupplyProperty
    → Documento: D01 (SOSA)
    → Estado: soportada

# CAPA 4 — VARIABLES MEDIDAS
ex:pH_Observable rdfs:subClassOf sosa:ObservableProperty
    → Documento: D01 (SOSA)
    → Estado: soportada

ex:DissolvedOxygen_Observable rdfs:subClassOf sosa:ObservableProperty
    → Documento: D01 (SOSA)
    → Estado: soportada

ex:pH_Sensor_BioLectorXT sosa:observes ex:pH_Observable
    → Documento: D01 (SOSA: sosa:observes)
    → Estado: soportada

ex:Observation_pH_001 rdf:type sosa:Observation
    → Documento: D01 (SOSA)
    → Estado: soportada

ex:Observation_pH_001 sosa:hasFeatureOfInterest ex:CultivationMedium_001
    → Documento: D01 (SOSA: hasFeatureOfInterest)
    → Estado: soportada

ex:Observation_pH_001 sosa:observedProperty ex:pH_Observable
    → Documento: D01 (SOSA)
    → Estado: soportada

# CAPA 5 — DATOS GENERADOS
ex:Observation_pH_001 sosa:hasResult "7.2"
    → Documento: D01, D02 (SSN 2023 deprecó clase Result; valor literal)
    → Estado: soportada (con nota: D02 depreca sosa:Result como clase)

ex:MeasuredDataRecord_pH_001 rdf:type bfo:GenericallyDependentContinuant
    → Documento: D05, D06 (NIST: artefactos digitales como GDC)
    → Estado: parcialmente soportada (IOF aún desarrollando este patrón)

ex:MeasuredDataRecord_pH_001 ex:generatedBy ex:Observation_pH_001
    → Documento: D05 (inferido de figura 7 NIST)
    → Estado: requiere validación experta
```

---

## 12. Sinónimos y variantes terminológicas

| Término principal                    | Sinónimos / variantes documentadas                                                                                 | Idioma | Documento     |
| ------------------------------------ | ------------------------------------------------------------------------------------------------------------------ | ------ | ------------- |
| `PhysicalBioreactor`                 | Physical Equipment, Process Equipment, Material Entity (BFO), ssn:System, OME (Object of Manufacturing Enterprise) | EN     | D05, D07, D01 |
| `BiologicalCultivationProcess`       | Bioprocess, Cell Culture Process, Fermentation Process, bfo:Process, MammalianCellCultureProcess (MCBO)            | EN     | D04, D07      |
| `ControlSystem`                      | Control Module (ISA-88), Procedural Control Model, Automation System, ssn:System                                   | EN     | D08, D01      |
| `CultivationObservableProperty`      | Observable Property, Process Variable, Measured Parameter, Quality (BFO), sosa:ObservableProperty                  | EN     | D01, D04      |
| Equipo físico                        | Physical equipment, hardware layer, physical model (ISA-88)                                                        | ES/EN  | D08           |
| Proceso biológico                    | Biological process, cell culture process, bioprocess, fermentation                                                 | ES/EN  | D04           |
| Variables medidas                    | Process variables, observable properties, measured parameters, operational variables                               | ES/EN  | D01, D04      |
| Datos generados                      | Generated data, observation results, measurement data, digital artifacts, data records                             | ES/EN  | D05, D06      |
| `sosa:Observation`                   | Observation act, measurement event, sensing event                                                                  | EN     | D01, D02, D03 |
| `bfo:GenericallyDependentContinuant` | Information artifact, digital artifact, data item, data record                                                     | EN     | D06, D07      |

---

## 13. Vacíos, riesgos y decisiones pendientes

**Información faltante:**

- No se localizaron documentos que describan explícitamente cómo los fabricantes (m2p-labs/Beckman Coulter para BioLector XT, Sartorius) exportan o estructuran sus datos; el mapeo de formatos propietarios a `sosa:Observation` + `sosa:hasResult` deberá hacerse mediante análisis directo de los archivos de exportación.
- No existe evidencia en el corpus de una ontología OWL ya publicada específicamente para BioLector XT o Sartorius 5L/10L.
- El patrón exacto para modelar datos generados como `bfo:GenericallyDependentContinuant` vs. literal XSD directo aún está en debate activo en IOF (evidencia: D06 identifica este como vacío explícito).

**Ambigüedades terminológicas:**

- El biorreactor puede ser simultáneamente `sosa:Platform` (aloja sensores) y `sosa:FeatureOfInterest` (es lo que se observa/controla). Esta dualidad debe resolverse con una decisión de diseño explícita.
- `ObservableProperty` en SOSA es una clase abstracta; su relación con `bfo:Quality` no está formalmente alineada en los documentos encontrados; MCBO la modela como `bfo:Quality`, pero SOSA no importa BFO.
- En SSN 2023 (D02), la clase `sosa:Result` fue **deprecada** y se prefiere el valor literal directamente vía `sosa:hasSimpleResult` o un nodo anónimo. Esto afecta cómo se modela la Capa 5.

**Configuraciones dependientes del equipo:**

- Los sensores del BioLector XT (fluorescencia, biomasa, pH, DO por fibra óptica en microplacas) tienen modalidades distintas a los sensores del Sartorius (sondas de inmersión); la representación como `sosa:Sensor` puede ser la misma clase, pero sus `ssn-system:SystemCapability` y rangos de medida difieren.

**Datos que requieren validación con expertos:**

- La relación exacta en BFO entre el proceso biológico y el equipo físico que lo soporta (¿`participates in`? ¿`occurs in`? ¿relación de sitio?).
- Si los módulos de control de ISA-88 deben ser subclases de `ssn:System` o modelarse de forma diferente.
- La granularidad de la Capa 5: ¿los datos se modelan como literales XSD + metadatos en un nodo blanco, o como individuos de clase `MeasuredDataRecord`?

**Documentos adicionales necesarios:**

- Manual técnico BioLector XT (m2p-labs / Beckman Coulter) — para confirmar tipos de sensores y variables reportadas.
- Manuales Sartorius BIOSTAT A Plus 5L y 10L — para confirmar módulos de control, sensores y protocolo de datos.
- Especificación `sosa:Result` deprecation en SSN 2023 (D02) — lectura completa del draft W3C.
- ISA-88 (ANSI/ISA-88.01-2010) texto completo — para mapeo formal de `PhysicalModel` y `ProceduralControlModel`.

---

## 14. Registro metodológico para el documento de investigación

La pregunta ALC-05 indaga sobre la estrategia ontológica para separar cinco capas conceptuales en sistemas de biorreactores: el equipo físico, el proceso biológico, el sistema de control, las variables medidas y los datos generados. La búsqueda documental se orientó mediante términos como _ontological separation equipment process control OWL_, _BFO continuant occurrent bioprocess_, _SSN SOSA sensor observation data_, e _ISA-88 ISA-95 physical model OWL bioreactor_, consultando repositorios de W3C, OGC, NIST, bioRxiv y CEUR-WS entre 2014 y 2026. Se aplicaron criterios de inclusión que priorizaron estándares W3C/OGC con trazabilidad permanente, publicaciones NIST con revisión institucional, preprints de acceso verificable y artículos revisados por pares en revistas de ontologías. Se excluyeron fuentes sin autoría verificable, blogs comerciales y entradas enciclopédicas sin referencias primarias. El corpus seleccionado (D01–D09) convergió en tres marcos complementarios: (1) **BFO** (ISO/IEC 21838-2:2021) como ontología fundacional que distingue _continuants_ (equipo físico, datos como artefactos de información) de _occurrents_ (proceso biológico, observaciones, actuaciones); (2) **SSN/SOSA** (W3C/OGC, 2017 y 2023) como vocabulario estándar para modelar sensores (`sosa:Sensor`), actuadores (`sosa:Actuator`), observaciones (`sosa:Observation`), propiedades observables (`sosa:ObservableProperty`), features of interest y resultados; y (3) **ISA-88 / IOF Core** (NIST) como referencia para la separación entre el modelo físico de equipos y el modelo procedimental de control en procesos por lotes, formalizado en OWL 2. La evidencia extraída sustenta la separación en cinco capas: equipo físico como `bfo:MaterialEntity` / `ssn:System`; proceso biológico como `bfo:Process`; sistema de control como subconjunto de `ssn:System` con actuadores `sosa:Actuator`; variables medidas como `sosa:ObservableProperty` (con correlato en `bfo:Quality`); y datos generados como `bfo:GenericallyDependentContinuant` o literales XSD ligados mediante `sosa:hasResult`. Los conceptos ontológicos candidatos identificados incluyen `PhysicalBioreactor`, `BiologicalCultivationProcess`, `ControlSystem`, `BioreactorSensor`, `CultivationObservableProperty`, `CultivationObservation` y `MeasuredDataRecord`. Las limitaciones principales son: la ausencia de documentación oficial de fabricantes que permita verificar sensores y estructuras de datos específicas de BioLector XT y Sartorius; la ambigüedad sobre si el biorreactor es `sosa:Platform` o `sosa:FeatureOfInterest`; el estado de debate activo sobre la representación de artefactos digitales en IOF Core; y la deprecación de `sosa:Result` como clase en SSN 2023, que afecta el modelado de la Capa 5. Todos los conceptos y relaciones identificados tienen estatus de **candidatos** hasta su validación por expertos en bioprocesos, ingeniería de ontologías y operación de los sistemas específicos.

---

## 15. Estado final

| Criterio                       | Estado                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| ------------------------------ | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Nivel de confianza general** | **Medio-Alto** — La separación en capas está bien soportada por estándares internacionales (BFO, SSN/SOSA, ISA-88); la aplicación específica a BioLector XT / Sartorius requiere validación adicional                                                                                                                                                                                                                                                                 |
| **Estado de la respuesta**     | **Parcialmente soportada** — Las cinco capas están identificadas y justificadas con evidencia documental; el mapeo exacto a los equipos específicos del proyecto no está en el corpus                                                                                                                                                                                                                                                                                 |
| **Estado del corpus**          | **Parcial** — Suficiente para el nivel ontológico-arquitectural; insuficiente para nivel de individuo (configuraciones reales de los equipos)                                                                                                                                                                                                                                                                                                                         |
| **Próxima acción recomendada** | (1) Suministrar manuales técnicos de BioLector XT y Sartorius BIOSTAT para poblar la Capa 1 con individuos reales. (2) Leer texto completo de SSN 2023 draft (D02) para resolver la deprecación de `sosa:Result`. (3) Consultar la ontología MCBO (D04) en GitHub para revisar sus patrones de modelado de datos de biorreactor y evaluar reutilización directa. (4) Validar con experto la relación BFO entre `BiologicalCultivationProcess` y `PhysicalBioreactor`. |
