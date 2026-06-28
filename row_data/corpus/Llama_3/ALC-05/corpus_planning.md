## Prompt maestro — ALC-05

### 1. Identificación de la pregunta

- **ID:** ALC-05
- **Nivel metodológico:** conceptual-ontológico (definición de clases superiores)
- **Tema:** Arquitectura ontológica para biorreactores multiescala
- **Pregunta:** ¿Cómo se separan ontológicamente el equipo físico, el proceso biológico, el sistema de control, las variables medidas y los datos generados?

### 2. Propósito de la pregunta

La pregunta busca establecer los límites formales entre cinco dominios que suelen confundirse en documentación técnica: el hardware (BioLector XT, Biostat B), lo que ocurre biológicamente dentro, los lazos de control que lo gobiernan, las magnitudes que se miden y la información que se registra. Definir esa separación es condición previa para la ontología OWL/RDF, porque permite crear clases disjuntas, propiedades funcionales y equivalencias entre escalas sin mezclar artefacto con fenómeno.

### 3. Plan de búsqueda documental

**Información técnica requerida:**

- descripción de equipo físico y módulos
- definición de proceso biológico en biorreactores
- arquitectura de control (PID, controladores, software)
- lista de variables medidas in situ
- naturaleza de los datos generados

**Tipos de documentos:** manuales oficiales de fabricante, datasheets, páginas técnicas, revisión regulatoria PAT, artículo de ontología de bioprocesos.

**Repositorios:** sartorius.com, beckman.com/m2p-labs, manualslib, VTT Publications, Stanford BMI.

**Términos ES/EN:**

- ES: "biorreactor equipo físico", "proceso biológico fermentación", "sistema control PID", "variables medidas pH DO"
- EN: "bioreactor physical equipment", "biological process cultivation", "control system PID", "measured variables", "process data"

**Ecuaciones de búsqueda:**

- "BioLector XT" AND "datasheet"
- "Biostat B" AND "control tower" site:sartorius.com
- "bioprocess" AND "monitoring" AND "control"

**Criterios:** inclusión 2021-2026 para manuales vigentes; se acepta VTT 2006 por ser referencia regulatoria PAT aún citada.

### 4. Documentos candidatos encontrados

| ID documento | Título                                                                                | Entidad autora                                       |              Año | Tipo de fuente     | URL/DOI verificable                                                                                                                    | Relación con la pregunta                                       | Decisión preliminar |
| ------------ | ------------------------------------------------------------------------------------- | ---------------------------------------------------- | ---------------: | ------------------ | -------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------- | ------------------- |
| DOC-01       | BioLector XT Microbioreactor – Technical Specifications                               | Beckman Coulter / m2p-labs                           |             2021 | Datasheet oficial  | https://media.beckman.com/-/media/pdf-assets/technical-note/technical-datasheet-biolector-xt.pdf                                       | Define equipo, sensores, rangos                                | Include             |
| DOC-02       | Biostat® B – The Multi-Talented Bioreactor for Research and Development               | Sartorius Stedim Biotech                             |      2021-2023\* | Brochure técnico   | https://www.sartorius.com/download/34576/5/broch-biostat-b-sbi1513-e-1--data.pdf                                                       | Describe equipo físico, control tower, vasos 1-10 L            | Include             |
| DOC-03       | BIOSTAT B Operating Manual – PID Controller Parameters                                | Sartorius Stedim Biotech                             | 2023 (impresión) | Manual             | https://www.manualslib.com/manual/3343908/Sartorius-Stedim-Biotech-Biostat-B.html?page=144                                             | Sistema de control                                             | Include             |
| DOC-04       | BioLector XT Microbioreactor – product page                                           | Beckman Coulter Life Sciences                        |             2024 | Página técnica     | https://goto.beckman.com/en/microbioreactor-for-high-throughput-microfermentation-and-bioprocess-control/                              | Variables monitorizadas, datos                                 | Include             |
| DOC-05       | Knowledge-Based Bioprocess Design for Protein Therapeutic Manufacturing               | Stanford University (Bay Ontology Protein Solutions) |            ~2020 | Proyecto académico | http://web.stanford.edu/class/biomedin210/Previous Projects/knowledge_based_protein_therapeutics_design.pdf                            | Propuesta de clases ontológicas (Vessel, Protocol, Experiment) | Include             |
| DOC-06       | Process analytical technology (PAT) needs and applications in the bioprocess industry | VTT Technical Research Centre                        |             2006 | Informe técnico    | https://www.researchgate.net/publication/240935706_Process_analytical_technology_PAT_needs_and_applications_in_the_bioprocess_industry | Define bioproceso, mediciones básicas, control                 | Include             |

### 5. Evaluación de documentos candidatos

| ID documento | Relevancia | Autoridad | Trazabilidad | Cobertura de la pregunta                | Evidencia localizable                                                                                                                      | Justificación                              |
| ------------ | ---------- | --------- | ------------ | --------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------ |
| DOC-01       | Alta       | Alta      | Alta         | Equipo, sensores, variables             | Rangos pH 4-7.5, DO 0-100%, temperatura 10-50°C                                                                                            | Fuente primaria fabricante                 |
| DOC-02       | Alta       | Alta      | Alta         | Equipo físico, control, escalas 1-10 L  | Vasos 1 L,2 L,5 L,10 L; control tower contiene módulos aeración, bomba, temperatura                                                        | Brochure oficial                           |
| DOC-03       | Media      | Alta      | Alta         | Sistema control PID                     | Definición parámetros P,I,D                                                                                                                | Manual operativo                           |
| DOC-04       | Alta       | Alta      | Media        | Variables medidas, datos                | "rapidly evaluate biomass, pH, dissolved oxygen (DO)"; "Superior Data Quality: Continuous monitoring"                                      | Página oficial                             |
| DOC-05       | Media      | Media     | Media        | Separación ontológica                   | Clases: Publication, Experiment, Culture, Organism, Product, Protocol, Vessel, Chemical; propiedades control: deadband, duration, setpoint | Propuesta académica, útil como antecedente |
| DOC-06       | Alta       | Alta      | Alta         | Definición proceso, mediciones, control | "bioprocess, generally associated with cultivation in appropriate bioreactors"; mediciones físicas y químicas in situ                      | Revisión regulatoria ampliamente citada    |

### 6. Corpus documental seleccionado

| ID documento | Documento seleccionado | Pregunta asociada | Fragmentos relevantes                                  | Estado       |
| ------------ | ---------------------- | ----------------- | ------------------------------------------------------ | ------------ |
| DOC-01       | BioLector XT datasheet | ALC-05            | pH optodes, DO optodes, control PI                     | Seleccionado |
| DOC-02       | Biostat B brochure     | ALC-05            | equipo físico, control tower, control automático pH/DO | Seleccionado |
| DOC-03       | Biostat B manual PID   | ALC-05            | parámetros P,I,D                                       | Seleccionado |
| DOC-04       | BioLector XT página    | ALC-05            | variables monitorizadas, calidad de datos              | Seleccionado |
| DOC-05       | Stanford ontology      | ALC-05            | clases candidatas                                      | Seleccionado |
| DOC-06       | VTT PAT                | ALC-05            | definición bioproceso y mediciones                     | Seleccionado |

### 7. Respuesta basada en evidencia

**Evidencia explícita:**

- **Equipo físico** es el artefacto tangible. DOC-02 describe Biostat B como control tower que "contiene módulos de aireación, bomba y control de temperatura" y vasos Univessel Glass de "1 L, 2 L, 5 L and 10 L". DOC-01 detalla BioLector XT con dimensiones, peso 58 kg, y módulos opcionales.

- **Proceso biológico** es la actividad de cultivo, distinta del hardware. DOC-06 lo define: "The bioprocess, generally associated with cultivation in appropriate bioreactors (fermenters), includes the cultivation of the living biocatalyst". DOC-04 lo ejemplifica: "high-throughput microbial fermentation" con evaluación de biomasa.

- **Sistema de control** es la lógica que actúa sobre el equipo. DOC-03 establece que la adaptación de controladores PID requiere ajustar "P, I, or D". DOC-02 especifica "Automatic pH Control" por adición ácido/base y "Automatic DO Control" con controlador avanzado. DOC-01 añade control PI microfluídico con "Fully editable PI control".

- **Variables medidas** son magnitudes físicas/químicas captadas por sensores. DOC-01 lista "0 – 100 % dissolved oxygen" y "pH 4 – 7.5". DOC-06 enumera mediciones básicas in situ: "physical (temperature, weight, pressure, gas and liquid flow... ) and chemical measurements (pH, pO2)".

- **Datos generados** son registros digitales derivados de las mediciones. DOC-02 indica que BioPAT MFCS es solución "for capturing, storing and visualizing process data". DOC-04 afirma "Superior Data Quality: Continuous monitoring improves reproducibility".

**Inferencia razonable basada en evidencia:**
La separación ontológica no es meramente funcional sino mereológica: el equipo _alberga_ sensores, el sistema de control _implementa_ algoritmos que _actúan_ sobre actuadores, las variables son _propiedades observables_ del proceso, y los datos son _representaciones_ de esas variables en un momento dado. DOC-05 apoya esta distinción al modelar Vessel (equipo), Protocol (control), y data properties como setpoint separados de la entidad física.

**Información no establecida en el corpus:**
No se encontró en los documentos una taxonomía OWL formal publicada por Sartorius o Beckman que defina explícitamente las cinco clases como disjuntas. Tampoco hay mapeo estándar entre "datos" y "información" según ISA-88 en estos manuales.

### 8. Tabla de afirmaciones y evidencia

| ID evidencia | Afirmación                                                  | Tipo      | Documento | Página/sección | Fragmento fiel                                                                                                             | Confianza | Validación experta |
| ------------ | ----------------------------------------------------------- | --------- | --------- | -------------- | -------------------------------------------------------------------------------------------------------------------------- | --------- | ------------------ |
| E1           | Equipo físico incluye control tower y vasos 1-10 L          | Explícita | DOC-02    | Brochure p.2-4 | "Our proven autoclavable borosilicate glass culture vessel is available in four different volumes: 1 L, 2 L, 5 L and 10 L" | Alta      | No requerida       |
| E2           | Sistema control contiene módulos aeración/bomba/temperatura | Explícita | DOC-02    | p.5            | "The control tower contains both the aeration, pump and temperature control modules"                                       | Alta      | No                 |
| E3           | Control PID usa parámetros P,I,D                            | Explícita | DOC-03    | p.144          | "Setting the 'P', 'I', or 'D' Controller Parameters"                                                                       | Alta      | No                 |
| E4           | Proceso biológico = cultivo en biorreactor                  | Explícita | DOC-06    | p.3            | "bioprocess... includes the cultivation of the living biocatalyst"                                                         | Alta      | No                 |
| E5           | Variables medidas incluyen pH 4-7.5 y DO 0-100%             | Explícita | DOC-01    | specs          | "pH 4 – 7.5"; "0 – 100 % dissolved oxygen"                                                                                 | Alta      | No                 |
| E6           | Datos generados son capturados por MFCS                     | Explícita | DOC-02    | p.8            | "BioPAT MFCS is a 'plugandplay' solution... for capturing, storing and visualizing process data"                           | Alta      | No                 |
| E7           | Variables medidas básicas incluyen temperatura, pH, pO2     | Explícita | DOC-06    | p.6            | "physical (temperature... ) and chemical measurements (pH, pO2)"                                                           | Alta      | No                 |
| E8           | Ontología previa separa Vessel, Protocol, Experiment        | Inferida  | DOC-05    | métodos        | Clases listadas                                                                                                            | Media     | Requiere           |

### 9. Conceptos ontológicos candidatos

| Concepto candidato | Tipo sugerido                 | Definición basada en evidencia                                  | Fuente         | Estado    |
| ------------------ | ----------------------------- | --------------------------------------------------------------- | -------------- | --------- |
| PhysicalEquipment  | Clase                         | Artefacto tangible que alberga el cultivo (control tower, vaso) | DOC-02         | Candidato |
| BioreactorVessel   | Subclase de PhysicalEquipment | Recipiente con volumen definido (1-10 L, 800-2400 µL)           | DOC-02, DOC-01 | Candidato |
| Sensor             | Subclase de PhysicalEquipment | Dispositivo que mide pH, DO                                     | DOC-01         | Candidato |
| Actuator           | Subclase de PhysicalEquipment | Bomba, válvula, agitador                                        | DOC-02         | Candidato |
| BiologicalProcess  | Clase                         | Cultivo de biocatalizador en biorreactor                        | DOC-06         | Candidato |
| ControlSystem      | Clase                         | Conjunto de controladores y software que regulan                | DOC-03, DOC-02 | Candidato |
| Controller         | Subclase de ControlSystem     | Implementa algoritmo PID/PI                                     | DOC-03         | Candidato |
| MeasuredVariable   | Clase                         | Magnitud observable (pH, DO, temperature)                       | DOC-06, DOC-01 | Candidato |
| ProcessData        | Clase                         | Registro digital de variable en tiempo                          | DOC-02         | Candidato |
| ControlProtocol    | Concepto auxiliar             | Conjunto de setpoint, deadband, duration                        | DOC-05         | Candidato |

### 10. Relaciones ontológicas candidatas

| Relación candidata | Dominio sugerido  | Rango sugerido    | Significado                 | Evidencia                 | Estado    |
| ------------------ | ----------------- | ----------------- | --------------------------- | ------------------------- | --------- |
| hosts              | PhysicalEquipment | Sensor            | equipo alberga sensor       | DOC-01 optodes integrados | Candidato |
| implements         | ControlSystem     | Controller        | sistema ejecuta controlador | DOC-03 PID                | Candidato |
| regulates          | ControlSystem     | BiologicalProcess | control actúa sobre proceso | DOC-02 pH control         | Candidato |
| measures           | Sensor            | MeasuredVariable  | sensor captura variable     | DOC-01 DO/pH              | Candidato |
| generates          | Sensor            | ProcessData       | medición produce dato       | DOC-02 MFCS               | Candidato |
| hasSetpoint        | ControlProtocol   | MeasuredVariable  | protocolo define objetivo   | DOC-05 setpoint           | Candidato |
| hasWorkingVolume   | BioreactorVessel  | xsd:float         | volumen operativo           | DOC-02 1-10 L             | Candidato |

### 11. Triadas RDF candidatas

- **BiostatBControlTower -> rdf:type -> PhysicalEquipment** — DOC-02, sección control tower — estado: soportada
- **BiostatBControlTower -> hosts -> TemperatureControlModule** — DOC-02 — soportada
- **UnivesselGlass5L -> rdf:type -> BioreactorVessel** — DOC-02 — soportada
- **BioLectorXT -> measures -> DissolvedOxygen** — DOC-01 — soportada
- **PIDController -> implements -> ControlAlgorithm** — DOC-03 — parcialmente soportada (requiere validación término)
- **AutomaticPHControl -> regulates -> BiologicalProcess** — DOC-02 — soportada
- **ProcessData -> isGeneratedBy -> Sensor** — DOC-02 MFCS — requiere validación experta

### 12. Sinónimos y variantes terminológicas

| Término principal | Sinónimos documentados                     | Idioma | Documento      |
| ----------------- | ------------------------------------------ | ------ | -------------- |
| PhysicalEquipment | control tower, microbioreactor, bioreactor | EN     | DOC-02, DOC-01 |
| BiologicalProcess | cultivation, fermentation, bioprocess      | EN     | DOC-06         |
| ControlSystem     | DCU, local control, PI controller          | EN     | DOC-02, DOC-03 |
| MeasuredVariable  | process parameter, cultivation parameter   | EN     | DOC-04, DOC-06 |
| ProcessData       | process data, monitoring data              | EN     | DOC-02         |

### 13. Vacíos, riesgos y decisiones pendientes

- No hay ontología oficial de Sartorius/Beckman publicada; la separación se infiere de manuales, no de modelo OWL existente.
- Ambigüedad entre "sistema de control" y "software supervisor" (MFCS vs DCU); requiere modelar jerarquía.
- Falta definición explícita de "dato" vs "información" en documentos; DOC-05 sugiere data properties pero sin ontología de proveniencia.
- Equivalencias funcionales entre escalas (48 pocillos vs 5 L) no están cuantificadas en corpus; se necesitarán estudios de escalado.
- Validación experta necesaria para distinguir Actuator de Sensor en microfluídica BioLector.

### 14. Registro metodológico

Se analizó la pregunta ALC-05 mediante búsqueda dirigida en documentación oficial de Beckman Coulter y Sartorius (2021-2024) y literatura técnica PAT (VTT 2006) y académica (Stanford). Se aplicaron criterios de inclusión centrados en trazabilidad de fabricante y evidencia extraíble de especificaciones. El corpus de seis documentos permitió separar explícitamente: equipo físico (control tower, vasos 1-10 L, BioLector XT), proceso biológico (cultivo), sistema de control (PID/PI, control automático pH/DO), variables medidas (pH 4-7.5, DO 0-100%, temperatura, etc.) y datos generados (captura MFCS). A partir de ello se propusieron clases candidatas en inglés y relaciones tipo hosts, regulates, measures, generates. La limitación principal es la ausencia de una ontología publicada por los fabricantes; por tanto las triadas quedan como candidatas pendientes de validación con expertos de bioprocesos.

### 15. Estado final

- **Nivel de confianza general:** Medio (evidencia sólida de manuales, pero sin ontología formal de referencia)
- **Estado de la respuesta:** Parcialmente soportada (separación conceptual demostrada, formalización OWL pendiente)
- **Estado del corpus:** Parcial (suficiente para definir clases, insuficiente para equivalencias entre escalas)
- **Próxima acción recomendada:** Suministrar manuales completos de BioLector XT (versión con microfluídica) y de Biostat B-DCU 5L/10L, y validar con ingeniero de procesos las relaciones ControlSystem-regulates-BiologicalProcess para modelar en OWL.
