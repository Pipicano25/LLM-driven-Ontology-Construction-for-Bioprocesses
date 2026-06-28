## 1. Identificación de la pregunta

- **ID:** ALC-05
- **Nivel metodológico:** Conceptual–ontológico, con evidencia técnica de equipos y estándares semánticos.
- **Tema:** Separación semántica entre activos físicos, proceso biológico, control, variables y datos.
- **Pregunta:** ¿Cómo se separan ontológicamente el equipo físico, el proceso biológico, el sistema de control, las variables medidas y los datos generados?

**Nota de alcance:** “Sartorius 5 L” y “Sartorius 10 L” describen capacidades o configuraciones de recipiente, pero no identifican por sí solos un modelo, número de serie ni configuración instrumental única. La instanciación definitiva requiere confirmar el equipo instalado.

---

## 2. Propósito de la pregunta

La pregunta busca evitar que una misma entidad ontológica represente simultáneamente el biorreactor físico, el cultivo, la lógica de control, una variable como pH y el dato numérico generado. Esta separación permite representar trazabilidad desde el activo físico y los sensores hasta observaciones, resultados, archivos de datos, alarmas y decisiones.

Para el corpus, la pregunta requiere combinar documentación técnica de BioLector XT y Sartorius con estándares semánticos que distingan sistemas, sensores, actuadores, observaciones, propiedades, actividades y entidades de datos.

---

## 3. Plan de búsqueda documental

### Información técnica requerida

- Arquitectura física de BioLector XT, Biostat B y recipientes Univessel Glass de 5 L y 10 L.
- Sensores, actuadores, módulos de control, variables y modos de operación.
- Evidencia sobre adquisición, almacenamiento y visualización de datos.
- Definiciones formales para `System`, `Sensor`, `Actuator`, `Observation`, `Property`, `FeatureOfInterest`, `Activity`, `Entity` y procedencia.

### Tipos de documentos necesarios

- Manuales, fichas técnicas y brochures oficiales de fabricante.
- Páginas oficiales de producto vigentes.
- Estándares W3C para sensores, observaciones y procedencia.
- Posteriormente: SOPs locales, configuraciones de hardware, exportaciones de datos, recetas de cultivo y registros de calibración.

### Repositorios y sitios sugeridos

- Beckman Coulter Life Sciences.
- Sartorius.
- W3C.
- Crossref, PubMed, Scopus, Web of Science y Google Scholar para artículos complementarios.
- Repositorio documental interno del laboratorio.

### Términos de búsqueda

**Español**

- “separación ontológica biorreactor proceso control datos”
- “sensor actuador observación variable proceso biológico ontología”
- “BioLector XT sensores pH oxígeno disuelto datos”
- “Sartorius Biostat B 5 L 10 L control sensores”

**English**

- “bioreactor ontology equipment process control observation data”
- “BioLector XT technical data sheet pH dissolved oxygen”
- “Biostat B control tower sensor process data”
- “SOSA observation sensor actuator feature of interest”
- “PROV-O measurement provenance data generation”

### Ecuaciones de búsqueda sugeridas

```text
("BioLector XT" AND ("pH" OR "dissolved oxygen" OR biomass) AND ("technical data" OR datasheet))

("Biostat B" AND ("5 L" OR "10 L") AND (sensor OR control OR "process data"))

("Semantic Sensor Network Ontology" OR SOSA) AND
(observation OR sensor OR actuator OR property)

("PROV-O" OR "PROV Ontology") AND
(entity OR activity OR "wasGeneratedBy" OR "wasDerivedFrom")
```

### Criterios aplicables

Se priorizaron fuentes oficiales de fabricante y estándares W3C. Se excluyeron o dejaron como inciertas fuentes redundantes, genéricas o no específicas para los sistemas evaluados.

---

## 4. Documentos candidatos encontrados

| ID documento | Título                                                                | Entidad autora                |                Año | Tipo de fuente             | URL/DOI verificable                                                                                                                         | Relación con la pregunta                                                                                       | Decisión preliminar |
| ------------ | --------------------------------------------------------------------- | ----------------------------- | -----------------: | -------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------- | ------------------- |
| D01          | BioLector XT Microbioreactor                                          | Beckman Coulter Life Sciences |        No indicado | Página oficial de producto | [URL oficial](https://www.beckman.com/microbioreactor/biolector-xt) ([beckman.com][1])                                                      | Describe monitorización en tiempo real, sensores ópticos y variables de cultivo.                               | Include             |
| D02          | BioLector XT Technical Data Sheet                                     | Beckman Coulter Life Sciences |        No indicado | Ficha técnica oficial      | [URL oficial](https://www.beckman.com/resources/reading-material/product-instructions/biolector-xt-technical-data-sheet) ([beckman.com][2]) | Aporta evidencia de pH, DO, control de pH, alimentación y módulos de control.                                  | Include             |
| D03          | Biostat B: The Multi-Talented Bioreactor for Research and Development | Sartorius                     |               2021 | Brochure técnico oficial   | [PDF oficial](https://www.sartorius.com/download/34576/broch-biostat-b-sbi1513-e-1--data.pdf) ([Sartorius][3])                              | Describe recipientes de 5 L y 10 L, control, sensores, automatización y datos de proceso.                      | Include             |
| D04          | Biostat B – Benchtop Bioreactor Controller                            | Sartorius                     |        No indicado | Página oficial de producto | [URL oficial](https://www.sartorius.com/en/products/fermentation-bioreactors/benchtop-bioreactors/biostat-b) ([Sartorius][4])               | Confirma información general ya cubierta con mayor detalle en D03.                                             | Exclude             |
| D05          | Univessel Glass – Autoclavable Cultivation Vessel                     | Sartorius                     |        No indicado | Página oficial de producto | [URL oficial](https://www.sartorius.com/en/products/fermentation-bioreactors/benchtop-bioreactors/univessel-glass) ([Sartorius][5])         | Relaciona los recipientes de cultivo con configuraciones de 5 L y 10 L.                                        | Include             |
| D06          | Semantic Sensor Network Ontology – 2023 Edition                       | W3C                           | 2025, edición 2023 | Estándar semántico         | [URL oficial](https://www.w3.org/TR/vocab-ssn-2023/) ([W3C][6])                                                                             | Proporciona clases y propiedades para sistemas, sensores, actuadores, observaciones, propiedades y resultados. | Include             |
| D07          | PROV-O: The PROV Ontology                                             | W3C Provenance Working Group  |               2013 | Recomendación W3C          | [URL oficial](https://www.w3.org/TR/prov-o/) ([W3C][7])                                                                                     | Permite representar actividades, entidades, generación y derivación de datos.                                  | Include             |
| D08          | Single-Use Bioreactors                                                | Sartorius                     |        No indicado | Página oficial de producto | [URL oficial](https://www.sartorius.com/en/products/fermentation-bioreactors/single-use-bioreactors) ([Sartorius][8])                       | Distingue recipiente y unidad de control, pero es genérico y no específico para los recipientes de interés.    | Uncertain           |

---

## 5. Evaluación de documentos candidatos

| ID documento | Relevancia | Autoridad | Trazabilidad | Cobertura de la pregunta | Evidencia localizable | Justificación                                                                                                                               |
| ------------ | ---------- | --------- | ------------ | ------------------------ | --------------------- | ------------------------------------------------------------------------------------------------------------------------------------------- |
| D01          | Alta       | Alta      | Alta         | Media                    | Alta                  | Identifica BioLector XT como microbiorreactor con monitorización en tiempo real de biomasa, fluorescencia, pH y DO. ([beckman.com][1])      |
| D02          | Alta       | Alta      | Alta         | Alta                     | Alta                  | Distingue variables, sensores ópticos, control de pH, alimentación y módulos de control. ([beckman.com][2])                                 |
| D03          | Alta       | Alta      | Alta         | Alta                     | Alta                  | Proporciona evidencia sobre recipientes de 5 L y 10 L, control, sensores, modos de proceso y captura de datos. ([Sartorius][3])             |
| D05          | Alta       | Alta      | Alta         | Media                    | Media                 | Complementa la identificación de recipientes Univessel Glass de 5 L y 10 L. ([Sartorius][5])                                                |
| D06          | Alta       | Alta      | Alta         | Alta                     | Alta                  | Define formalmente la separación entre sistemas, sensores, actuadores, observaciones, propiedades y entidades observadas. ([W3C][6])        |
| D07          | Alta       | Alta      | Alta         | Alta                     | Alta                  | Define `prov:Entity`, `prov:Activity`, generación, uso y derivación de datos. ([W3C][7])                                                    |
| D08          | Media      | Alta      | Alta         | Baja                     | Media                 | Útil como respaldo arquitectónico general, pero no permite inferir la configuración de los sistemas específicos evaluados. ([Sartorius][8]) |

---

## 6. Corpus documental seleccionado

| ID documento | Documento seleccionado                                                | Pregunta asociada | Fragmentos o páginas relevantes                                                                                                     | Estado       |
| ------------ | --------------------------------------------------------------------- | ----------------- | ----------------------------------------------------------------------------------------------------------------------------------- | ------------ |
| D01          | BioLector XT Microbioreactor                                          | ALC-05            | Descripción funcional: biomasa, fluorescencia, pH, DO, sensores ópticos y control microfluídico. ([beckman.com][1])                 | Seleccionado |
| D02          | BioLector XT Technical Data Sheet                                     | ALC-05            | Secciones de condiciones de cultivo, sensores de pH/DO, control de pH, alimentación y módulos de control. ([beckman.com][2])        | Seleccionado |
| D03          | Biostat B: The Multi-Talented Bioreactor for Research and Development | ALC-05            | Págs. 1–2, 5–6, 10–11, 17, 20–21: recipientes, sensores, control, modos de proceso y captura de datos. ([Sartorius][3])             | Seleccionado |
| D05          | Univessel Glass – Autoclavable Cultivation Vessel                     | ALC-05            | Sección de recipientes Univessel Glass de 2 L, 5 L y 10 L. ([Sartorius][5])                                                         | Seleccionado |
| D06          | Semantic Sensor Network Ontology – 2023 Edition                       | ALC-05            | Clases y propiedades SOSA/SSN para sistemas, sensores, actuadores, observaciones, propiedades, resultados y subsistemas. ([W3C][6]) | Seleccionado |
| D07          | PROV-O: The PROV Ontology                                             | ALC-05            | Clases `prov:Entity`, `prov:Activity` y relaciones `prov:wasGeneratedBy`, `prov:used`, `prov:wasDerivedFrom`. ([W3C][7])            | Seleccionado |

El corpus es suficiente para una separación conceptual preliminar, pero no para afirmar la configuración física exacta de los sistemas Sartorius instalados.

---

## 7. Respuesta basada en evidencia

La separación ontológica recomendada es de cinco capas conectadas, no de una única clase genérica llamada `Bioreactor`.

| Capa               | Qué representa                                                                                | Representación candidata                                                  | No debe confundirse con                                   |
| ------------------ | --------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------- | --------------------------------------------------------- |
| Equipo físico      | Activos, recipientes, sensores, bombas, agitadores, módulos de gas y controlador físico.      | `BioreactorAsset`, `CultureVessel`, `Sensor`, `Actuator`, `ControlTower`. | Cultivo, observación, variable medida o archivo de datos. |
| Proceso biológico  | Ejecución temporal del cultivo, fases, alimentación, batch, fed-batch, continuo o perfusión.  | `CultivationRun`, `ProcessPhase`, `Culture`.                              | El recipiente físico ni la unidad de control.             |
| Sistema de control | Lógica e infraestructura que aplica acciones para alcanzar condiciones objetivo.              | `ControlSystem`, `ControlProcedure`, `ControlSetpoint`, `sosa:Actuation`. | El sensor, la variable o el dato resultante.              |
| Variables medidas  | Propiedades observables o controlables: pH, DO, biomasa, temperatura, espuma, turbidez.       | Instancias de `sosa:Property`, agrupadas como `ProcessVariable`.          | La observación concreta o su valor numérico.              |
| Datos generados    | Observaciones, resultados, series temporales, archivos exportados, alarmas y datos derivados. | `sosa:Observation`, `MeasurementResult`, `ProcessDataSet`, `prov:Entity`. | El proceso físico o el instrumento que los produjo.       |

### Evidencia explícita

BioLector XT permite monitorización en tiempo real de biomasa, fluorescencia, pH y oxígeno disuelto mediante sensores ópticos; además, sus especificaciones describen control de pH y opciones de alimentación. ([beckman.com][1])

El brochure de Biostat B distingue recipientes de cultivo, torre de control, módulos de aireación, bombas, temperatura, sensores y mecanismos de control automático de pH y DO; también documenta captura, almacenamiento y visualización de datos de proceso. ([Sartorius][3])

SOSA/SSN separa formalmente `sosa:System`, `sosa:Sensor`, `sosa:Actuator`, `sosa:Observation`, `sosa:Property`, `sosa:FeatureOfInterest` y relaciones como `sosa:observedProperty`, `sosa:madeBySensor` y `sosa:hasResult`. ([W3C][6])

PROV-O distingue entidades y actividades, y permite vincular datos con las actividades que los generaron o de las que se derivaron. ([W3C][7])

### Inferencia razonable basada en evidencia

1. Un cultivo debe modelarse como entidad biológica distinta del recipiente donde ocurre.
2. Una variable como `pH` debe modelarse como propiedad, no como sensor ni como observación.
3. Una medición de pH debe modelarse como una `sosa:Observation` vinculada a un sensor, una propiedad, un cultivo o sistema objetivo, un tiempo y un resultado.
4. Un archivo CSV, serie temporal o exportación debe modelarse como entidad de datos con procedencia, no como la observación misma.
5. La torre de control, el controlador BioLector o módulos equivalentes pueden modelarse como sistemas de control, mientras que bombas, válvulas y controladores de flujo pueden modelarse como actuadores o subsistemas.

### Información no establecida en el corpus

- Modelo exacto, serie, firmware y configuración de cada sistema Sartorius de 5 L y 10 L.
- Sensores realmente instalados en cada unidad.
- Configuración local de alarmas, límites, recetas, setpoints y controladores PI/PID.
- Formato real de archivos exportados, frecuencia de muestreo, metadatos y reglas de calidad de datos.
- Correspondencia exacta entre cada señal de software y su sensor o canal físico.

---

## 8. Tabla de afirmaciones y evidencia

| ID evidencia | Afirmación                                                                                             | Tipo de evidencia | Documento       | Página/sección                         | Fragmento o resumen fiel                                                                                                     | Confianza | Validación experta                                        |
| ------------ | ------------------------------------------------------------------------------------------------------ | ----------------- | --------------- | -------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------- | --------- | --------------------------------------------------------- |
| E01          | BioLector XT monitoriza biomasa, fluorescencia, pH y DO en tiempo real.                                | Explícita         | D01             | Descripción de producto                | El fabricante presenta el equipo como microbiorreactor para evaluación en tiempo real de esos parámetros. ([beckman.com][1]) | Alta      | No para la afirmación general; sí para instalación local. |
| E02          | BioLector XT tiene sensores ópticos de pH y DO y funciones de control de pH.                           | Explícita         | D02             | Especificaciones de sensores y control | La ficha técnica describe optodos de pH/DO y control de pH con opciones configurables. ([beckman.com][2])                    | Alta      | Sí, para confirmar módulos instalados.                    |
| E03          | Biostat B admite configuraciones con recipientes de 5 L y 10 L.                                        | Explícita         | D03             | Descripción de recipientes             | El brochure enumera recipientes Univessel Glass de 1 L, 2 L, 5 L y 10 L. ([Sartorius][3])                                    | Alta      | Sí, para identificar el modelo local.                     |
| E04          | Biostat B separa torre de control, bombas, aireación, control de temperatura y conexiones de sensores. | Explícita         | D03             | Arquitectura del sistema               | Se documentan módulos de control, bombas, aireación y conexiones para sensores. ([Sartorius][3])                             | Alta      | Sí, para configuración concreta.                          |
| E05          | Biostat B puede controlar automáticamente pH y DO.                                                     | Explícita         | D03             | Control automático de pH y DO          | El documento describe acciones sobre ácido/base, CO₂, agitación y gases para controlar pH y DO. ([Sartorius][3])             | Alta      | Sí, para estrategia aplicada en cada corrida.             |
| E06          | Biostat B puede capturar, almacenar y visualizar datos de proceso.                                     | Explícita         | D03             | Biobrain Supervise                     | El brochure atribuye esas funciones al sistema de supervisión de proceso. ([Sartorius][3])                                   | Alta      | Sí, para confirmar software y exportaciones locales.      |
| E07          | SOSA/SSN separa sistemas, sensores, actuadores, observaciones, propiedades y entidades observadas.     | Explícita         | D06             | Vocabulario SOSA/SSN                   | El estándar enumera estas clases y sus relaciones centrales. ([W3C][6])                                                      | Alta      | No.                                                       |
| E08          | Una corrida de cultivo puede modelarse como actividad y los datos como entidades generadas.            | Inferida          | D06, D07        | Alineamiento SOSA–PROV y PROV-O        | SOSA alinea observaciones y actuaciones con actividades; PROV-O define actividades, entidades y generación. ([W3C][6])       | Media     | Sí.                                                       |
| E09          | La configuración exacta de Sartorius 5 L y 10 L no puede derivarse solo de la capacidad nominal.       | No establecida    | Corpus completo | No aplica                              | Faltan manuales, etiquetas de modelo, configuraciones y registros de activos del laboratorio.                                | Alta      | Sí, obligatoria.                                          |

---

## 9. Conceptos ontológicos candidatos

| Concepto candidato                                | Tipo sugerido     | Definición basada en evidencia                                                                               | Fuente asociada             | Estado                      |
| ------------------------------------------------- | ----------------- | ------------------------------------------------------------------------------------------------------------ | --------------------------- | --------------------------- |
| `BioreactorAsset`                                 | Clase             | Activo físico que proporciona infraestructura para cultivo, medición y/o control.                            | D01, D03, D05               | Candidato                   |
| `BioLectorXTModel`                                | Subclase          | Modelo de microbiorreactor asociado a monitorización óptica y control configurado.                           | D01, D02                    | Candidato                   |
| `BiostatBModel`                                   | Subclase          | Modelo de biorreactor de banco asociado a torre de control y recipientes intercambiables.                    | D03                         | Candidato                   |
| `UnivesselGlass5LModel`                           | Subclase          | Configuración de recipiente de cultivo de capacidad nominal 5 L.                                             | D03, D05                    | Candidato                   |
| `UnivesselGlass10LModel`                          | Subclase          | Configuración de recipiente de cultivo de capacidad nominal 10 L.                                            | D03, D05                    | Candidato                   |
| `CultureVessel`                                   | Clase             | Recipiente físico donde se contiene la cultura.                                                              | D03, D05                    | Candidato                   |
| `CultivationRun`                                  | Clase             | Ejecución temporal de una operación de cultivo. Alinear con `prov:Activity`.                                 | D03, D07                    | Candidato                   |
| `ProcessPhase`                                    | Clase             | Segmento temporal de una corrida, por ejemplo batch, fed-batch, continuo o perfusión.                        | D03                         | Candidato                   |
| `Culture`                                         | Clase             | Entidad biológica cultivada y posible `sosa:FeatureOfInterest`.                                              | D06                         | Candidato                   |
| `ControlSystem`                                   | Clase             | Sistema que implementa lógica o procedimientos de control. Alinear con `sosa:System`.                        | D03, D06                    | Candidato                   |
| `Sensor`                                          | Clase             | Sistema que implementa un procedimiento de observación. Alinear con `sosa:Sensor`.                           | D03, D06                    | Candidato                   |
| `Actuator`                                        | Clase             | Sistema que implementa una acción sobre una propiedad o condición del proceso.                               | D03, D06                    | Candidato                   |
| `ProcessVariable`                                 | Clase             | Propiedad medible o controlable del cultivo, del recipiente o de un componente. Alinear con `sosa:Property`. | D01, D03, D06               | Candidato                   |
| `pH`, `DissolvedOxygen`, `Biomass`, `Temperature` | Individuo         | Instancias controladas de `ProcessVariable`; no son observaciones ni valores numéricos.                      | D01, D03, D06               | Candidato                   |
| `MeasurementObservation`                          | Subclase          | Observación concreta de una propiedad mediante un sensor. Alinear con `sosa:Observation`.                    | D06                         | Candidato                   |
| `MeasurementResult`                               | Clase             | Resultado asociado a una observación; puede alinearse con `prov:Entity`.                                     | D06, D07                    | Candidato                   |
| `ProcessDataSet`                                  | Clase             | Conjunto o archivo de datos de proceso derivado de observaciones.                                            | D03, D07                    | Candidato                   |
| `ControlSetpoint`                                 | Concepto auxiliar | Valor u objetivo operativo usado por un sistema de control.                                                  | D02, D03                    | Requiere validación experta |
| `DataQualityAssertion`                            | Concepto auxiliar | Afirmación sobre validez, calibración, ausencia de datos o calidad de una medición.                          | No establecido en el corpus | Requiere corpus adicional   |

**Nota técnica:** no se recomienda usar `sosa:ObservableProperty` ni `sosa:ActuatableProperty` como clases principales, porque la edición actual de SSN indica que dichas especializaciones están deprecadas en favor de `sosa:Property`. Tampoco se recomienda modelar resultados nuevos como `sosa:Result`, clase indicada como deprecada. ([W3C][6])

---

## 10. Relaciones ontológicas candidatas

| Relación candidata          | Dominio sugerido   | Rango sugerido      | Significado                                                        | Evidencia asociada | Estado                      |
| --------------------------- | ------------------ | ------------------- | ------------------------------------------------------------------ | ------------------ | --------------------------- |
| `hasPhysicalComponent`      | `BioreactorAsset`  | `PhysicalEquipment` | Relaciona un activo compuesto con sus componentes físicos.         | D03, D05           | Candidato local             |
| `sosa:hasSubSystem`         | `sosa:System`      | `sosa:System`       | Relaciona un sistema con sus subsistemas.                          | D06 ([W3C][6])     | Candidato soportado         |
| `sosa:hosts`                | `sosa:Platform`    | `sosa:System`       | Indica que una plataforma aloja un sistema, por ejemplo un sensor. | D06 ([W3C][6])     | Candidato soportado         |
| `isExecutedIn`              | `CultivationRun`   | `BioreactorAsset`   | Relaciona una corrida con el activo físico donde se ejecuta.       | D01, D03           | Candidato local             |
| `hasProcessPhase`           | `CultivationRun`   | `ProcessPhase`      | Relaciona una corrida con sus fases temporales.                    | D03                | Candidato local             |
| `sosa:hasFeatureOfInterest` | `sosa:Observation` | `Culture`           | Indica la entidad sobre la cual aplica la observación.             | D06 ([W3C][6])     | Candidato soportado         |
| `sosa:observedProperty`     | `sosa:Observation` | `sosa:Property`     | Indica la propiedad medida, por ejemplo pH o DO.                   | D06 ([W3C][6])     | Candidato soportado         |
| `sosa:madeBySensor`         | `sosa:Observation` | `sosa:Sensor`       | Vincula una observación con el sensor productor.                   | D06 ([W3C][6])     | Candidato soportado         |
| `sosa:hasResult`            | `sosa:Observation` | `MeasurementResult` | Vincula una observación con su resultado.                          | D06 ([W3C][6])     | Candidato soportado         |
| `sosa:phenomenonTime`       | `sosa:Observation` | `TemporalEntity`    | Representa el tiempo al que aplica la medición.                    | D06 ([W3C][6])     | Candidato soportado         |
| `sosa:actsOn`               | `sosa:Actuator`    | `sosa:Property`     | Indica la propiedad sobre la que puede actuar un actuador.         | D06                | Requiere validación experta |
| `sosa:actsOnProperty`       | `sosa:Actuation`   | `sosa:Property`     | Indica la propiedad afectada por una actuación de control.         | D06 ([W3C][6])     | Candidato soportado         |
| `hasSetpoint`               | `ControlSystem`    | `ControlSetpoint`   | Relaciona un control con su objetivo configurado.                  | D02, D03           | Candidato local             |
| `prov:wasGeneratedBy`       | `ProcessDataSet`   | `prov:Activity`     | Vincula una entidad de datos con la actividad que la generó.       | D07 ([W3C][7])     | Candidato soportado         |
| `prov:wasDerivedFrom`       | `ProcessDataSet`   | `prov:Entity`       | Relaciona un conjunto derivado con sus datos fuente.               | D07 ([W3C][7])     | Candidato soportado         |

---

## 11. Triadas RDF candidatas

| Triada RDF candidata                                                           | Documento de soporte | Página o sección                                                 | Estado                      |
| ------------------------------------------------------------------------------ | -------------------- | ---------------------------------------------------------------- | --------------------------- |
| `BioLectorXT_Unit_01 -> rdf:type -> BioreactorAsset`                           | D01, D02             | Descripción del producto y ficha técnica. ([beckman.com][1])     | requiere validación experta |
| `BiostatB_Unit_01 -> hasPhysicalComponent -> UnivesselGlass5L_01`              | D03, D05             | Recipientes de 5 L y arquitectura de sistema. ([Sartorius][3])   | parcialmente soportada      |
| `BiostatB_Unit_01 -> hasPhysicalComponent -> BiostatBControlTower_01`          | D03                  | Torre de control y módulos asociados. ([Sartorius][3])           | parcialmente soportada      |
| `BiostatBControlTower_01 -> rdf:type -> ControlSystem`                         | D03, D06             | Control tower y definición de `sosa:System`. ([Sartorius][3])    | parcialmente soportada      |
| `pHSensor_01 -> rdf:type -> sosa:Sensor`                                       | D02, D03, D06        | Sensores de pH y definición de sensor. ([beckman.com][2])        | parcialmente soportada      |
| `pHSensor_01 -> sosa:observes -> pH`                                           | D02, D03, D06        | Evidencia de sensores de pH y patrón SOSA. ([beckman.com][2])    | requiere validación experta |
| `CultivationRun_001 -> rdf:type -> prov:Activity`                              | D03, D07             | Modos de proceso y definición de actividad. ([Sartorius][3])     | parcialmente soportada      |
| `Observation_pH_001 -> rdf:type -> sosa:Observation`                           | D06                  | Definición de observación. ([W3C][6])                            | soportada                   |
| `Observation_pH_001 -> sosa:hasFeatureOfInterest -> Culture_001`               | D06                  | Relación entre observación y entidad observada. ([W3C][6])       | soportada                   |
| `Observation_pH_001 -> sosa:observedProperty -> pH`                            | D06                  | Propiedad observada. ([W3C][6])                                  | soportada                   |
| `Observation_pH_001 -> sosa:madeBySensor -> pHSensor_01`                       | D06                  | Sensor que realiza la observación. ([W3C][6])                    | soportada                   |
| `Observation_pH_001 -> sosa:hasResult -> MeasurementResult_pH_001`             | D06                  | Relación entre observación y resultado. ([W3C][6])               | soportada                   |
| `MeasurementResult_pH_001 -> prov:wasGeneratedBy -> Observation_pH_001`        | D06, D07             | Alineamiento SOSA–PROV y generación de entidades. ([W3C][6])     | requiere validación experta |
| `ProcessDataSet_001 -> prov:wasDerivedFrom -> MeasurementResultCollection_001` | D07                  | Derivación entre entidades de datos. ([W3C][7])                  | parcialmente soportada      |
| `DOControlActuation_001 -> sosa:actsOnProperty -> DissolvedOxygen`             | D03, D06             | Control automático de DO y patrón de actuación. ([Sartorius][3]) | parcialmente soportada      |
| `CultivationRun_001 -> isExecutedIn -> UnivesselGlass5L_01`                    | D03, D05             | Relación inferida entre corrida y recipiente. ([Sartorius][3])   | requiere validación experta |

---

## 12. Sinónimos y variantes terminológicas

| Término principal      | Sinónimos o variantes documentadas                                           | Idioma | Documento de soporte        |
| ---------------------- | ---------------------------------------------------------------------------- | ------ | --------------------------- |
| `dissolved oxygen`     | `DO`                                                                         | Inglés | D01, D03 ([beckman.com][1]) |
| `mass flow controller` | `MFC`                                                                        | Inglés | D03 ([Sartorius][3])        |
| `culture vessel`       | `cultivation vessel`                                                         | Inglés | D03, D05 ([Sartorius][3])   |
| `pH control`           | `triggered pH control`; `automatic pH control`                               | Inglés | D02, D03 ([beckman.com][2]) |
| `process data`         | `process data capture`; `process data visualization`                         | Inglés | D03 ([Sartorius][3])        |
| `Control Tower`        | `BioPAT® DCU` como designación de controlador; no asumir sinonimia estricta. | Inglés | D03 ([Sartorius][3])        |

---

## 13. Vacíos, riesgos y decisiones pendientes

- Debe obtenerse la referencia exacta de modelo, configuración, sensores, actuadores, software y firmware para cada sistema Sartorius de 5 L y 10 L.
- Debe verificarse si el BioLector XT disponible posee módulos de gasificación, control de pH, alimentación y las placas específicas utilizadas.
- `pH`, `DO`, temperatura o biomasa no deben asociarse automáticamente al mismo `FeatureOfInterest`; algunas propiedades corresponden al cultivo, otras al recipiente o a un componente físico.
- Debe decidirse si los modelos comerciales se representarán como clases y las unidades instaladas como individuos.
- Debe definirse una ontología de unidades y cantidades, por ejemplo para valores, unidades, límites y setpoints.
- Debe incorporarse evidencia local sobre frecuencia de muestreo, calibración, calidad, datos faltantes, alarmas y exportación de archivos.
- Las relaciones locales como `isExecutedIn`, `hasPhysicalComponent`, `hasSetpoint` y `hasProcessPhase` requieren revisión ontológica y validación por especialistas de bioproceso y automatización.

---

## 14. Registro metodológico para el documento de investigación

La pregunta ALC-05 examinó la separación ontológica entre infraestructura física de biorreactores, proceso biológico, control, variables medidas y datos generados. La búsqueda priorizó documentación oficial de Beckman Coulter y Sartorius, complementada con los estándares W3C SOSA/SSN y PROV-O. Se seleccionaron fuentes que describen BioLector XT, Biostat B, recipientes Univessel Glass de 5 L y 10 L, sensores, control de pH y DO, módulos de proceso y captura de datos. La evidencia permitió proponer, de forma preliminar, clases para activos físicos, corridas de cultivo, sistemas de control, variables de proceso, observaciones y conjuntos de datos. La principal limitación es la ausencia de documentación específica de la configuración instalada, por lo que las instancias de equipos, sensores, señales, alarmas y relaciones de control requieren validación con expertos y registros locales. ([beckman.com][1])

---

## 15. Estado final

- **Nivel de confianza general:** Medio.
- **Estado de la respuesta:** Parcialmente soportada.
- **Estado del corpus:** Parcial.
- **Próxima acción recomendada:** recopilar manuales y configuraciones locales de los sistemas Sartorius de 5 L y 10 L, junto con ejemplos reales de exportación de datos y recetas de control, antes de fijar individuos OWL y restricciones de propiedades.

[1]: https://www.beckman.com/microbioreactor/biolector-xt "BioLector XT Microbioreactor"
[2]: https://www.beckman.com/resources/reading-material/product-instructions/biolector-xt-technical-data-sheet "BioLector XT Technical Data Sheet"
[3]: https://www.sartorius.com/download/34576/broch-biostat-b-sbi1513-e-1--data.pdf "Biostat® B Multi-talented bioreactor"
[4]: https://www.sartorius.com/en/products/fermentation-bioreactors/benchtop-bioreactors/biostat-b " Biostat® B - Benchtop Bioreactor Controller | Sartorius"
[5]: https://www.sartorius.com/en/products/fermentation-bioreactors/benchtop-bioreactors/univessel-glass "Univessel® Glass - Autoclavable Cultivation Vessel | Sartorius"
[6]: https://www.w3.org/TR/vocab-ssn-2023/ "Semantic Sensor Network Ontology - 2023 Edition"
[7]: https://www.w3.org/TR/prov-o/ "PROV-O: The PROV Ontology"
[8]: https://www.sartorius.com/en/products/fermentation-bioreactors/single-use-bioreactors "Single-Use Bioreactors | Sartorius"
