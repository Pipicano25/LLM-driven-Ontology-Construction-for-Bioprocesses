# 1) ID y pregunta

**ID:** ALC-08
**Pregunta:** ¿Qué conceptos deben quedar fuera del alcance inicial para evitar que la ontología sea demasiado amplia?

# 2) Respuesta basada en evidencia

El corpus **no establece una lista explícita y cerrada de conceptos que deban excluirse** de la ontología inicial.

Sí establece dos criterios para delimitar el alcance:

1. Las preguntas de competencia permiten determinar qué es relevante y qué no lo es para una ontología.
2. La modularización de ontologías contribuye a mantener límites de dominio claros.

Los fragmentos técnicos incluidos evidencian que el núcleo inmediato del corpus se concentra en:

- microbioreactores y biorreactores de banco;
- recipientes de cultivo;
- volúmenes de trabajo;
- medición en línea de biomasa, fluorescencia, pH y DO;
- control de pH;
- alimentación continua;
- experimentos de cultivo.

Por tanto, la exclusión de otros dominios no descritos en el corpus no puede declararse como definitiva. Como inferencia razonable, los componentes no necesarios para responder las preguntas de competencia ni para representar los sistemas de cultivo, medición y control documentados deberían diferirse a módulos posteriores y requerir validación experta.

# 3) Tabla de afirmaciones y evidencia

| ID     | Afirmación                                                                                                                                                  | Texto o fragmento de evidencia                                                                                                                    | Fuente y ubicación                                        | Concepto / relación / triada candidata                                                                                                            | Tipo de evidencia                             | Confianza | Validación experta |
| ------ | ----------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------- | --------- | ------------------ |
| AF-001 | El BioLector XT permite medición en línea de biomasa, fluorescencia, pH y DO.                                                                               | “Disposable 48 well MTPs enable online measurement of biomass, fluorescence, pH and DO...”                                                        | SRC-001; Advantages & Applications, párrafo introductorio | `BioLectorXT measuresOnline Biomass`; `BioLectorXT measuresOnline Fluorescence`; `BioLectorXT measuresOnline pH`; `BioLectorXT measuresOnline DO` | Explícita                                     | Alta      | No                 |
| AF-002 | El BioLector XT incorpora soporte para control simultáneo de pH y alimentación.                                                                             | “...patented microfluidic technology supports simultaneous pH control and feeding.”                                                               | SRC-001; Advantages & Applications, párrafo introductorio | `BioLectorXT supportsPHControl pH`; `BioLectorXT supportsFeeding Feeding`                                                                         | Explícita                                     | Alta      | Sí                 |
| AF-003 | El BioLector XT mide biomasa, pH, DO y fluorescencia durante un experimento de cultivo.                                                                     | “The BioLector XT microbioreactor measures biomass, pH, DO, and fluorescence online while running a cultivation experiment.”                      | SRC-002; BioLector XT Modules, párrafo introductorio      | `Microbioreactor measuresOnline ProcessParameter`; `CultivationExperiment`                                                                        | Explícita                                     | Alta      | No                 |
| AF-004 | El control activo de pH depende de señales en línea.                                                                                                        | “Active control of pH according to online signals...”                                                                                             | SRC-003; Available optional modules, E-XTMF               | `PHControl uses OnlineSignal`                                                                                                                     | Explícita                                     | Alta      | Sí                 |
| AF-005 | La alimentación continua puede involucrar hasta dos soluciones y se asocia con placas microfluídicas.                                                       | “...continuous feeding of up to two solutions only with Microfluidic plates.”                                                                     | SRC-003; Available optional modules, E-XTMF               | `MicrofluidicPlate supports ContinuousFeeding`; `ContinuousFeeding hasMaximumNumberOfSolutions 2`                                                 | Explícita                                     | Alta      | Sí                 |
| AF-006 | Un recipiente de cultivo de vidrio puede estar disponible en volúmenes de 1 L, 2 L, 5 L y 10 L.                                                             | “...culture vessel is available in four different volumes: 1 L, 2 L, 5 L and 10 L.”                                                               | SRC-004; página 3, Univessel® Glass                       | `CultivationVessel hasWorkingVolume Volume1L`; `Volume2L`; `Volume5L`; `Volume10L`                                                                | Explícita                                     | Alta      | No                 |
| AF-007 | Univessel Glass es un recipiente de cultivo para biorreactores de banco Biostat.                                                                            | “The Univessel® Glass is our platform cultivation vessel for all Biostat® benchtop bioreactors.”                                                  | SRC-005; página 1, introducción                           | `UnivesselGlass isCultivationVesselFor BenchtopBioreactor`                                                                                        | Explícita                                     | Alta      | Sí                 |
| AF-008 | Los requisitos priorizados orientan la planificación del desarrollo ontológico.                                                                             | “The ontology developers schedule and plan the ontology development according to the prioritization of the requirements...”                       | SRC-006; Ontology implementation workflow                 | `OntologyRequirement guides OntologyDevelopmentPlan`                                                                                              | Explícita                                     | Media     | No                 |
| AF-009 | Las preguntas de competencia ayudan a determinar qué contenido es relevante para la ontología.                                                              | “By establishing CQs, we reach an effective way to determine what is relevant to the ontology and what is not.”                                   | SRC-007; página 3, Ontologies and Competency Questions    | `CompetencyQuestion determinesRelevanceOf OntologyContent`                                                                                        | Explícita                                     | Alta      | No                 |
| AF-010 | La modularización contribuye a límites claros de dominio.                                                                                                   | “Ontologies will be modularized to ensure scalability, reusability, and clear domain boundaries.”                                                 | SRC-009; Foundational Design Principles, Modularity       | `Ontology hasModule OntologyModule`; `OntologyModule hasDomainBoundary DomainBoundary`                                                            | Explícita                                     | Alta      | Sí                 |
| AF-011 | La relación counterpart permite representar artefactos digitales de manera intuitiva y concisa.                                                             | “Counterpart relation was selected for its ability to facilitate a more intuitive and concise representation of many kinds of digital artifacts.” | SRC-008; resumen de publicación NIST                      | `DigitalArtifact isCounterpartOf DigitalArtifact`                                                                                                 | Explícita                                     | Media     | Sí                 |
| AF-012 | La interoperabilidad de datos puede verse afectada por diferencias entre sistemas informáticos de diseño, análisis y manufactura.                           | “Poor data interoperability... owing to different computerized design, analysis, and manufacturing software and hardware systems.”                | SRC-010; Industry Need                                    | `DataInteroperabilityIssue isAssociatedWith ComputerizedSystem`                                                                                   | Explícita                                     | Media     | Sí                 |
| AF-013 | El corpus permite delimitar el núcleo inicial alrededor de cultivo, medición y control, y diferir elementos no requeridos por las preguntas de competencia. | Basado en AF-001 a AF-010.                                                                                                                        | SRC-001 a SRC-009                                         | `InitialOntologyScope includes CultivationMeasurementAndControlDomain`                                                                            | Inferida                                      | Media     | Sí                 |
| AF-014 | El corpus no permite definir una lista definitiva de dominios excluidos.                                                                                    | No existe un fragmento que enumere exclusiones concretas.                                                                                         | SRC-001 a SRC-010                                         | `No explicit exclusion list established`                                                                                                          | Explícita respecto a la ausencia de evidencia | Alta      | No                 |

# 4) Conceptos candidatos

| Concepto candidato          | Evidencia principal       | Tipo      | Observación                                                        |
| --------------------------- | ------------------------- | --------- | ------------------------------------------------------------------ |
| `Microbioreactor`           | SRC-002                   | Explícita | El BioLector XT se denomina microbioreactor.                       |
| `BenchtopBioreactor`        | SRC-005                   | Explícita | Se mencionan los Biostat benchtop bioreactors.                     |
| `CultivationVessel`         | SRC-004, SRC-005          | Explícita | Aparecen las expresiones culture vessel y cultivation vessel.      |
| `WorkingVolume`             | SRC-005                   | Explícita | Se indican volúmenes de trabajo de 1 L, 2 L, 5 L y 10 L.           |
| `CultivationExperiment`     | SRC-002                   | Explícita | Se menciona running a cultivation experiment.                      |
| `OnlineMeasurement`         | SRC-001, SRC-002          | Explícita | Se documenta medición en línea.                                    |
| `Biomass`                   | SRC-001, SRC-002          | Explícita | Variable medida en línea.                                          |
| `Fluorescence`              | SRC-001, SRC-002          | Explícita | Variable medida en línea.                                          |
| `pH`                        | SRC-001, SRC-002, SRC-003 | Explícita | Variable medida y controlada.                                      |
| `DO`                        | SRC-001, SRC-002          | Explícita | Variable medida en línea.                                          |
| `PHControl`                 | SRC-001, SRC-003          | Explícita | Se documenta control de pH.                                        |
| `ContinuousFeeding`         | SRC-003                   | Explícita | Se documenta alimentación continua.                                |
| `MicrofluidicPlate`         | SRC-003                   | Explícita | Se asocia con control de pH y alimentación continua.               |
| `OnlineSignal`              | SRC-003                   | Explícita | Señal utilizada para control activo de pH.                         |
| `CompetencyQuestion`        | SRC-007                   | Explícita | Elemento metodológico para delimitar relevancia.                   |
| `OntologyRequirement`       | SRC-006                   | Explícita | Requisito que puede ser priorizado.                                |
| `OntologyModule`            | SRC-009                   | Explícita | Elemento para modularizar la ontología.                            |
| `DomainBoundary`            | SRC-009                   | Explícita | Límite de dominio asociado a la modularización.                    |
| `DigitalArtifact`           | SRC-008                   | Explícita | Entidad asociada a la relación counterpart.                        |
| `DataInteroperabilityIssue` | SRC-010                   | Explícita | Problema de interoperabilidad de datos.                            |
| `ComputerizedSystem`        | SRC-010                   | Explícita | Sistemas de software y hardware de diseño, análisis y manufactura. |

# 5) Relaciones candidatas con dominio y rango sugeridos

| Relación candidata          | Dominio sugerido            | Rango sugerido            | Evidencia        | Tipo      | Validación experta |
| --------------------------- | --------------------------- | ------------------------- | ---------------- | --------- | ------------------ |
| `measuresOnline`            | `Microbioreactor`           | `ProcessParameter`        | SRC-001, SRC-002 | Explícita | Sí                 |
| `supportsPHControl`         | `Microbioreactor`           | `pH`                      | SRC-001, SRC-003 | Explícita | Sí                 |
| `usesOnlineSignal`          | `PHControl`                 | `OnlineSignal`            | SRC-003          | Explícita | Sí                 |
| `supportsContinuousFeeding` | `MicrofluidicPlate`         | `ContinuousFeeding`       | SRC-003          | Explícita | Sí                 |
| `feedsSolution`             | `ContinuousFeeding`         | `Solution`                | SRC-003          | Explícita | Sí                 |
| `hasCultivationVessel`      | `BenchtopBioreactor`        | `CultivationVessel`       | SRC-005          | Inferida  | Sí                 |
| `hasWorkingVolume`          | `CultivationVessel`         | `WorkingVolume`           | SRC-004, SRC-005 | Explícita | No                 |
| `guidesPlanningOf`          | `OntologyRequirement`       | `OntologyDevelopmentPlan` | SRC-006          | Inferida  | Sí                 |
| `determinesRelevanceOf`     | `CompetencyQuestion`        | `OntologyContent`         | SRC-007          | Inferida  | Sí                 |
| `hasModule`                 | `Ontology`                  | `OntologyModule`          | SRC-009          | Inferida  | Sí                 |
| `definesBoundaryFor`        | `OntologyModule`            | `DomainBoundary`          | SRC-009          | Inferida  | Sí                 |
| `isCounterpartOf`           | `DigitalArtifact`           | `DigitalArtifact`         | SRC-008          | Explícita | Sí                 |
| `isAssociatedWith`          | `DataInteroperabilityIssue` | `ComputerizedSystem`      | SRC-010          | Inferida  | Sí                 |

# 6) Triadas RDF candidatas

```turtle
:BioLectorXT rdf:type :Microbioreactor .

:BioLectorXT :measuresOnline :Biomass .
:BioLectorXT :measuresOnline :Fluorescence .
:BioLectorXT :measuresOnline :pH .
:BioLectorXT :measuresOnline :DO .

:BioLectorXT :supportsPHControl :pH .
:BioLectorXT :supportsFeeding :ContinuousFeeding .

:PHControl :usesOnlineSignal :OnlineSignal .

:MicrofluidicPlate :supportsContinuousFeeding :ContinuousFeeding .
:ContinuousFeeding :feedsSolution :Solution1 .
:ContinuousFeeding :feedsSolution :Solution2 .

:UnivesselGlass rdf:type :CultivationVessel .
:UnivesselGlass :hasWorkingVolume :Volume1L .
:UnivesselGlass :hasWorkingVolume :Volume2L .
:UnivesselGlass :hasWorkingVolume :Volume5L .
:UnivesselGlass :hasWorkingVolume :Volume10L .

:UnivesselGlass :isCultivationVesselFor :BiostatBenchtopBioreactor .

:CompetencyQuestion :determinesRelevanceOf :OntologyContent .

:OntologyRequirement :guidesPlanningOf :OntologyDevelopmentPlan .

:Ontology :hasModule :OntologyModule .
:OntologyModule :definesBoundaryFor :DomainBoundary .

:DigitalArtifact1 :isCounterpartOf :DigitalArtifact2 .

:DataInteroperabilityIssue :isAssociatedWith :ComputerizedSystem .
```

# 7) Sinónimos documentados

| Término 1                      | Término 2                      | Fuente            | Estado                                                                     |
| ------------------------------ | ------------------------------ | ----------------- | -------------------------------------------------------------------------- |
| `culture vessel`               | `cultivation vessel`           | SRC-004 y SRC-005 | Inferencia razonable de posible equivalencia; requiere validación experta. |
| `BioLector XT`                 | `BioLector XT microbioreactor` | SRC-002           | Explícita.                                                                 |
| `Biostat benchtop bioreactors` | `benchtop bioreactors`         | SRC-005           | Explícita como variante textual.                                           |

No se establecen sinónimos explícitos para `DO`, `pH`, `biomass`, `fluorescence`, `continuous feeding` o `online signal`.

# 8) Vacíos del corpus

1. No existe una lista explícita de conceptos, procesos o dominios que deban excluirse del alcance inicial.
2. No se incluyen preguntas de competencia específicas adicionales a ALC-08.
3. No se definen formalmente las clases, propiedades, restricciones OWL, dominios, rangos ni cardinalidades.
4. No se detallan sensores, actuadores, unidades de medida, límites operativos o métodos de calibración.
5. No se explica el significado de `DO` dentro del corpus suministrado.
6. No se describen fases de proceso, organismos, medios de cultivo, productos biológicos ni condiciones de operación.
7. No se establecen equivalencias completas entre los sistemas BioLector XT y Biostat.
8. No se especifica cuáles modelos de Biostat se relacionan directamente con recipientes de 5 L o 10 L.
9. No se detallan los tipos concretos de artefactos digitales que deben conectarse mediante `isCounterpartOf`.
10. No se define un modelo formal para representar problemas de interoperabilidad entre software y hardware.
11. No se identifican módulos que deban excluirse definitivamente, como purificación, cadena de suministro, regulación, analítica avanzada o gemelos digitales.

# 9) Estado final

**Parcialmente soportado.**

El corpus soporta la necesidad de delimitar la ontología mediante preguntas de competencia, priorización de requisitos y modularización. También soporta un núcleo técnico relacionado con sistemas de cultivo, recipientes, volumen, medición en línea, control de pH y alimentación.

Sin embargo, el corpus no establece una lista explícita de conceptos que deban quedar fuera del alcance inicial. Cualquier exclusión concreta requiere preguntas de competencia adicionales, decisión metodológica documentada y validación experta.
