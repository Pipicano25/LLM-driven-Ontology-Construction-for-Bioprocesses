# Delimitación inicial del alcance ontológico para BioLector XT y sistemas Sartorius 5 L y 10 L

> **Pregunta ontológica:** ALC-08  
> **Tema:** Exclusiones iniciales para controlar la amplitud de una ontología OWL/RDF de bioprocesos multiescala  
> **Estado del documento:** Resultado de investigación documental preliminar; los conceptos y triadas son candidatos hasta validación experta.

---

## 1. Identificación de la pregunta

- **ID:** ALC-08
- **Nivel metodológico:** Delimitación de alcance ontológico y control de amplitud conceptual.
- **Tema:** Exclusiones iniciales para una ontología OWL/RDF de bioprocesos multiescala centrada en BioLector XT y sistemas Sartorius de 5 L y 10 L.
- **Pregunta:** ¿Qué conceptos deben quedar fuera del alcance inicial para evitar que la ontología sea demasiado amplia?

---

## 2. Propósito de la pregunta

Esta pregunta busca definir una frontera inicial de modelado para la ontología. En ingeniería ontológica, la especificación de requisitos y las _competency questions_ permiten determinar qué conocimiento debe representar la ontología, qué relaciones son necesarias y qué elementos pueden aplazarse a iteraciones posteriores.

Para este proyecto, ALC-08 contribuye directamente a:

1. evitar una ontología excesivamente grande, heterogénea y difícil de validar;
2. concentrar el corpus documental en conceptos observables y trazables;
3. priorizar las preguntas de competencia relacionadas con equipos, escalas, variables, sensores, actuadores, fases y equivalencias funcionales;
4. registrar explícitamente los dominios diferidos para futuras versiones de la ontología.

La metodología LOT plantea una construcción basada en requisitos y desarrollo iterativo. Asimismo, la literatura sobre _competency questions_ indica que estas se utilizan principalmente para delimitar el alcance y evaluar la conceptualización ontológica.

---

## 3. Plan de búsqueda documental

| Componente                       | Detalle                                                                                                                                                                                                                                                                                                                                                         |
| -------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Información técnica requerida    | Capacidades observables de equipos, escalas, volúmenes de trabajo, variables medidas/controladas, modos de proceso, recipientes de cultivo, distinción entre proceso planificado y ejecución real, y dominios potencialmente diferibles.                                                                                                                        |
| Tipos de documentos necesarios   | Páginas oficiales de fabricante, fichas técnicas, manuales, folletos oficiales, artículos científicos revisados por pares, publicaciones institucionales, metodologías de ingeniería ontológica y documentación sectorial verificable.                                                                                                                          |
| Repositorios y sitios sugeridos  | Beckman Coulter, Sartorius, NIST, NIIMBL, OAGi/BMIC, LOT/OEG-UPM, bases bibliográficas académicas y DOI verificables.                                                                                                                                                                                                                                           |
| Términos de búsqueda en español  | `BioLector XT ficha técnica`, `Sartorius 5 L 10 L biorreactor folleto`, `ontología biomanufactura preguntas de competencia`, `delimitación de alcance ontología bioprocesos`, `NIST ontología biomanufactura fed-batch`.                                                                                                                                        |
| Términos de búsqueda en inglés   | `BioLector XT technical data sheet`, `Biostat B 5 L 10 L official brochure`, `competency questions ontology scope`, `biomanufacturing ontology roadmap`, `NIST fed-batch bioreactor ontology`.                                                                                                                                                                  |
| Ecuaciones de búsqueda sugeridas | `site:beckman.com "BioLector XT" ("technical data sheet" OR modules OR "advantages and applications")`; `site:sartorius.com ("Biostat B" OR "Univessel Glass") ("5 L" OR "10 L")`; `("competency questions" AND "ontology scope") filetype:pdf`; `site:nist.gov biomanufacturing ontology fed-batch`; `site:oagi.org biopharmaceutical manufacturing ontology`. |
| Criterios de inclusión           | Fuente real, verificable y accesible; entidad responsable; relación con BioLector XT, Sartorius 5 L/10 L o delimitación ontológica; evidencia localizable y extraíble.                                                                                                                                                                                          |
| Criterios de exclusión           | Blogs sin trazabilidad, duplicados sin valor adicional, páginas comerciales no verificables, fuentes sin autoría o fecha, y documentos no relacionados con la pregunta.                                                                                                                                                                                         |

---

## 4. Documentos candidatos encontrados

| ID documento | Título                                                                                                                         |                  Entidad autora |  Año | Tipo de fuente                          | URL/DOI verificable                                                                                                                                            | Relación con la pregunta                                                                                  | Decisión preliminar |
| ------------ | ------------------------------------------------------------------------------------------------------------------------------ | ------------------------------: | ---: | --------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------- | ------------------- |
| DOC-01       | _BioLector XT - Advantages and Applications_                                                                                   |                 Beckman Coulter | s.f. | Página oficial de producto              | [Sitio oficial](https://www.beckman.com/microbioreactor/biolector-xt/advantages-and-applications)                                                              | Define capacidades y variables nucleares del equipo.                                                      | Include             |
| DOC-02       | _BioLector XT Modules_                                                                                                         |                 Beckman Coulter | s.f. | Página oficial de producto              | [Sitio oficial](https://www.beckman.com/microbioreactor/biolector-xt/modules)                                                                                  | Delimita módulos y funciones base.                                                                        | Include             |
| DOC-03       | _BioLector XT Technical Data Sheet_                                                                                            |                 Beckman Coulter | s.f. | Ficha técnica oficial                   | [Ficha técnica](https://www.beckman.com/resources/reading-material/product-instructions/biolector-xt-technical-data-sheet)                                     | Proporciona parámetros operativos verificables.                                                           | Include             |
| DOC-04       | _Biostat® B Multi-talented bioreactor_                                                                                         |                       Sartorius | 2025 | Folleto oficial PDF                     | [PDF oficial](https://www.sartorius.com/download/34576/broch-biostat-b-sbi1513-e-1--data.pdf)                                                                  | Describe modos de proceso, aplicaciones y configuraciones base asociadas a 5 L y 10 L.                    | Include             |
| DOC-05       | _Univessel® Glass Reliability and Continuity_                                                                                  |                       Sartorius | s.f. | Folleto oficial PDF                     | [PDF oficial](https://www.sartorius.com/download/10336/broch-univesselglass-sbi1554-e-data.pdf)                                                                | Proporciona volúmenes de trabajo y compatibilidad para recipientes de 5 L y 10 L.                         | Include             |
| DOC-06       | _LOT methodology website_                                                                                                      | Ontology Engineering Group, UPM | 2024 | Sitio metodológico oficial              | [LOT](https://lot.linkeddata.es/)                                                                                                                              | Justifica delimitación de alcance mediante requisitos e iteraciones.                                      | Include             |
| DOC-07       | _Use of Competency Questions in Ontology Engineering_                                                                          |               Monfardini et al. | 2023 | Artículo académico                      | [PDF](https://www.inf.ufes.br/~monalessa/wp-content/papercite-data/pdf/use_of_competency_questions_in_ontology_engineering__a_survey_2023.pdf)                 | Aporta evidencia metodológica sobre alcance y preguntas de competencia.                                   | Include             |
| DOC-08       | _A Basic Formal Ontology-Based Ontological Modeling for Plan and Occurrence, a Biomanufacturing Process Verification Use Case_ |                     NIST / ASME | 2024 | Publicación institucional / congreso    | [NIST](https://www.nist.gov/publications/basic-formal-ontology-based-ontological-modeling-plan-and-occurrence-biomanufacturing)                                | Aporta patrón plan–ejecución y fases operativas de biorreactor.                                           | Include             |
| DOC-09       | _Biopharmaceutical Manufacturing Industry Council_                                                                             |                            OAGi | s.f. | Página oficial de iniciativa ontológica | [BMIC](https://oagi.org/pages/biopharmaceutical-manufacturing-industry-council-bmic)                                                                           | Muestra dominios fundacionales y expansiones posteriores.                                                 | Include             |
| DOC-10       | _Open-Sourced Biopharmaceutical Manufacturing Ontology_                                                                        |                          NIIMBL | s.f. | Página oficial de proyecto              | [NIIMBL](https://www.niimbl.org/projects/opensourced-biopharmaceutical-manufacturing-ontology/)                                                                | Explicita interoperabilidad y ciclo de vida amplio del sector.                                            | Include             |
| DOC-11       | _Biostat® B-DCU - Industry Standard Bioreactor_                                                                                |                       Sartorius | s.f. | Página oficial de producto              | [Sartorius](https://www.sartorius.com/en/products/fermentation-bioreactors/benchtop-bioreactors/biostat-b-dcu)                                                 | Es relevante como posible variante, pero no se confirmó que sea el sistema objetivo.                      | Exclude             |
| DOC-12       | _Implementing an ontology and digital data capture to improve biomanufacturing_                                                |                       BioPhorum | 2023 | White paper / página de descarga        | [Página de descarga](https://www.biophorum.com/download/big-data-to-smart-data-implementing-an-ontology-and-digital-data-capture-to-improve-biomanufacturing/) | Potencialmente útil, pero no se recuperó contenido suficiente para extracción fiel durante esta revisión. | Uncertain           |

---

## 5. Evaluación de documentos candidatos

| ID documento | Relevancia | Autoridad | Trazabilidad | Cobertura de la pregunta | Evidencia localizable | Justificación                                                                                     |
| ------------ | ---------- | --------- | ------------ | ------------------------ | --------------------- | ------------------------------------------------------------------------------------------------- |
| DOC-01       | Alta       | Alta      | Alta         | Media                    | Alta                  | Delimita variables observables y controlables en BioLector XT.                                    |
| DOC-02       | Alta       | Alta      | Alta         | Media                    | Alta                  | Describe modularidad y funciones base, útiles para evitar modelar módulos no requeridos.          |
| DOC-03       | Alta       | Alta      | Alta         | Alta                     | Alta                  | Proporciona parámetros técnicos, sensores y opciones microfluídicas.                              |
| DOC-04       | Alta       | Alta      | Alta         | Alta                     | Alta                  | Cubre 5 L y 10 L, modos de proceso y múltiples aplicaciones; muestra el riesgo de sobreextensión. |
| DOC-05       | Alta       | Alta      | Alta         | Media                    | Alta                  | Verifica working volumes y compatibilidad de recipientes.                                         |
| DOC-06       | Alta       | Alta      | Alta         | Alta                     | Alta                  | Justifica una ontología basada en requisitos priorizados e iterativos.                            |
| DOC-07       | Alta       | Alta      | Alta         | Alta                     | Alta                  | Sustenta el papel de las _competency questions_ en alcance y conceptualización.                   |
| DOC-08       | Media      | Alta      | Alta         | Alta                     | Alta                  | Aporta modelado de proceso planificado frente a ejecución real.                                   |
| DOC-09       | Alta       | Alta      | Alta         | Alta                     | Alta                  | Evidencia útil para distinguir núcleo fundacional de extensiones sectoriales.                     |
| DOC-10       | Media      | Alta      | Alta         | Media                    | Alta                  | Muestra que el ciclo de vida _design-to-manufacture_ excede el alcance inicial deseable.          |
| DOC-12       | Media      | Media     | Media        | Media                    | Baja                  | Fuente verificable, pero sin suficiente contenido accesible para extracción textual trazable.     |

---

## 6. Corpus documental seleccionado

> El corpus seleccionado permite construir una respuesta **parcialmente soportada**. Existe evidencia sólida para justificar una delimitación metodológica y técnica, pero no se identificó una lista cerrada y oficial de exclusiones específica para este proyecto.

| ID documento | Documento seleccionado                                      | Pregunta asociada | Fragmentos o secciones relevantes                                     | Estado   |
| ------------ | ----------------------------------------------------------- | ----------------- | --------------------------------------------------------------------- | -------- |
| DOC-01       | BioLector XT - Advantages and Applications                  | ALC-08            | Sección de capacidades, medición en línea y microfluídica.            | Selected |
| DOC-02       | BioLector XT Modules                                        | ALC-08            | Capacidades base y ampliación por módulos.                            | Selected |
| DOC-03       | BioLector XT Technical Data Sheet                           | ALC-08            | `Cultivation conditions` y `Microfluidic features`.                   | Selected |
| DOC-04       | Biostat® B Multi-talented bioreactor                        | ALC-08            | Aplicaciones, tipos celulares, modos de proceso y configuración base. | Selected |
| DOC-05       | Univessel® Glass Reliability and Continuity                 | ALC-08            | Working volumes y compatibilidad de recipientes 5 L/10 L.             | Selected |
| DOC-06       | LOT methodology website                                     | ALC-08            | Requirements specification, implementation y maintenance.             | Selected |
| DOC-07       | Use of Competency Questions in Ontology Engineering         | ALC-08            | Alcance, usos y relaciones sugeridas por las CQs.                     | Selected |
| DOC-08       | NIST BFO-based ontological modeling for plan and occurrence | ALC-08            | Resumen, metodología, caso de estudio y conclusiones.                 | Selected |
| DOC-09       | Biopharmaceutical Manufacturing Industry Council            | ALC-08            | Principios fundacionales y hoja de ruta Year 2/3/Beyond.              | Selected |
| DOC-10       | Open-Sourced Biopharmaceutical Manufacturing Ontology       | ALC-08            | Industry need, approach e impacts.                                    | Selected |

---

## 7. Respuesta basada en evidencia

### Respuesta sustentada a la pregunta

Para evitar que la ontología inicial sea demasiado amplia, su primera iteración debería concentrarse en un **núcleo operacional multiescala de cultivo**. Este núcleo debe cubrir exclusivamente los elementos necesarios para responder las preguntas de competencia iniciales relacionadas con:

- sistemas de biorreactores;
- recipientes y volúmenes de trabajo;
- escalas de operación;
- modos de proceso;
- variables medidas y controladas;
- sensores, actuadores e instrumentos verificados;
- estrategias básicas de control;
- fases del proceso;
- observaciones, muestras, eventos y alarmas mínimas;
- correspondencia entre proceso planificado y ejecución real;
- equivalencias funcionales entre escalas.

La documentación de BioLector XT y Sartorius permite sustentar este núcleo operacional. La metodología LOT y la literatura sobre _competency questions_ justifican construir la ontología de forma iterativa y restringida a requisitos priorizados.

### Evidencia explícita

1. Las _competency questions_ son utilizadas para definir el alcance y evaluar la conceptualización ontológica.
2. La metodología LOT establece una especificación de requisitos y una implementación iterativa por subconjuntos priorizados.
3. El BMIC identifica como núcleo de biomanufactura conceptos de proceso, equipos, estrategias de control, parámetros e indicadores.
4. Las hojas de ruta sectoriales ubican dominios como downstream, interoperabilidad entre proveedores, analítica avanzada y extensiones materiales como expansiones posteriores.
5. BioLector XT y Biostat/Univessel describen capacidades orientadas al cultivo, control y monitoreo de biorreactores; no constituyen documentación de procesos de purificación ni de gestión corporativa integral.

### Inferencia razonable basada en evidencia

Los bloques conceptuales siguientes deben quedar **fuera del alcance inicial**, o modelarse solamente como áreas diferidas:

| Concepto o bloque a dejar fuera inicialmente                                                                 | Tipo de soporte                      | Justificación                                                                                                                                                                        |
| ------------------------------------------------------------------------------------------------------------ | ------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `DownstreamOperation`, `PurificationStep`, `FiltrationStep`, `ChromatographyStep`                            | Inferida con apoyo documental fuerte | El corpus de equipos se concentra en cultivo y control; BMIC trata la expansión a downstream como posterior.                                                                         |
| `CrossEnterpriseIntegration`, `SupplierDataExchange`, `ExternalPartnerRecord`                                | Explícita / inferida                 | La interoperabilidad entre empresas y proveedores pertenece a una capa corporativa amplia, no necesaria para responder preguntas de competencia centradas en equipos de cultivo.     |
| `AdvancedRootCauseAnalysis`, `MultiRunInvestigation`, `AdvancedAnalyticsModel`, `AIMLArtifact`               | Explícita / inferida                 | La hoja de ruta BMIC ubica estas capacidades en fases posteriores. Para la primera versión bastan eventos, alarmas y observaciones mínimas.                                          |
| `ExtendedMaterialOntology`                                                                                   | Explícita                            | Una taxonomía completa de excipientes, consumibles, filtros, estabilidad, disolución y granulometría amplía innecesariamente el alcance inicial.                                     |
| `VaccineManufacturingContext`, `CellTherapyContext`, `PlantCellContext`, `InsectCellContext`, `FungiContext` | Inferida con apoyo medio-alto        | Los equipos sirven múltiples células e industrias. Una taxonomía exhaustiva de aplicaciones multiplicaría clases y relaciones sin ser estrictamente requerida por las CQs iniciales. |
| `FullDigitalThreadArtifact` más allá de `ProcessPlan` y `ActualProcessExecution`                             | Inferida con apoyo fuerte            | No se requiere inicialmente modelar CAD/PLM, scheduling, documentación corporativa completa o ciclo de vida empresarial.                                                             |
| Integraciones, periféricos y módulos opcionales no confirmados                                               | Inferida                             | Deben modelarse solo cuando sean parte comprobada de la configuración real del laboratorio.                                                                                          |
| Regulación, auditoría, gestión documental y trazabilidad GMP completa                                        | Inferida con apoyo documental        | Son dominios relevantes, pero exceden una primera ontología de equipos y ejecución de cultivo. Deben diferirse salvo que una CQ lo exija.                                            |
| Modelado completo de cadena de suministro y logística                                                        | Inferida                             | No es necesario para responder preguntas iniciales sobre escalas, variables, sensores y equivalencias de biorreactores.                                                              |
| Gemelos digitales completos, simulación CFD, control predictivo o modelos mecanísticos detallados            | Inferida                             | Pueden integrarse en fases posteriores; inicialmente basta representar el proceso, sus parámetros y observaciones.                                                                   |

### Información no establecida en el corpus

No se identificó un documento que indique literalmente una lista oficial y cerrada de conceptos excluidos para este proyecto. Por ello, la lista anterior debe considerarse una **propuesta de exclusión candidata**, a validar por el investigador y expertos de dominio.

Tampoco se confirmó mediante manual de laboratorio la configuración exacta de los sistemas denominados solo como “Sartorius 5 L” y “Sartorius 10 L”. Antes de consolidar sensores, bombas, MFCs, software o alarmas específicas, debe verificarse el modelo y los módulos realmente instalados.

---

## 8. Tabla de afirmaciones y evidencia

| ID evidencia | Afirmación                                                                                                                                 | Tipo de evidencia | Documento              | Página/sección                       | Fragmento o resumen fiel                                                                                    | Confianza | Validación experta |
| ------------ | ------------------------------------------------------------------------------------------------------------------------------------------ | ----------------- | ---------------------- | ------------------------------------ | ----------------------------------------------------------------------------------------------------------- | --------- | ------------------ |
| EV-01        | Las _competency questions_ ayudan principalmente a definir el alcance ontológico.                                                          | Explícita         | DOC-07                 | P. 0–1 y p. 15                       | El estudio reporta que las CQs se utilizan principalmente para definir alcance y evaluar conceptualización. | Alta      | No indispensable   |
| EV-02        | La especificación de requisitos debe declarar por qué se construye la ontología y qué requisitos debe cumplir.                             | Explícita         | DOC-06                 | Requirements specification           | LOT establece que esta actividad define motivación, propósito y requisitos.                                 | Alta      | No indispensable   |
| EV-03        | La implementación ontológica puede organizarse por subconjuntos de requisitos priorizados en cada iteración.                               | Explícita         | DOC-06                 | Ontology implementation              | LOT propone planificar el desarrollo conforme a la priorización de requisitos.                              | Alta      | No indispensable   |
| EV-04        | El núcleo de ontologías de biomanufactura cubre procesos, equipos, estrategias de control, parámetros e indicadores.                       | Explícita         | DOC-09                 | BMIC Process WG                      | BMIC define conceptos para equipos, estrategias de control, parámetros de proceso e indicadores.            | Alta      | No indispensable   |
| EV-05        | BMIC trata downstream como una expansión posterior al punto de partida en cell culture.                                                    | Explícita         | DOC-09                 | Process WG / Year 2                  | El roadmap comienza con cell culture y amplía posteriormente hacia downstream.                              | Alta      | No indispensable   |
| EV-06        | Root-cause analysis, multi-run investigations y supplier interoperability aparecen como capacidades posteriores.                           | Explícita         | DOC-09                 | Quality/Materials WG; Year 3; Beyond | El roadmap ubica estos elementos en etapas de evolución posterior.                                          | Alta      | No indispensable   |
| EV-07        | BioLector XT se centra en variables de cultivo como biomasa, pH, DO, fluorescencia, temperatura, agitación y alimentación/control de pH.   | Explícita         | DOC-01, DOC-02, DOC-03 | Capacidades y ficha técnica          | Las fuentes oficiales delimitan las capacidades observables del microbioreactor.                            | Alta      | No indispensable   |
| EV-08        | Biostat B / Univessel cubre recipientes 5 L y 10 L, modos batch/fed-batch/continuous/perfusion y sensores básicos de pH, DO y temperatura. | Explícita         | DOC-04, DOC-05         | Folleto y brochure                   | El material de Sartorius establece recipientes, working volumes y paquetes de control.                      | Alta      | No indispensable   |
| EV-09        | Una taxonomía exhaustiva de dominios biológicos e industriales incrementaría innecesariamente el alcance inicial.                          | Inferida          | DOC-04, DOC-06, DOC-07 | Aplicaciones + alcance por CQs       | Los equipos se aplican a múltiples células e industrias; deben incluirse solo conceptos requeridos por CQs. | Media     | Sí                 |
| EV-10        | No existe en el corpus una lista explícita y cerrada de conceptos excluidos para este proyecto.                                            | No establecida    | Corpus completo        | Revisión completa                    | La decisión final debe ser tomada por el investigador con validación experta.                               | Alta      | Sí                 |

---

## 9. Conceptos ontológicos candidatos

> Todos los conceptos son candidatos y no deben considerarse definitivos antes de validación posterior.

| Concepto candidato       | Tipo sugerido     | Definición basada en evidencia                                                      | Fuente asociada        | Estado    |
| ------------------------ | ----------------- | ----------------------------------------------------------------------------------- | ---------------------- | --------- |
| `BioreactorSystem`       | Clase             | Sistema de cultivo que soporta observación y/o control de parámetros de bioproceso. | DOC-04, DOC-09         | Candidate |
| `Microbioreactor`        | Subclase          | Biorreactor de microescala basado en microplaca, sensores ópticos y microfluídica.  | DOC-01, DOC-03         | Candidate |
| `BenchtopBioreactor`     | Subclase          | Biorreactor de sobremesa compatible con recipientes de cultivo en escala de litros. | DOC-04, DOC-05         | Candidate |
| `CultivationVessel`      | Clase             | Recipiente asociado a un sistema de cultivo.                                        | DOC-04, DOC-05         | Candidate |
| `ProcessMode`            | Clase             | Modo operativo, por ejemplo batch, fed-batch, continuous o perfusion.               | DOC-04                 | Candidate |
| `ProcessParameter`       | Clase             | Parámetro medido o controlado, por ejemplo pH, DO, temperatura o agitación.         | DOC-02, DOC-03, DOC-04 | Candidate |
| `ControlStrategy`        | Clase             | Estrategia usada para mantener o modificar un parámetro de proceso.                 | DOC-03, DOC-04, DOC-09 | Candidate |
| `ProcessPhase`           | Clase             | Fase distinguible de un proceso, por ejemplo crecimiento o producción.              | DOC-08                 | Candidate |
| `PlannedProcess`         | Clase             | Representación del proceso planificado.                                             | DOC-08                 | Candidate |
| `ActualProcessExecution` | Clase             | Ocurrencia real de un proceso ejecutado.                                            | DOC-08                 | Candidate |
| `MeasurementProcess`     | Clase             | Proceso de medición o adquisición de datos relevante para el control y la calidad.  | DOC-09                 | Candidate |
| `QualityAttribute`       | Clase             | Atributo de calidad relevante para el seguimiento del proceso.                      | DOC-09                 | Candidate |
| `MaterialLot`            | Clase             | Lote de material o medio asociado a una ejecución.                                  | DOC-09, DOC-10         | Candidate |
| `InitialOntologyScope`   | Concepto auxiliar | Entidad para registrar la frontera de la primera iteración ontológica.              | DOC-06, DOC-07         | Candidate |
| `DeferredDomainArea`     | Concepto auxiliar | Área semántica diferida a futuras iteraciones.                                      | DOC-06, DOC-09         | Candidate |
| `hasWorkingVolumeValue`  | Propiedad de dato | Valor numérico o rango de volumen de trabajo de un recipiente o sistema.            | DOC-05                 | Candidate |

---

## 10. Relaciones ontológicas candidatas

| Relación candidata        | Dominio sugerido                            | Rango sugerido         | Significado                                                      | Evidencia asociada     | Estado    |
| ------------------------- | ------------------------------------------- | ---------------------- | ---------------------------------------------------------------- | ---------------------- | --------- |
| `hasCultivationVessel`    | `BioreactorSystem`                          | `CultivationVessel`    | Vincula un sistema con su recipiente de cultivo.                 | DOC-04, DOC-05         | Candidate |
| `supportsProcessMode`     | `BioreactorSystem`                          | `ProcessMode`          | Indica modos de operación soportados.                            | DOC-04                 | Candidate |
| `measuresParameter`       | `BioreactorSystem`                          | `ProcessParameter`     | Indica parámetros medidos en línea.                              | DOC-01, DOC-02, DOC-03 | Candidate |
| `controlsParameter`       | `BioreactorSystem`                          | `ProcessParameter`     | Indica parámetros controlados por el sistema.                    | DOC-03, DOC-04         | Candidate |
| `hasControlStrategy`      | `BioreactorSystem`                          | `ControlStrategy`      | Conecta un sistema con sus estrategias de control disponibles.   | DOC-03, DOC-09         | Candidate |
| `hasProcessPhase`         | `PlannedProcess` / `ActualProcessExecution` | `ProcessPhase`         | Descompone un proceso en fases.                                  | DOC-08                 | Candidate |
| `isCounterpartOf`         | `ActualProcessExecution`                    | `PlannedProcess`       | Relaciona una ejecución real con un proceso planificado.         | DOC-08                 | Candidate |
| `hasMeasurementProcess`   | `ActualProcessExecution`                    | `MeasurementProcess`   | Relaciona una ejecución con sus mediciones o registros.          | DOC-09                 | Candidate |
| `usesMaterialLot`         | `ActualProcessExecution`                    | `MaterialLot`          | Relaciona una ejecución con los lotes de materiales usados.      | DOC-09, DOC-10         | Candidate |
| `excludesDomainArea`      | `InitialOntologyScope`                      | `DeferredDomainArea`   | Registra áreas explícitamente excluidas de la primera iteración. | DOC-06, DOC-09         | Candidate |
| `defersToFutureIteration` | `DeferredDomainArea`                        | `InitialOntologyScope` | Marca un dominio como diferido a una iteración futura.           | DOC-06, DOC-09         | Candidate |

---

## 11. Triadas RDF candidatas

| Triada RDF candidata                                                               | Documento de soporte           | Página o sección                              | Estado                      |
| ---------------------------------------------------------------------------------- | ------------------------------ | --------------------------------------------- | --------------------------- |
| `BioLectorXT -> rdf:type -> Microbioreactor`                                       | DOC-01, DOC-03                 | Página de producto y ficha técnica.           | soportada                   |
| `BioLectorXT -> measuresParameter -> DissolvedOxygen`                              | DOC-01, DOC-03                 | Capacidades y condiciones de cultivo.         | soportada                   |
| `BioLectorXT -> supportsControlStrategy -> PHControl`                              | DOC-01, DOC-03                 | Capacidades de control de pH y microfluídica. | soportada                   |
| `BioLectorXT -> supportsControlStrategy -> Feeding`                                | DOC-01, DOC-03                 | Opciones de alimentación y microfluídica.     | soportada                   |
| `BiostatB -> hasCultivationVessel -> UnivesselGlass5L`                             | DOC-04, DOC-05                 | Compatibilidad y recipientes de 5 L.          | soportada                   |
| `BiostatB -> hasCultivationVessel -> UnivesselGlass10L`                            | DOC-04, DOC-05                 | Compatibilidad y recipientes de 10 L.         | soportada                   |
| `FedBatchBioreactorOperationPlan -> hasProcessPhase -> GrowthPhase`                | DOC-08                         | Caso de estudio.                              | soportada                   |
| `FedBatchBioreactorOperationPlan -> hasProcessPhase -> ProductionPhase`            | DOC-08                         | Caso de estudio.                              | soportada                   |
| `ActualProcessExecution -> isCounterpartOf -> PlannedProcess`                      | DOC-08                         | Patrón plan–ocurrencia.                       | soportada                   |
| `InitialOntologyScope -> excludesDomainArea -> DownstreamOperation`                | DOC-09 + síntesis metodológica | Process WG / Year 2.                          | parcialmente soportada      |
| `InitialOntologyScope -> excludesDomainArea -> CrossEnterpriseIntegration`         | DOC-09, DOC-10                 | Roadmap sectorial e interoperabilidad.        | parcialmente soportada      |
| `InitialOntologyScope -> excludesDomainArea -> AdvancedRootCauseAnalysis`          | DOC-09                         | Quality WG / Year 3.                          | parcialmente soportada      |
| `InitialOntologyScope -> excludesDomainArea -> ExtendedMaterialOntology`           | DOC-09                         | Materials WG / Year 2–3.                      | parcialmente soportada      |
| `InitialOntologyScope -> excludesDomainArea -> ApplicationSpecificBiologyTaxonomy` | DOC-04 + síntesis metodológica | Aplicaciones y alcance por CQs.               | requiere validación experta |

---

## 12. Sinónimos y variantes terminológicas

| Término principal   | Sinónimos o variantes documentadas             | Idioma | Documento de soporte |
| ------------------- | ---------------------------------------------- | ------ | -------------------- |
| `Bioreactor`        | `Fermenter`, `bioreactor`                      | Inglés | DOC-11               |
| `DissolvedOxygen`   | `DO`                                           | Inglés | DOC-03, DOC-04       |
| `MicrotiterPlate`   | `MTP`                                          | Inglés | DOC-01, DOC-03       |
| `WorkingVolume`     | `Max. working volume`                          | Inglés | DOC-04, DOC-05       |
| `CultivationVessel` | `Culture vessel`                               | Inglés | DOC-04, DOC-05       |
| `PHControl`         | `Automatic pH Control`, `Triggered pH Control` | Inglés | DOC-03, DOC-04       |

---

## 13. Vacíos, riesgos y decisiones pendientes

1. **Ambigüedad del equipo Sartorius.**  
   Los nombres “Sartorius 5 L” y “Sartorius 10 L” no identifican una configuración única. Es necesario confirmar modelo, controlador, accesorios, sensores y periféricos realmente instalados.

2. **Ausencia de manual técnico de la configuración local.**  
   El corpus incluye material oficial de producto, pero no un manual abierto de la instalación específica. Por ello, no deben fijarse como definitivos sensores, bombas, MFCs, alarmas o software que no estén documentados en el laboratorio.

3. **No existe una lista universal de exclusiones.**  
   La literatura sustenta la construcción iterativa y guiada por requisitos, no una lista cerrada aplicable a todos los proyectos.

4. **Riesgo de sobreextensión biológica.**  
   Modelar desde el inicio todas las especies, líneas celulares, productos, industrias y aplicaciones puede producir una taxonomía difícil de mantener y evaluar.

5. **Riesgo de sobreextensión empresarial.**  
   Integrar al inicio regulación, cadena de suministro, proveedores, gestión documental, trazabilidad GMP completa, ERP/MES/LIMS y analítica avanzada puede desalinear la ontología respecto de sus CQs iniciales.

6. **Decisión pendiente sobre el nivel de granularidad.**  
   Debe definirse si `Sensor`, `Actuator`, `Instrument`, `ControlLoop`, `Alarm`, `Event` y `DataQualityIssue` se modelarán como clases generales, subclases específicas o individuos configurables.

7. **Documentos adicionales necesarios.**
   - Manuales o IFU oficiales de los equipos concretos del laboratorio.
   - SOPs de operación y mantenimiento.
   - Diccionarios de variables del laboratorio.
   - Registros de alarmas, eventos y muestras.
   - Especificación de los módulos instalados en BioLector XT.
   - Validación experta de la matriz CQ–concepto–fuente–prioridad.

---

## 14. Registro metodológico para el documento de investigación

La pregunta ALC-08 se analizó como un problema de delimitación de alcance para una primera versión OWL/RDF orientada a BioLector XT y sistemas Sartorius de 5 L y 10 L. La estrategia documental combinó fuentes oficiales de fabricante, literatura metodológica de ingeniería ontológica, publicaciones institucionales y documentación de iniciativas sectoriales de ontologías de biomanufactura. Se aplicaron criterios de inclusión centrados en verificabilidad, trazabilidad y disponibilidad de evidencia extraíble. El corpus seleccionado mostró que el núcleo inicial debe concentrarse en sistemas de biorreactores, recipientes, escalas, volúmenes de trabajo, modos de proceso, variables operativas, sensores, actuadores, estrategias de control, fases, observaciones y relación entre procesos planificados y ejecutados. A partir de la evidencia se propuso diferir dominios como operaciones downstream, integración interempresarial, analítica avanzada, taxonomías exhaustivas de materiales y aplicaciones, ciclo de vida digital completo, gestión regulatoria integral y periféricos no confirmados. Tales exclusiones se registraron como candidatas y permanecen sujetas a validación de expertos, dado que el corpus no contiene una lista oficial de exclusiones específica para el proyecto y que la configuración real de los equipos Sartorius debe verificarse antes de consolidar el modelo.

---

## 15. Estado final

| Criterio                   | Estado                                                                                                                                                                                                                                                                                |
| -------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Nivel de confianza general | Medio                                                                                                                                                                                                                                                                                 |
| Estado de la respuesta     | Parcialmente soportada                                                                                                                                                                                                                                                                |
| Estado del corpus          | Parcial                                                                                                                                                                                                                                                                               |
| Próxima acción recomendada | Construir y validar una matriz `CQ ↔ concepto ↔ fuente ↔ prioridad ↔ decisión de alcance`, aceptando en la primera iteración solo conceptos estrictamente necesarios para representar equipos, recipientes, volumen de trabajo, parámetros, control, fases y relación plan–ejecución. |
