# Extracción de conocimiento ontológico — ALC-05

---

## 1. ID y pregunta

**ID:** ALC-05
**Pregunta:** ¿Cómo se separan ontológicamente el equipo físico, el proceso biológico, el sistema de control, las variables medidas y los datos generados?

---

## 2. Respuesta basada en evidencia

La separación ontológica de las cinco capas se sustenta en tres marcos documentados en el corpus:

**Capa 1 — Equipo físico:** BFO divide las entidades en dos categorías disjuntas: _continuant_ y _occurrent_. Los continuants consisten en objetos y regiones espaciales, y pueden permanecer a través del tiempo. El biorreactor físico es un `bfo:MaterialEntity` / `bfo:Object`. En SSN, un `ssn:System` es una abstracción para un dispositivo físico que puede contener otros sistemas, y se describe en términos de un conjunto de `ssn-system:SystemCapability`.

**Capa 2 — Proceso biológico:** En MCBO, `MammalianCellCultureProcess` se define como la intersección de `CellCultureProcess` con una restricción de participante que requiere al menos una célula mamífera. Las condiciones ambientales del cultivo se modelan como cualidades del sistema de cultivo celular material, en consonancia con los principios BFO. El proceso biológico es un `bfo:Process` (occurrent).

**Capa 3 — Sistema de control:** SSN/SOSA va más allá de la representación de equipos y abarca dispositivos de control. Los sistemas pueden implementar procedimientos que ejecutan acciones basadas en entradas de observación. `sosa:Actuator` son dispositivos que implementan procedimientos SOSA para alterar el estado del entorno. `sosa:ActuatableProperty` caracteriza qué aspectos de un `sosa:FeatureOfInterest` pueden ser actuados.

**Capa 4 — Variables medidas:** Las clases núcleo de SSN/SOSA incluyen: `Sensor` (dispositivos que realizan observaciones), `Observation` (fenómenos medidos), `Feature of Interest` (entidades del mundo real), `ObservableProperty` (características observables), `Stimulus` (que desencadena respuestas del sensor) y `Result` (datos generados como salida).

**Capa 5 — Datos generados:** Existe una falta de ontologías coherentes para representar conocimiento de procesos de biofabricación, modelos de control y ocurrencias reales. Si bien IOF Core ha proporcionado una base en BFO, aún existen construcciones insuficientes y orientación clara sobre la representación de artefactos digitales y sus correspondencias con las contrapartes físicas. Los datos generados se modelan como `bfo:GenericallyDependentContinuant` o como literales XSD vinculados mediante `sosa:hasResult`.

---

## 3. Tabla de afirmaciones y evidencia

| ID ev. | Afirmación                                                                                                            | Evidencia (fragmento resumido)                                                                                                    | Fuente           | Sección                                       | Tipo      | Confianza | Validación experta                                                   |
| ------ | --------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------- | ---------------- | --------------------------------------------- | --------- | --------- | -------------------------------------------------------------------- |
| E01    | El biorreactor físico es un `bfo:MaterialEntity` (`bfo:Object`), un continuant independiente                          | BFO divide entidades en continuants (objetos) y occurrents (procesos); los objetos persisten en el tiempo                         | SRC-007          | Estructura BFO: división Continuant/Occurrent | Explícita | Alta      | No                                                                   |
| E02    | El `ssn:System` modela el dispositivo físico y puede contener subsistemas                                             | En SSN, un `ssn:System` es una abstracción para un dispositivo físico que puede contener otros sistemas                           | SRC-001          | Sección SSN System                            | Explícita | Alta      | No                                                                   |
| E03    | El proceso biológico de cultivo es un `bfo:Process` (occurrent) que depende de una entidad material                   | BFO: los procesos son occurrents que se extienden en el tiempo y dependen de entidades materiales                                 | SRC-007          | División Continuant/Occurrent                 | Explícita | Alta      | No                                                                   |
| E04    | `MammalianCellCultureProcess` es la intersección de `CellCultureProcess` con restricción de participante mamífero     | MCBO define `MammalianCellCultureProcess` como intersección de `CellCultureProcess` + participante mamífero                       | SRC-004          | Sección diseño ontológico                     | Explícita | Alta      | Sí — confirmar generalización a `BiologicalCultivationProcess`       |
| E05    | Las condiciones de cultivo (pH, DO, temperatura) se modelan como `bfo:Quality` que inhieren en la entidad de cultivo  | MCBO: condiciones ambientales del cultivo se modelan como cualidades del sistema de cultivo material, consistente con BFO         | SRC-004          | Sección diseño ontológico                     | Explícita | Alta      | Sí — verificar equivalencia con `sosa:ObservableProperty`            |
| E06    | El sistema de control se modela con `sosa:Actuator` y `sosa:Actuation`                                                | SSN/SOSA incluye `sosa:Actuator` como dispositivos que implementan procedimientos para alterar el estado del entorno              | SRC-001          | Sección SOSA core: Actuator                   | Explícita | Alta      | No                                                                   |
| E07    | `sosa:ActuatableProperty` caracteriza qué aspectos del feature of interest pueden ser actuados                        | SOSA introduce `sosa:ActuatableProperty` para caracterizar qué aspectos de un `FeatureOfInterest` pueden ser actuados             | SRC-001          | Sección SOSA core: ActuatableProperty         | Explícita | Alta      | No                                                                   |
| E08    | Las variables medidas son `sosa:ObservableProperty`; el acto de medición es `sosa:Observation`                        | SSN/SOSA: `ObservableProperty` son características observables; `Observation` son los fenómenos medidos                           | SRC-001, SRC-003 | SOSA core; tabla de clases SSN/SOSA           | Explícita | Alta      | No                                                                   |
| E09    | El biorreactor puede actuar como `sosa:Platform` que aloja sensores                                                   | SSN define `sosa:Platform` como entidad que aloja o porta sensores y actuadores                                                   | SRC-001          | Sección Platform                              | Inferida  | Media     | Sí — decidir si biorreactor es Platform, FeatureOfInterest o ambos   |
| E10    | Los datos generados se vinculan mediante `sosa:hasResult` a la observación                                            | SSN/SOSA: `sosa:hasResult` conecta una observación con su resultado                                                               | SRC-001          | Sección SOSA: hasResult                       | Explícita | Alta      | No                                                                   |
| E11    | En SSN 2023, `sosa:Result` como clase fue deprecada; se prefiere valor literal o nodo anónimo                         | SSN 2023: marca `sosa:Result` como deprecated; agrega `ObservationCollection`, `ActuationCollection`                              | SRC-002          | Sección de cambios 2023                       | Explícita | Alta      | Sí — definir si el proyecto usa Result como clase o literal          |
| E12    | Los artefactos digitales (datos generados) no tienen aún representación completa en IOF Core                          | IOF Core tiene construcciones insuficientes para representar artefactos digitales y sus correspondencias con contrapartes físicas | SRC-006          | Abstract / introducción                       | Explícita | Alta      | Sí — seguir desarrollo IOF                                           |
| E13    | Los datos de sensores del biorreactor actualizan su gemelo digital; las simulaciones del gemelo controlan actuadores  | Figura 7 NIST: datos de sensores → actualizan digital twin; simulaciones del twin → controlan parámetros de actuadores            | SRC-005          | Figuras 5, 6, 7, 8                            | Explícita | Alta      | Sí — mapear a clases OWL concretas                                   |
| E14    | ISA-88 se formaliza en módulos OWL 2 separados: modelo físico y modelo procedimental de control                       | ISA-88 se divide en módulos ontológicos OWL 2; módulo procedimental como el más avanzado                                          | SRC-008          | Sección implementación OWL 2                  | Explícita | Alta      | Sí — verificar cuáles módulos aplican al proyecto                    |
| E15    | La arquitectura BFO + IOF Core (hub-and-spoke) es la base recomendada por NIST para bioprocesos, incluyendo ISA-88/95 | NIST propone BFO como top-level y arquitectura hub-and-spoke; ontologización basada en ISA-88 e ISA-95                            | SRC-009          | Sección Technical Idea                        | Explícita | Alta      | No                                                                   |
| E16    | `ObservationCollection` y `ActuationCollection` permiten agrupar series temporales de observaciones                   | SSN 2023 agrega `ObservationCollection`, `ActuationCollection`, `SamplingCollection` con `hasMember` / `isMemberOf`               | SRC-002          | Sección de cambios 2023                       | Explícita | Alta      | Sí — evaluar uso para series de datos de proceso                     |
| E17    | La separación receta/equipo de ISA-88 corresponde a separar proceso biológico de equipo físico en la ontología        | ISA-88 separa la receta (qué se hace) del equipo (cómo se hace); cada módulo tiene control dedicado                               | SRC-008          | Sección módulos ISA-88                        | Inferida  | Media     | Sí — validar equivalencia con la división BFO Process/MaterialEntity |
| E18    | SOSA define `ObservingProcedure`, `ActuatingProcedure` y `SamplingProcedure` como procedimientos especializados       | SSN 2023 agrega `ActuatingProcedure`, `ObservingProcedure`, `SamplingProcedure` como especializaciones de `Procedure`             | SRC-002          | Sección de cambios 2023                       | Explícita | Alta      | No                                                                   |

---

## 4. Conceptos candidatos

| Concepto candidato              | Tipo                                             | Definición basada en corpus                                                                                                                                  | Fuente                    | Estado                                  |
| ------------------------------- | ------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------- | --------------------------------------- |
| `PhysicalBioreactor`            | Clase                                            | Entidad material independiente (`bfo:MaterialEntity` / `bfo:Object`) que constituye el sistema de biorreactor en una escala operativa dada                   | SRC-007, SRC-005          | Candidato                               |
| `BiologicalCultivationProcess`  | Clase                                            | Proceso occurrent (`bfo:Process`) que representa el cultivo celular o fermentación dentro del biorreactor; depende de la entidad de cultivo material         | SRC-007, SRC-004          | Candidato                               |
| `CellCultureProcess`            | Clase (padre)                                    | Superclase del proceso de cultivo celular, generalizable más allá de mamíferos; base de `MammalianCellCultureProcess` en MCBO                                | SRC-004                   | Candidato — reutilizar de MCBO          |
| `ControlSystem`                 | Clase / Subclase de `ssn:System`                 | Sistema físico (continuant) que implementa lógica de control; contiene sensores y actuadores como subsistemas                                                | SRC-001, SRC-008          | Candidato                               |
| `BioreactorSensor`              | Subclase de `sosa:Sensor`                        | Sensor físico instalado en o sobre el biorreactor que realiza observaciones de propiedades del cultivo                                                       | SRC-001, SRC-003          | Candidato                               |
| `BioreactorActuator`            | Subclase de `sosa:Actuator`                      | Dispositivo físico que altera propiedades del entorno de cultivo (agitador, válvula de gas, bomba)                                                           | SRC-001, SRC-005          | Candidato                               |
| `CultivationObservableProperty` | Subclase de `sosa:ObservableProperty`            | Propiedad observable del cultivo (pH, DO, temperatura, biomasa); correlaciona con `bfo:Quality` de la entidad de cultivo                                     | SRC-001, SRC-004          | Candidato                               |
| `CultivationObservation`        | Subclase de `sosa:Observation`                   | Acto singular de medición de una propiedad observable del cultivo en un instante temporal                                                                    | SRC-001, SRC-002, SRC-003 | Candidato                               |
| `CultivationActuation`          | Subclase de `sosa:Actuation`                     | Acto occurrent mediante el cual un actuador modifica una propiedad actable del entorno de cultivo                                                            | SRC-001, SRC-005          | Candidato                               |
| `CultivationActuatableProperty` | Subclase de `sosa:ActuatableProperty`            | Propiedad del entorno de cultivo que puede ser alterada por un actuador (velocidad de agitación, flujo de gas, temperatura de calefacción)                   | SRC-001                   | Candidato                               |
| `MeasuredDataRecord`            | Subclase de `bfo:GenericallyDependentContinuant` | Artefacto de información (dato numérico con unidad y timestamp) generado como resultado de una observación; su modelado completo no está definido aún en IOF | SRC-006, SRC-007          | Candidato — patrón IOF incompleto       |
| `ObservationCollection`         | Clase (reutilizar de SSN 2023)                   | Colección de observaciones relacionadas; útil para series temporales de datos de proceso                                                                     | SRC-002                   | Candidato — disponible en SSN 2023      |
| `ObservingProcedure`            | Clase (reutilizar de SSN 2023)                   | Procedimiento especializado de observación; subclase de `sosa:Procedure`                                                                                     | SRC-002                   | Candidato — disponible en SSN 2023      |
| `ActuatingProcedure`            | Clase (reutilizar de SSN 2023)                   | Procedimiento especializado de actuación; subclase de `sosa:Procedure`                                                                                       | SRC-002                   | Candidato — disponible en SSN 2023      |
| `CultivationFeatureOfInterest`  | Subclase de `sosa:FeatureOfInterest`             | Entidad del mundo real sobre la que se realizan observaciones: el cultivo, el medio, o el biorreactor mismo                                                  | SRC-001, SRC-003          | Candidato — requiere decisión de diseño |

---

## 5. Relaciones candidatas con dominio y rango sugeridos

| Relación candidata          | Dominio sugerido         | Rango sugerido                           | Significado                                                                      | Fuente                                                  | Estado                                                          |
| --------------------------- | ------------------------ | ---------------------------------------- | -------------------------------------------------------------------------------- | ------------------------------------------------------- | --------------------------------------------------------------- |
| `sosa:hosts`                | `PhysicalBioreactor`     | `BioreactorSensor`, `BioreactorActuator` | El biorreactor aloja físicamente sensores y actuadores como plataforma SSN       | SRC-001                                                 | Soportada — relación estándar SOSA Platform                     |
| `ssn:hasSubSystem`          | `ControlSystem`          | `BioreactorSensor`, `BioreactorActuator` | El sistema de control contiene sensores y actuadores como subsistemas            | SRC-001                                                 | Soportada — relación estándar SSN                               |
| `sosa:observes`             | `BioreactorSensor`       | `CultivationObservableProperty`          | El sensor está configurado para observar una propiedad específica del cultivo    | SRC-001                                                 | Soportada — relación estándar SOSA                              |
| `sosa:madeObservation`      | `BioreactorSensor`       | `CultivationObservation`                 | El sensor realizó un acto concreto de observación                                | SRC-001                                                 | Soportada — relación estándar SOSA                              |
| `sosa:hasFeatureOfInterest` | `CultivationObservation` | `CultivationFeatureOfInterest`           | La observación tiene como sujeto la entidad de interés del cultivo o biorreactor | SRC-001, SRC-003                                        | Soportada — relación estándar SOSA                              |
| `sosa:observedProperty`     | `CultivationObservation` | `CultivationObservableProperty`          | La observación registra una propiedad observable específica                      | SRC-001                                                 | Soportada — relación estándar SOSA                              |
| `sosa:hasResult`            | `CultivationObservation` | literal XSD o nodo de resultado          | La observación produce un resultado numérico tipado                              | SRC-001, SRC-002                                        | Soportada — con nota: clase `sosa:Result` deprecada en SSN 2023 |
| `sosa:actsOnProperty`       | `CultivationActuation`   | `CultivationActuatableProperty`          | El acto de actuación modifica una propiedad actable del entorno de cultivo       | SRC-001                                                 | Soportada — relación estándar SOSA                              |
| `sosa:madeActuation`        | `BioreactorActuator`     | `CultivationActuation`                   | El actuador realizó un acto de actuación concreto                                | SRC-001                                                 | Soportada — relación estándar SOSA                              |
| `ex:supportsProcess`        | `PhysicalBioreactor`     | `BiologicalCultivationProcess`           | El equipo físico soporta / es el sustrato material del proceso biológico         | SRC-007 (BFO: proceso depende de material entity)       | Inferida — relación BFO exacta requiere validación              |
| `ex:implementsControl`      | `PhysicalBioreactor`     | `ControlSystem`                          | El biorreactor está gobernado por un sistema de control específico               | SRC-005, SRC-008                                        | Inferida — requiere validación                                  |
| `ex:generatesDataRecord`    | `CultivationObservation` | `MeasuredDataRecord`                     | La observación genera un artefacto de información persistente                    | SRC-005, SRC-006 (inferido de figuras NIST y vacío IOF) | Inferida — patrón IOF incompleto; requiere validación experta   |
| `hasMember` / `isMemberOf`  | `ObservationCollection`  | `CultivationObservation`                 | Agrupa observaciones individuales en una colección (serie temporal)              | SRC-002                                                 | Soportada — relación estándar SSN 2023                          |

---

## 6. Triadas RDF candidatas

```turtle
# ─── CAPA 1: EQUIPO FÍSICO ────────────────────────────────────────────────────

ex:PhysicalBioreactor rdfs:subClassOf bfo:MaterialEntity
    # SRC-007 | División Continuant/Occurrent BFO
    # Tipo: explícita | Confianza: alta | Estado: soportada

ex:PhysicalBioreactor rdfs:subClassOf ssn:System
    # SRC-001 | Sección SSN System
    # Tipo: explícita | Confianza: alta | Estado: soportada

ex:BioLectorXT_unit01 rdf:type ex:PhysicalBioreactor
    # SRC-005 | Figura 7 NIST (biorreactor como entidad individual)
    # Tipo: inferida | Confianza: media | Estado: requiere validación experta

# ─── CAPA 2: PROCESO BIOLÓGICO ───────────────────────────────────────────────

ex:BiologicalCultivationProcess rdfs:subClassOf bfo:Process
    # SRC-007 (BFO: Process como occurrent) + SRC-004 (MCBO: CellCultureProcess)
    # Tipo: explícita | Confianza: alta | Estado: soportada

ex:CellCultureProcess rdfs:subClassOf ex:BiologicalCultivationProcess
    # SRC-004 | MCBO: definición de CellCultureProcess
    # Tipo: inferida | Confianza: media | Estado: parcialmente soportada

ex:CultivationRun_20240115 rdf:type ex:BiologicalCultivationProcess
    # SRC-004 | Patrón MCBO de instanciación de procesos
    # Tipo: inferida | Confianza: media | Estado: requiere validación experta

ex:CultivationRun_20240115 ex:supportsedBy ex:BioLectorXT_unit01
    # SRC-007 (BFO: proceso depende de entidad material)
    # Tipo: inferida | Confianza: media | Estado: requiere validación experta

# ─── CAPA 3: SISTEMA DE CONTROL ──────────────────────────────────────────────

ex:ControlSystem rdfs:subClassOf ssn:System
    # SRC-001 (SSN System) + SRC-008 (ISA-88 OWL módulos)
    # Tipo: explícita | Confianza: alta | Estado: soportada

ex:BioreactorActuator rdfs:subClassOf sosa:Actuator
    # SRC-001 | Sección SOSA core: Actuator
    # Tipo: explícita | Confianza: alta | Estado: soportada

ex:CO2_Valve_unit01 rdf:type ex:BioreactorActuator
    # SRC-001, SRC-005 (actuadores del biorreactor)
    # Tipo: inferida | Confianza: media | Estado: requiere validación experta

ex:Actuation_CO2_001 rdf:type sosa:Actuation
    # SRC-001 | Sección SOSA core: Actuation
    # Tipo: explícita | Confianza: alta | Estado: soportada

ex:Actuation_CO2_001 sosa:actsOnProperty ex:CO2SupplyProperty
    # SRC-001 | sosa:actsOnProperty
    # Tipo: explícita | Confianza: alta | Estado: soportada

ex:CO2SupplyProperty rdf:type sosa:ActuatableProperty
    # SRC-001 | Sección SOSA core: ActuatableProperty
    # Tipo: explícita | Confianza: alta | Estado: soportada

ex:ControlSystem ssn:hasSubSystem ex:BioreactorSensor_pH_01
    # SRC-001 | ssn:hasSubSystem
    # Tipo: explícita | Confianza: alta | Estado: soportada

# ─── CAPA 4: VARIABLES MEDIDAS ───────────────────────────────────────────────

ex:CultivationObservableProperty rdfs:subClassOf sosa:ObservableProperty
    # SRC-001 | SOSA core: ObservableProperty
    # Tipo: explícita | Confianza: alta | Estado: soportada

ex:pH_Observable rdf:type ex:CultivationObservableProperty
    # SRC-001, SRC-004 (pH como propiedad del cultivo)
    # Tipo: inferida | Confianza: alta | Estado: parcialmente soportada

ex:DissolvedOxygen_Observable rdf:type ex:CultivationObservableProperty
    # SRC-001, SRC-004
    # Tipo: inferida | Confianza: alta | Estado: parcialmente soportada

ex:BioreactorSensor rdfs:subClassOf sosa:Sensor
    # SRC-001 | SOSA core: Sensor
    # Tipo: explícita | Confianza: alta | Estado: soportada

ex:BioreactorSensor_pH_01 sosa:observes ex:pH_Observable
    # SRC-001 | sosa:observes
    # Tipo: explícita | Confianza: alta | Estado: soportada

ex:Observation_pH_001 rdf:type sosa:Observation
    # SRC-001 | SOSA core: Observation
    # Tipo: explícita | Confianza: alta | Estado: soportada

ex:Observation_pH_001 sosa:hasFeatureOfInterest ex:CultivationMedium_001
    # SRC-001 | sosa:hasFeatureOfInterest
    # Tipo: explícita | Confianza: alta | Estado: soportada

ex:Observation_pH_001 sosa:observedProperty ex:pH_Observable
    # SRC-001 | sosa:observedProperty
    # Tipo: explícita | Confianza: alta | Estado: soportada

ex:Observation_pH_001 sosa:madeBySensor ex:BioreactorSensor_pH_01
    # SRC-001 | sosa:madeBySensor
    # Tipo: explícita | Confianza: alta | Estado: soportada

# ─── CAPA 5: DATOS GENERADOS ─────────────────────────────────────────────────

ex:Observation_pH_001 sosa:hasResult "7.2"
    # SRC-001 (sosa:hasResult) + SRC-002 (sosa:Result deprecada como clase)
    # Tipo: explícita | Confianza: alta | Estado: soportada
    # Nota: SSN 2023 deprecó sosa:Result como clase; se prefiere literal o nodo anónimo

ex:MeasuredDataRecord_pH_001 rdf:type bfo:GenericallyDependentContinuant
    # SRC-006 (artefactos digitales como GDC en IOF/BFO) + SRC-007 (BFO)
    # Tipo: inferida | Confianza: media | Estado: parcialmente soportada
    # Nota: IOF Core reconoce vacío en representación de artefactos digitales

ex:MeasuredDataRecord_pH_001 ex:generatedBy ex:Observation_pH_001
    # SRC-005 (figura 7 NIST: datos de sensores → digital twin)
    # Tipo: inferida | Confianza: media | Estado: requiere validación experta

ex:ObsCollection_Run_001 rdf:type sosa:ObservationCollection
    # SRC-002 | SSN 2023: ObservationCollection
    # Tipo: explícita | Confianza: alta | Estado: soportada

ex:ObsCollection_Run_001 sosa:hasMember ex:Observation_pH_001
    # SRC-002 | SSN 2023: hasMember
    # Tipo: explícita | Confianza: alta | Estado: soportada
```

---

## 7. Sinónimos documentados

| Término principal               | Sinónimos / variantes en el corpus                                                                                | Idioma | Fuente                    |
| ------------------------------- | ----------------------------------------------------------------------------------------------------------------- | ------ | ------------------------- |
| `PhysicalBioreactor`            | Physical Equipment, bioreactor (essential biomanufacturing equipment), ssn:System, bfo:MaterialEntity, bfo:Object | EN     | SRC-005, SRC-007, SRC-001 |
| `BiologicalCultivationProcess`  | Bioprocess, Cell Culture Process, CellCultureProcess, MammalianCellCultureProcess, bfo:Process                    | EN     | SRC-004, SRC-007          |
| `ControlSystem`                 | Procedural Control Model (ISA-88), Control Module, automation system, ssn:System                                  | EN     | SRC-008, SRC-001          |
| `CultivationObservableProperty` | Process variable, observable property, measured parameter, bfo:Quality (condiciones de cultivo en MCBO)           | EN     | SRC-001, SRC-004          |
| `CultivationObservation`        | Observation act, measurement event, sensing event, sosa:Observation                                               | EN     | SRC-001, SRC-002, SRC-003 |
| `MeasuredDataRecord`            | Digital artifact, data item, information artifact, bfo:GenericallyDependentContinuant                             | EN     | SRC-006, SRC-007          |
| `sosa:Actuator`                 | Control device, actuator, BioreactorActuator                                                                      | EN     | SRC-001, SRC-005          |
| `sosa:hasResult`                | Observation result, measured value, result literal                                                                | EN     | SRC-001, SRC-002          |
| `ObservationCollection`         | Series temporal de observaciones, data series, ActuationCollection                                                | EN     | SRC-002                   |
| Physical Model (ISA-88)         | Physical layer, equipment hierarchy, Physical Model ontology module                                               | EN     | SRC-008                   |

---

## 8. Vacíos del corpus

| Vacío identificado                                               | Descripción                                                                                                                                                                                      | Fuente que lo señala        |
| ---------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | --------------------------- |
| **V01 — Modelado completo de artefactos digitales**              | IOF Core no tiene aún construcciones suficientes ni guía clara para representar artefactos digitales y su correspondencia con entidades físicas; la Capa 5 no está completamente cubierta        | SRC-006                     |
| **V02 — Deprecación de `sosa:Result` como clase**                | SSN 2023 deprecó `sosa:Result` como clase; no está establecido en el corpus cuál patrón exacto de nodo anónimo o literal reemplaza su uso en este proyecto                                       | SRC-002                     |
| **V03 — Biorreactor como `Platform` vs. `FeatureOfInterest`**    | El corpus no resuelve si el biorreactor debe modelarse como `sosa:Platform` (aloja sensores), como `sosa:FeatureOfInterest` (es lo que se observa/controla), o como ambos simultáneamente        | SRC-001, SRC-003            |
| **V04 — Relación BFO exacta entre proceso y equipo**             | El corpus no especifica la relación BFO formal exacta que conecta `BiologicalCultivationProcess` con `PhysicalBioreactor` (¿`participates in`? ¿`occurs in`? ¿relación de sitio `bfo:Site`?)     | SRC-007                     |
| **V05 — Datos específicos de BioLector XT y Sartorius**          | No hay en el corpus documentos de fabricante que describan los tipos de sensores, variables reportadas o formatos de datos de los sistemas BioLector XT, Sartorius 5L o Sartorius 10L            | No establecido en el corpus |
| **V06 — Equivalencia `bfo:Quality` ↔ `sosa:ObservableProperty`** | MCBO modela condiciones de cultivo como `bfo:Quality`; SOSA usa `sosa:ObservableProperty`; el corpus no establece una alineación formal entre ambas                                              | SRC-004, SRC-001            |
| **V07 — Módulos ISA-88 aplicables al proyecto**                  | El corpus menciona la formalización OWL 2 de ISA-88 en módulos, pero no especifica cuáles niveles (Process Cell, Unit, Equipment Module, Control Module) aplican a la escala BioLector/Sartorius | SRC-008, SRC-009            |
| **V08 — Relación `ex:generatesDataRecord`**                      | No existe en el corpus una relación estándar que conecte formalmente una observación SOSA con un artefacto de datos persistente (`MeasuredDataRecord`); el patrón es inferido de figuras NIST    | SRC-005, SRC-006            |

---

## 9. Estado final

| Criterio                           | Estado                                                                                                                                                                           |
| ---------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Estado general de la respuesta** | **Parcialmente soportada**                                                                                                                                                       |
| **Capa 1 — Equipo físico**         | Soportada — `bfo:MaterialEntity` + `ssn:System` con evidencia explícita alta (SRC-001, SRC-007)                                                                                  |
| **Capa 2 — Proceso biológico**     | Soportada — `bfo:Process` con patrón MCBO verificable (SRC-004, SRC-007); generalización a `BiologicalCultivationProcess` es inferida                                            |
| **Capa 3 — Sistema de control**    | Soportada — `sosa:Actuator`, `sosa:Actuation`, `sosa:ActuatableProperty` con evidencia explícita (SRC-001); módulos ISA-88 OWL verificados (SRC-008)                             |
| **Capa 4 — Variables medidas**     | Soportada — `sosa:ObservableProperty`, `sosa:Observation`, `sosa:FeatureOfInterest` con evidencia explícita alta (SRC-001, SRC-003)                                              |
| **Capa 5 — Datos generados**       | Parcialmente soportada — `sosa:hasResult` con literal soportado; `bfo:GenericallyDependentContinuant` inferido; vacío IOF reconocido explícitamente en corpus (SRC-006)          |
| **Corpus**                         | Parcial — suficiente para nivel arquitectural; insuficiente para individuos reales de BioLector XT y Sartorius                                                                   |
| **Próxima acción**                 | Suministrar manuales de fabricante BioLector XT y Sartorius BIOSTAT; leer texto completo SSN 2023 draft (SRC-002); validar con experto relación BFO entre proceso y equipo (V04) |
