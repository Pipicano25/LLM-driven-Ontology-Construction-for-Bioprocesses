## 1. Identificación de la pregunta

- **ID:** ALC-04
- **Nivel metodológico:** Arquitectura conceptual y extracción de evidencia técnica
- **Tema:** Componentes funcionales comunes para una ontología multiescala de biorreactores
- **Pregunta:** ¿Qué componentes comunes permiten describir estos tres biorreactores en una misma ontología?

**Precisión metodológica:** “Sartorius 5 L” y “Sartorius 10 L” no identifican por sí solos un modelo único. Sartorius documenta configuraciones Biostat B con recipientes Univessel Glass de 5 L y 10 L, pero también existen otros productos Sartorius con esos volúmenes. Por ello, la referencia a Biostat B se usa como una hipótesis de trabajo verificable, no como identificación definitiva del equipo del laboratorio. ([Sartorius][1])

---

## 2. Propósito de la pregunta

La pregunta busca identificar una capa común de representación ontológica que permita describir un microbioreactor BioLector XT y dos configuraciones Sartorius de mayor volumen sin asumir que poseen componentes físicos idénticos.

La contribución esperada es una estructura funcional común basada en: unidad de cultivo, volumen, medición, sensores, control, mezcla, transferencia de gas, control térmico y adición de líquidos. Las diferencias entre equipos deben expresarse mediante especializaciones físicas, por ejemplo, agitación orbital frente a agitación mecánica o optodos frente a sensores amperométricos. ([Beckman Coulter][2])

---

## 3. Plan de búsqueda documental

### Información técnica requerida

- Tipo de unidad de cultivo y recipiente.
- Volumen nominal, volumen de trabajo o volumen de llenado.
- Variables monitorizadas y controladas.
- Sensores y principios de medición.
- Sistemas de mezcla, aireación y transferencia de gas.
- Sistemas de temperatura, alimentación y corrección de pH.
- Controladores, software, datos y señales externas.
- Dependencias de configuración, accesorios y módulos opcionales.

### Tipos de documentos necesarios

- Fichas técnicas oficiales.
- Manuales de operación e instrucciones de uso.
- Folletos técnicos de fabricante.
- SOPs locales de instalación y operación.
- Registros de configuración del equipo.
- Artículos revisados por pares sobre escalamiento BioLector–biorreactor agitado.

### Repositorios y sitios sugeridos

- Sitios oficiales de Beckman Coulter Life Sciences.
- Sitios oficiales de Sartorius.
- PubMed, Scopus, Web of Science, Google Scholar.
- Repositorios institucionales de universidades.
- Sistema documental interno del laboratorio.

### Términos y ecuaciones de búsqueda sugeridas

- `"BioLector XT" AND ("technical data" OR "user manual" OR "microfluidic")`
- `"BioLector XT" AND ("pH optode" OR "dissolved oxygen" OR "gassing")`
- `"Biostat B" AND ("5 L" OR "10 L") AND (sensor OR controller OR aeration)`
- `"Univessel Glass" AND ("5 L" OR "10 L")`
- `(microbioreactor OR bioreactor) AND ontology AND sensor AND actuator`
- `(BioLector OR microbioreactor) AND scale-up AND stirred tank`
- `"biorreactor" AND ontología AND sensor AND actuador`
- `"BioLector XT" AND escalamiento AND biorreactor agitado`

### Criterios aplicados

Se priorizaron documentos oficiales de fabricante con componentes localizables. Se excluyeron productos Sartorius distintos cuando podían introducir ambigüedad respecto al modelo de 5 L y 10 L realmente disponible en el laboratorio.

---

## 4. Documentos candidatos encontrados

| ID documento | Título                                                                |                Entidad autora |                          Año | Tipo de fuente             | URL/DOI verificable                   | Relación con la pregunta                                                                                         | Decisión preliminar |
| ------------ | --------------------------------------------------------------------- | ----------------------------: | ---------------------------: | -------------------------- | ------------------------------------- | ---------------------------------------------------------------------------------------------------------------- | ------------------- |
| DOC-ALC04-01 | BioLector XT Technical Data Sheet                                     | Beckman Coulter Life Sciences | n.d.; página técnica vigente | Ficha técnica oficial      | Fuente oficial ([Beckman Coulter][2]) | Especifica temperatura, agitación, optodos de pH y DO, gasificación, microfluídica y placas de cultivo.          | Include             |
| DOC-ALC04-02 | Using the BioLector XT Microbioreactor Gassing Lid                    | Beckman Coulter Life Sciences |                         n.d. | Nota técnica oficial       | Fuente oficial ([Beckman Coulter][3]) | Describe placas MTP, gasificación directa, alimentación y muestreo mediante configuración microfluídica.         | Uncertain           |
| DOC-ALC04-03 | Biostat B: The Multi-Talented Bioreactor for Research and Development |      Sartorius Stedim Biotech |                         2021 | Folleto técnico oficial    | Fuente oficial ([Sartorius][4])       | Documenta recipientes de 5 L y 10 L, control de temperatura, pH, DO, velocidad de agitación, bombas y aireación. | Include             |
| DOC-ALC04-04 | Biostat B – Benchtop Bioreactor Controller                            |                     Sartorius |                         n.d. | Página oficial de producto | Fuente oficial ([Sartorius][1])       | Confirma Biostat B como controlador para sistemas agitados y recipientes de 5 L y 10 L.                          | Uncertain           |
| DOC-ALC04-05 | Biostat B-DCU Brochure                                                |                     Sartorius |                         n.d. | Folleto técnico oficial    | Fuente oficial ([Sartorius][5])       | Contiene capacidades de 5 L y 10 L, pero corresponde a una variante B-DCU no confirmada como equipo objetivo.    | Exclude             |
| DOC-ALC04-06 | Biostat Cplus                                                         |                     Sartorius |                         n.d. | Página oficial de producto | Fuente oficial ([Sartorius][6])       | Incluye capacidades de 5 L y 10 L, pero corresponde a un sistema discontinuado y distinto de Biostat B.          | Exclude             |

---

## 5. Evaluación de documentos candidatos

| ID documento | Relevancia | Autoridad | Trazabilidad | Cobertura de la pregunta | Evidencia localizable | Justificación                                                                                                                                                                    |
| ------------ | ---------- | --------- | ------------ | ------------------------ | --------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| DOC-ALC04-01 | Alta       | Alta      | Alta         | Alta                     | Alta                  | Expone variables operativas, optodos, gasificación, agitación, placas y funciones microfluídicas del BioLector XT. ([Beckman Coulter][2])                                        |
| DOC-ALC04-02 | Alta       | Alta      | Alta         | Media                    | Alta                  | Aporta detalles funcionales de gasificación y configuraciones de cultivo, pero no muestra año editorial visible. ([Beckman Coulter][3])                                          |
| DOC-ALC04-03 | Alta       | Alta      | Alta         | Alta                     | Alta                  | Incluye configuraciones Biostat B de 5 L y 10 L, controladores, sensores, bombas, aireación y elementos del recipiente. ([Sartorius][4])                                         |
| DOC-ALC04-04 | Alta       | Alta      | Media        | Media                    | Alta                  | Confirma que Biostat B admite recipientes agitados y Univessel Glass de 5 L y 10 L, pero no sustituye la evidencia de configuración específica del laboratorio. ([Sartorius][1]) |

---

## 6. Corpus documental seleccionado

| ID documento | Documento seleccionado                                                | Pregunta asociada | Fragmentos o páginas relevantes                                                                                      | Estado       |
| ------------ | --------------------------------------------------------------------- | ----------------- | -------------------------------------------------------------------------------------------------------------------- | ------------ |
| DOC-ALC04-01 | BioLector XT Technical Data Sheet                                     | ALC-04            | Secciones “Cultivation conditions”, “Microfluidic features” y “Microtiter plates”.                                   | Seleccionado |
| DOC-ALC04-03 | Biostat B: The Multi-Talented Bioreactor for Research and Development | ALC-04            | Secciones “Univessel Glass”, “Configurable Flexibility” y “Basic Configurations for Univessel Glass”; PDF pp. 21–22. | Seleccionado |

El corpus es suficiente para proponer una arquitectura funcional preliminar, pero no para confirmar que los equipos Sartorius concretos del laboratorio correspondan exactamente a Biostat B con Univessel Glass.

---

## 7. Respuesta basada en evidencia

### Evidencia explícita

El BioLector XT documenta condiciones de cultivo que incluyen temperatura, velocidad de agitación orbital, opciones de atmósfera gaseosa, optodos de pH y oxígeno disuelto, y funciones microfluídicas para control de pH y alimentación. También utiliza placas de microtitulación con múltiples pozos de cultivo. ([Beckman Coulter][2])

La documentación Biostat B describe recipientes Univessel Glass de 5 L y 10 L y configuraciones que controlan temperatura, pH, oxígeno disuelto y velocidad de agitación. Además, documenta módulos de aireación, controladores de caudal, bombas de corrección de pH, sensores de temperatura, pH y DO, agitadores y spargers. ([Sartorius][4])

### Inferencia razonable basada en evidencia

Los tres sistemas pueden describirse en una misma ontología si se modelan como realizaciones de una clase funcional común, `BioreactorSystem`, y no como dispositivos físicamente equivalentes.

Los componentes funcionales comunes candidatos son:

| Núcleo funcional común    | BioLector XT                                                       | Sartorius 5 L / 10 L de referencia                   | Representación ontológica candidata |
| ------------------------- | ------------------------------------------------------------------ | ---------------------------------------------------- | ----------------------------------- |
| Unidad de cultivo         | Pozos de placas MTP.                                               | Recipiente Univessel Glass.                          | `CultivationUnit`                   |
| Especificación de volumen | Volumen de llenado en µL según tipo de placa.                      | Volumen de trabajo en L según recipiente.            | `VolumeSpecification`               |
| Medición de proceso       | Optodos de pH y DO.                                                | Sensores de pH, DO y temperatura.                    | `MeasurementSubsystem`, `Sensor`    |
| Variables observadas      | pH, DO, biomasa, fluorescencia.                                    | Temperatura, pH, DO, velocidad de agitación.         | `ProcessParameter`                  |
| Control de proceso        | Control PI de pH y alimentación microfluídica opcional.            | Control digital de temperatura, pH, DO y agitación.  | `ProcessControlSystem`              |
| Mezcla                    | Agitación orbital.                                                 | Eje, motor e impulsor agitado.                       | `MixingSubsystem`                   |
| Transferencia de gas      | Control de gas en espacio de cabeza y módulos opcionales.          | Aireación, controladores de caudal, gases y sparger. | `GasTransferSubsystem`              |
| Control térmico           | Temperatura definida como condición de cultivo.                    | Módulo de control de temperatura y sensor Pt100.     | `TemperatureControlSubsystem`       |
| Adición de líquidos       | Alimentación y corrección de pH opcionales mediante microfluídica. | Bombas, botellas de corrección y puertos de adición. | `LiquidAdditionSubsystem`           |

La evidencia respalda la equivalencia funcional de estas categorías, pero no una equivalencia física directa entre sus implementaciones. Por ejemplo, un optodo de pH no debe declararse idéntico a una sonda convencional de pH, y la agitación orbital no debe declararse igual a la agitación por impulsor. ([Beckman Coulter][2])

### Información no establecida en el corpus

- Modelo exacto de los sistemas Sartorius de 5 L y 10 L.
- Configuración real de sensores, bombas, gases y accesorios de cada unidad.
- Mecanismos de alarmas, fallas, eventos y calidad de datos.
- Formato de exportación y granularidad de datos de los Sartorius específicos.
- Criterios cuantitativos de equivalencia funcional o escalamiento entre BioLector XT, 5 L y 10 L.

---

## 8. Tabla de afirmaciones y evidencia

| ID evidencia | Afirmación                                                                                                               | Tipo de evidencia | Documento                  | Página/sección                   | Fragmento o resumen fiel                                                                                                                               | Confianza | Validación experta                |
| ------------ | ------------------------------------------------------------------------------------------------------------------------ | ----------------- | -------------------------- | -------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------ | --------- | --------------------------------- |
| E-ALC04-01   | BioLector XT documenta temperatura, agitación, optodos de pH y DO, además de opciones de gasificación.                   | Explícita         | DOC-ALC04-01               | Cultivation conditions           | La ficha técnica especifica temperatura, velocidad de agitación, rangos de O₂ y CO₂, optodos de oxígeno y optodos de pH. ([Beckman Coulter][2])        | Alta      | No                                |
| E-ALC04-02   | BioLector XT puede incluir control de pH y alimentación mediante microfluídica.                                          | Explícita         | DOC-ALC04-01               | Microfluidic features            | Se documenta control PI de pH, alimentación con una o dos líneas y perfiles de alimentación. ([Beckman Coulter][2])                                    | Alta      | Sí, según módulo instalado        |
| E-ALC04-03   | BioLector XT utiliza pozos de placas de microtitulación como unidades de cultivo.                                        | Explícita         | DOC-ALC04-01               | Microtiter plates                | La ficha especifica FlowerPlate, Round Well Plate y Microfluidic Plate con 32 o 48 pozos de cultivo. ([Beckman Coulter][2])                            | Alta      | No                                |
| E-ALC04-04   | Biostat B dispone de recipientes Univessel Glass de 5 L y 10 L.                                                          | Explícita         | DOC-ALC04-03               | Univessel Glass; PDF p. 21       | El documento lista recipientes de 1 L, 2 L, 5 L y 10 L y sus rangos de volumen de trabajo. ([Sartorius][4])                                            | Alta      | Sí, para confirmar equipo real    |
| E-ALC04-05   | Biostat B controla temperatura, pH, DO y velocidad de agitación.                                                         | Explícita         | DOC-ALC04-03               | Basic Configurations; PDF p. 22  | Las configuraciones microbianas y de cultivo celular indican control de temperatura, pH, DO y velocidad de agitación. ([Sartorius][4])                 | Alta      | Sí, según configuración instalada |
| E-ALC04-06   | Biostat B puede incluir sensores de temperatura, pH y DO.                                                                | Explícita         | DOC-ALC04-03               | Basic Configurations; PDF p. 22  | Se indican sensor Pt100, sensor de pH y sensor amperométrico de DO. ([Sartorius][4])                                                                   | Alta      | Sí, para configuración exacta     |
| E-ALC04-07   | Los tres sistemas pueden compartir clases funcionales de cultivo, medición, control, mezcla, gasificación y temperatura. | Inferida          | DOC-ALC04-01; DOC-ALC04-03 | Secciones técnicas seleccionadas | La inferencia se basa en que ambos tipos de sistema documentan funciones equivalentes aunque con componentes físicos distintos. ([Beckman Coulter][2]) | Media     | Sí                                |
| E-ALC04-08   | Alarmas, fallas, eventos y calidad de datos no están suficientemente documentados en el corpus seleccionado.             | No establecida    | Corpus seleccionado        | Revisión de secciones incluidas  | Los documentos revisados no definen una taxonomía operativa de fallas, alarmas o calidad de datos.                                                     | Media     | Sí                                |

---

## 9. Conceptos ontológicos candidatos

| Concepto candidato               | Tipo sugerido     | Definición basada en evidencia                                                     | Fuente asociada                     | Estado                      |
| -------------------------------- | ----------------- | ---------------------------------------------------------------------------------- | ----------------------------------- | --------------------------- |
| `BioreactorSystem`               | Clase             | Sistema técnico que sostiene y regula una operación de cultivo.                    | DOC-ALC04-01; DOC-ALC04-03          | Candidato                   |
| `MicrobioreactorSystem`          | Subclase          | Sistema de cultivo de microescala basado en placas de microtitulación.             | DOC-ALC04-01 ([Beckman Coulter][2]) | Candidato                   |
| `StirredTankBioreactorSystem`    | Subclase          | Sistema de cultivo basado en recipiente agitado, eje, motor e impulsor.            | DOC-ALC04-03 ([Sartorius][4])       | Candidato                   |
| `CultivationUnit`                | Clase             | Unidad física donde ocurre la cultivación, como pozo MTP o recipiente de vidrio.   | DOC-ALC04-01; DOC-ALC04-03          | Candidato                   |
| `MicrotiterPlateCultivationWell` | Subclase          | Pozo individual de placa empleado para cultivo BioLector XT.                       | DOC-ALC04-01 ([Beckman Coulter][2]) | Candidato                   |
| `CultureVessel`                  | Clase             | Recipiente de cultivo de un biorreactor.                                           | DOC-ALC04-03 ([Sartorius][4])       | Candidato                   |
| `VolumeSpecification`            | Concepto auxiliar | Representación de volumen, unidad y rol del volumen: llenado, nominal o trabajo.   | DOC-ALC04-01; DOC-ALC04-03          | Candidato                   |
| `MeasurementSubsystem`           | Clase             | Subsistema que obtiene observaciones del proceso.                                  | DOC-ALC04-01; DOC-ALC04-03          | Candidato                   |
| `pHSensor`                       | Subclase          | Sensor u optodo empleado para observar pH.                                         | DOC-ALC04-01; DOC-ALC04-03          | Candidato                   |
| `DissolvedOxygenSensor`          | Subclase          | Sensor u optodo empleado para observar oxígeno disuelto.                           | DOC-ALC04-01; DOC-ALC04-03          | Candidato                   |
| `ProcessControlSystem`           | Clase             | Subsistema que aplica control a parámetros del cultivo.                            | DOC-ALC04-01; DOC-ALC04-03          | Candidato                   |
| `MixingSubsystem`                | Clase             | Subsistema que mezcla el cultivo por agitación orbital o mecánica.                 | DOC-ALC04-01; DOC-ALC04-03          | Candidato                   |
| `GasTransferSubsystem`           | Clase             | Subsistema que suministra o regula gases asociados al cultivo.                     | DOC-ALC04-01; DOC-ALC04-03          | Candidato                   |
| `TemperatureControlSubsystem`    | Clase             | Subsistema asociado al establecimiento o control de temperatura.                   | DOC-ALC04-01; DOC-ALC04-03          | Candidato                   |
| `LiquidAdditionSubsystem`        | Clase             | Subsistema opcional para alimentación, corrección de pH o adición de líquidos.     | DOC-ALC04-01; DOC-ALC04-03          | Candidato                   |
| `ProcessParameter`               | Clase             | Variable observable o controlable, como pH, DO, temperatura o velocidad de mezcla. | DOC-ALC04-01; DOC-ALC04-03          | Candidato                   |
| `CultivationRun`                 | Clase             | Ejecución temporal de un experimento o cultivo.                                    | DOC-ALC04-01; DOC-ALC04-03          | Requiere validación experta |

---

## 10. Relaciones ontológicas candidatas

| Relación candidata               | Dominio sugerido       | Rango sugerido                | Significado                                                                       | Evidencia asociada                                                                      | Estado                      |
| -------------------------------- | ---------------------- | ----------------------------- | --------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------- | --------------------------- |
| `hasCultivationUnit`             | `BioreactorSystem`     | `CultivationUnit`             | Relaciona un sistema con su unidad de cultivo.                                    | Pozos MTP y recipientes Univessel. ([Beckman Coulter][2])                               | Candidata                   |
| `hasVolumeSpecification`         | `CultivationUnit`      | `VolumeSpecification`         | Asocia una unidad de cultivo con su volumen y unidad.                             | Volúmenes de llenado y trabajo documentados. ([Beckman Coulter][2])                     | Candidata                   |
| `hasMeasurementSubsystem`        | `BioreactorSystem`     | `MeasurementSubsystem`        | Indica que el sistema incluye observación de variables del proceso.               | Optodos y sensores documentados. ([Beckman Coulter][2])                                 | Candidata                   |
| `hasSensor`                      | `MeasurementSubsystem` | `Sensor`                      | Relaciona un subsistema de medición con su sensor.                                | pH, DO y Pt100 en configuraciones Biostat; optodos en BioLector. ([Beckman Coulter][2]) | Candidata                   |
| `observesParameter`              | `Sensor`               | `ProcessParameter`            | Indica la variable observada por un sensor.                                       | Observación de pH y DO. ([Beckman Coulter][2])                                          | Candidata                   |
| `hasProcessControlSystem`        | `BioreactorSystem`     | `ProcessControlSystem`        | Conecta un sistema con su capacidad de control.                                   | Control PI BioLector y controlador digital Biostat. ([Beckman Coulter][2])              | Candidata                   |
| `regulatesParameter`             | `ProcessControlSystem` | `ProcessParameter`            | Expresa una variable regulada por el controlador.                                 | pH, temperatura, DO y mezcla según configuración. ([Beckman Coulter][2])                | Candidata                   |
| `hasMixingSubsystem`             | `BioreactorSystem`     | `MixingSubsystem`             | Expresa la capacidad de mezcla.                                                   | Shaking speed BioLector; stirrer speed Biostat. ([Beckman Coulter][2])                  | Candidata                   |
| `hasGasTransferSubsystem`        | `BioreactorSystem`     | `GasTransferSubsystem`        | Relaciona el sistema con su función de gasificación o aireación.                  | Módulos de gas BioLector; aireación y sparger Biostat. ([Beckman Coulter][2])           | Candidata                   |
| `hasTemperatureControlSubsystem` | `BioreactorSystem`     | `TemperatureControlSubsystem` | Relaciona el sistema con función térmica.                                         | Temperatura BioLector; módulo y Pt100 Biostat. ([Beckman Coulter][2])                   | Candidata                   |
| `mayHaveLiquidAdditionSubsystem` | `BioreactorSystem`     | `LiquidAdditionSubsystem`     | Indica una capacidad dependiente de configuración para alimentación o corrección. | Microfluídica opcional y bombas Biostat. ([Beckman Coulter][2])                         | Candidata                   |
| `hasPhysicalImplementation`      | `FunctionalComponent`  | `EquipmentComponent`          | Vincula una función abstracta con su realización física particular.               | Optodo frente a sonda; agitación orbital frente a impulsor. ([Beckman Coulter][2])      | Requiere validación experta |

---

## 11. Triadas RDF candidatas

| Triada RDF candidata                                                                           | Documento de soporte       | Página o sección                             | Estado                      |
| ---------------------------------------------------------------------------------------------- | -------------------------- | -------------------------------------------- | --------------------------- |
| `BioLectorXT -> rdf:type -> MicrobioreactorSystem`                                             | DOC-ALC04-01               | Título y Microtiter plates                   | soportada                   |
| `Sartorius_5L_BioreactorConfiguration -> rdf:type -> BioreactorSystem`                         | DOC-ALC04-03               | Univessel Glass                              | requiere validación experta |
| `Sartorius_10L_BioreactorConfiguration -> rdf:type -> BioreactorSystem`                        | DOC-ALC04-03               | Univessel Glass                              | requiere validación experta |
| `BioreactorSystem -> hasCultivationUnit -> CultivationUnit`                                    | DOC-ALC04-01; DOC-ALC04-03 | Microtiter plates; Univessel Glass           | parcialmente soportada      |
| `CultivationUnit -> hasVolumeSpecification -> VolumeSpecification`                             | DOC-ALC04-01; DOC-ALC04-03 | Microtiter plates; PDF p. 21                 | parcialmente soportada      |
| `BioreactorSystem -> hasMeasurementSubsystem -> MeasurementSubsystem`                          | DOC-ALC04-01; DOC-ALC04-03 | Cultivation conditions; Basic Configurations | parcialmente soportada      |
| `MeasurementSubsystem -> hasSensor -> pHSensor`                                                | DOC-ALC04-01; DOC-ALC04-03 | pH optodes; PDF p. 22                        | soportada                   |
| `MeasurementSubsystem -> hasSensor -> DissolvedOxygenSensor`                                   | DOC-ALC04-01; DOC-ALC04-03 | Oxygen optodes; PDF p. 22                    | soportada                   |
| `Sensor -> observesParameter -> pH`                                                            | DOC-ALC04-01; DOC-ALC04-03 | Cultivation conditions; PDF p. 22            | soportada                   |
| `Sensor -> observesParameter -> DissolvedOxygen`                                               | DOC-ALC04-01; DOC-ALC04-03 | Cultivation conditions; PDF p. 22            | soportada                   |
| `BioreactorSystem -> hasProcessControlSystem -> ProcessControlSystem`                          | DOC-ALC04-01; DOC-ALC04-03 | Microfluidic features; Basic Configurations  | parcialmente soportada      |
| `ProcessControlSystem -> mayRegulate -> pH`                                                    | DOC-ALC04-01; DOC-ALC04-03 | Triggered pH control; Basic Configurations   | soportada                   |
| `BioreactorSystem -> hasMixingSubsystem -> MixingSubsystem`                                    | DOC-ALC04-01; DOC-ALC04-03 | Shaking speed; stirrer speed                 | soportada                   |
| `BioreactorSystem -> hasGasTransferSubsystem -> GasTransferSubsystem`                          | DOC-ALC04-01; DOC-ALC04-03 | Gas modules; aeration module and sparger     | soportada                   |
| `BioreactorSystem -> hasTemperatureControlSubsystem -> TemperatureControlSubsystem`            | DOC-ALC04-01; DOC-ALC04-03 | Temperature; temperature control module      | parcialmente soportada      |
| `BioreactorSystem -> mayHaveLiquidAdditionSubsystem -> LiquidAdditionSubsystem`                | DOC-ALC04-01; DOC-ALC04-03 | Feeding options; integrated pumps            | soportada                   |
| `BioLectorXT -> hasCultivationUnit -> MicrotiterPlateCultivationWell`                          | DOC-ALC04-01               | Microtiter plates                            | soportada                   |
| `BioLectorXT -> hasMixingSubsystem -> OrbitalShakingSubsystem`                                 | DOC-ALC04-01               | Shaking speed                                | soportada                   |
| `BioLectorXT -> hasSensor -> pHOptode`                                                         | DOC-ALC04-01               | pH optodes                                   | soportada                   |
| `BioLectorXT -> hasSensor -> DissolvedOxygenOptode`                                            | DOC-ALC04-01               | Oxygen optodes                               | soportada                   |
| `Sartorius_5L_BioreactorConfiguration -> hasCultivationUnit -> UnivesselGlass5L`               | DOC-ALC04-03               | Univessel Glass                              | requiere validación experta |
| `Sartorius_10L_BioreactorConfiguration -> hasCultivationUnit -> UnivesselGlass10L`             | DOC-ALC04-03               | Univessel Glass                              | requiere validación experta |
| `Sartorius_5L_BioreactorConfiguration -> hasMixingSubsystem -> StirredTankAgitationSubsystem`  | DOC-ALC04-03               | Basic Configurations                         | requiere validación experta |
| `Sartorius_10L_BioreactorConfiguration -> hasMixingSubsystem -> StirredTankAgitationSubsystem` | DOC-ALC04-03               | Basic Configurations                         | requiere validación experta |

---

## 12. Sinónimos y variantes terminológicas

| Término principal         | Sinónimos o variantes documentadas           | Idioma | Documento de soporte                              |
| ------------------------- | -------------------------------------------- | ------ | ------------------------------------------------- |
| `DissolvedOxygen`         | dissolved oxygen; DO                         | Inglés | DOC-ALC04-01; DOC-ALC04-03 ([Beckman Coulter][2]) |
| `MicrotiterPlate`         | microtiter plate; MTP                        | Inglés | DOC-ALC04-01 ([Beckman Coulter][2])               |
| `CultureVessel`           | culture vessel; cultivation chamber          | Inglés | DOC-ALC04-03 ([Sartorius][4])                     |
| `GasTransferSubsystem`    | gassing; aeration                            | Inglés | DOC-ALC04-01; DOC-ALC04-03 ([Beckman Coulter][2]) |
| `LiquidAdditionSubsystem` | feeding; addition; correction agent addition | Inglés | DOC-ALC04-01; DOC-ALC04-03 ([Beckman Coulter][2]) |

---

## 13. Vacíos, riesgos y decisiones pendientes

- Confirmar el modelo exacto, número de serie y configuración de los Sartorius de 5 L y 10 L.
- No equiparar volumen de llenado BioLector XT con volumen de trabajo Sartorius.
- No declarar equivalencia física entre `pHOptode` y `pHSensor`.
- No declarar equivalencia física entre `OrbitalShakingSubsystem` y `StirredTankAgitationSubsystem`.
- Representar `LiquidAdditionSubsystem` como opcional o dependiente de configuración.
- Distinguir gasificación de espacio de cabeza en BioLector XT de aireación por sparger en Biostat B.
- Obtener manuales de instalación, listas de accesorios, calibraciones y SOPs locales.
- Verificar cómo se registran alarmas, fallas, decisiones, eventos y calidad de datos.
- Validar con expertos del proceso si temperatura, pH, DO y mezcla son las variables mínimas comunes para todos los protocolos experimentales.

---

## 14. Registro metodológico para el documento de investigación

La pregunta ALC-04 examinó qué componentes permiten representar en una misma ontología un microbioreactor BioLector XT y sistemas Sartorius de 5 L y 10 L. Se aplicó una búsqueda documental dirigida a fichas técnicas, folletos de fabricante e instrucciones de uso con énfasis en unidad de cultivo, volumen, sensores, variables operativas, control, mezcla, transferencia de gas y adición de líquidos. Se seleccionaron como fuentes principales la ficha técnica oficial del BioLector XT y la documentación técnica del Biostat B, debido a que contienen evidencia localizable sobre recipientes de cultivo, parámetros monitorizados, actuadores, módulos de control y configuraciones de operación. A partir de esta evidencia se identificaron conceptos ontológicos preliminares tales como BioreactorSystem, CultivationUnit, MeasurementSubsystem, ProcessControlSystem, MixingSubsystem, GasTransferSubsystem y TemperatureControlSubsystem. Asimismo, se propusieron relaciones candidatas para vincular sistemas, sensores, parámetros, unidades de cultivo y mecanismos de control. La principal limitación corresponde a la falta de identificación verificable de los modelos específicos Sartorius de 5 L y 10 L disponibles en el laboratorio, por lo cual las correspondencias con Biostat B deben ser validadas mediante manuales locales, registros de configuración y revisión experta.

El párrafo se fundamenta en la ficha técnica BioLector XT y en el folleto técnico Biostat B. ([Beckman Coulter][2])

---

## 15. Estado final

- **Nivel de confianza general:** Medio.
- **Estado de la respuesta:** Parcialmente soportada.
- **Estado del corpus:** Parcial.
- **Próxima acción recomendada:** Obtener los manuales, fotos de placa de identificación o registros de configuración de los Sartorius 5 L y 10 L para reemplazar las instancias provisionales por modelos y componentes confirmados.

[1]: https://www.sartorius.com/en/products/fermentation-bioreactors/benchtop-bioreactors/biostat-b " Biostat® B - Benchtop Bioreactor Controller | Sartorius"
[2]: https://www.beckman.com/resources/reading-material/product-instructions/biolector-xt-technical-data-sheet "BioLector XT Technical Data Sheet"
[3]: https://www.beckman.com/resources/reading-material/product-instructions/using-the-biolector-xt-microbioreactor-gassing-lid "Using the BioLector XT Microbioreactor Gassing Lid"
[4]: https://www.sartorius.com/download/34576/broch-biostat-b-sbi1513-e-1--data.pdf "Biostat® B Multi-talented bioreactor"
[5]: https://www.sartorius.com/download/12080/broch-biostat-b-dcu-sbi1555-e-data.pdf "Biostat B-DCU, Brochure"
[6]: https://www.sartorius.com/en/products/fermentation-bioreactors/stainless-steel-bioreactors/biostat-cplus?utm_source=chatgpt.com "Biostat® Cplus - Stainless Steel Fermenter / Bioreactor - Sartorius"
