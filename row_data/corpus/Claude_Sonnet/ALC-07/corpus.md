# Extracción condicionada por corpus — ALC-07

---

## 1. ID y Pregunta

**ID:** ALC-07
**Pregunta:** ¿Qué relaciones básicas debe tener cada biorreactor con sensores, actuadores, variables operativas, fases del proceso y eventos?

---

## 2. Respuesta basada en evidencia

### 2.1 Relaciones biorreactor → sensores

**BioLector XT:** Opera con sensores ópticos pre-calibrados en línea. Las MTPs de 48 pocillos permiten medición en línea de biomasa, fluorescencias, pH y oxígeno disuelto (DO). Adicionalmente, el módulo de regulación de O₂ incorpora un sensor de oxígeno dentro de la cámara de cultivo que mide continuamente el nivel de O₂ y regula automáticamente el flujo de nitrógeno u oxígeno.

**Sartorius 5L / 10L:** Los sensores especificados para el BIOSTAT B incluyen: pH, pO₂, temperatura, espuma (foam), nivel (level) y sustrato (substrate).

La relación estructural es: cada `Bioreactor` → `hasSensor` → `Sensor`, donde cada sensor se vincula a una propiedad observable específica.

### 2.2 Relaciones biorreactor → actuadores

**Sartorius:** El sistema de gasificación incluye hasta cuatro controladores de flujo másico (MFCs). El controlador avanzado de DO ajusta simultánea y automáticamente la velocidad del agitador y los caudales de gas de aire y oxígeno puro para controlar el punto de ajuste de DO.

**BioLector XT:** El módulo microfluidico actúa como actuador de pH y alimentación por pocillo, eliminando la manipulación manual de líquidos (SRC-001). Los módulos de regulación de O₂ actúan como actuadores de composición gaseosa (SRC-001).

La relación es: cada `Bioreactor` → `hasActuator` → `Actuator`, y cada actuador → `controls` → `OperatingVariable`.

### 2.3 Relaciones biorreactor → variables operativas

Durante el cultivo, el biorreactor monitorea y ajusta continuamente temperatura, pH, oxígeno disuelto y niveles de nutrientes para mantener el cultivo en su fase más productiva. En el BIOSTAT B, el controlador avanzado de DO vincula variables como velocidad de agitación y caudal de gas como parámetros co-regulados (SRC-003).

### 2.4 Relaciones biorreactor → fases del proceso

Los biorreactores pueden emplear estrategias de alimentación en batch, fed-batch o continuo para optimizar la producción. Las fases biológicas documentadas son: lag (adaptación celular), exponencial (crecimiento rápido de biomasa), estacionaria (equilibrio entre crecimiento y muerte) y muerte (agotamiento de nutrientes). Las fases operativas son: esterilización → inoculación → cultivo → cosecha (SRC-009).

En procesos de proteína recombinante, las fases batch y fed-batch son seguidas por una fase de inducción donde se inicia la expresión del producto objetivo.

### 2.5 Relaciones biorreactor → eventos

La inoculación marca el inicio del bioproceso. Los eventos de alarma documentados para BioLector XT incluyen: detección de fuga por flujo anormal, degradación de optodes por exposición a luz solar, y riesgo de ignición por aceites en líneas de gas (SRC-002). La fase fed-batch genera eventos de adición de substrato controlados por DO o pH (SRC-003, SRC-010).

### 2.6 Marco semántico para las relaciones

En SOSA, una Actuation es realizada por un Actuator y produce un Result. El modelado de actuaciones es análogo al de observaciones, basándose en la misma estructura central. Las actuaciones usando actuadores se describen con la misma terminología y relaciones que las observaciones, compartiendo superclases comunes Execution y System.

---

## 3. Tabla de afirmaciones y evidencia

| ID ev. | Afirmación                                                                                                 | Fragmento de evidencia                                                                                                                                                                          | Fuente / Sección                    | Concepto/Relación/Triada candidata                                                                                           | Tipo      | Confianza | Validación experta                                                                                      |
| ------ | ---------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------- | ---------------------------------------------------------------------------------------------------------------------------- | --------- | --------- | ------------------------------------------------------------------------------------------------------- |
| E01    | BioLector XT mide biomasa, fluorescencias, pH y DO mediante sensores ópticos en línea                      | "Disposable 48 well MTPs enable online measurement of biomass, fluorescences, pH and DO"                                                                                                        | SRC-001 / Página principal          | `BioLectorXT hasSensor BiomassSensor`, `pHSensor`, `DOSensor`                                                                | Explícita | Alta      | No                                                                                                      |
| E02    | BioLector XT tiene un sensor de O₂ interno en la cámara que regula flujo de N₂ u O₂                        | "an oxygen sensor inside the cultivation chamber. The sensor continuously measures the oxygen level inside the chamber and automatically regulates the flow of nitrogen into the chamber"       | SRC-001 / Sección módulos           | `BioLectorXT hasSensor OxygenSensor` ; `OxygenSensor triggersActuation GasFlowRegulation`                                    | Explícita | Alta      | No                                                                                                      |
| E03    | BioLector XT tiene hasta 6 módulos de filtro LED para parámetros específicos                               | "1x BioLector XT microbioreactor with 6 LED filter modules for the parameters biomass, pH (HP8), DO (Pst3), pH (LG1), DO (RF) and riboflavin"                                                   | SRC-001 / Especificaciones técnicas | `BioLectorXT hasMaxSensorModules 6` (dato de propiedad candidato)                                                            | Explícita | Alta      | No                                                                                                      |
| E04    | El módulo microfluidico del BioLector XT controla pH y alimentación por pocillo sin pipeteo                | "patented microfluidic technology supports simultaneous pH control and feeding. The optional microfluidic module eliminates manual liquid handling"                                             | SRC-001 / Módulo microfluidico      | `BioLectorXT hasActuator MicrofluidicModule` ; `MicrofluidicModule controls pH` ; `MicrofluidicModule controls FeedAddition` | Explícita | Alta      | Sí — clasificación sensor/actuador ambigua                                                              |
| E05    | BIOSTAT B tiene sensores de pH, pO₂, temperatura, espuma, nivel y sustrato                                 | "Sensors: pH, pO2, Temperature, Foam, Level, Substrate"                                                                                                                                         | SRC-005 / Technical features        | `SartoriusBioreactor hasSensor pHSensor`, `DOSensor`, `TemperatureSensor`, `FoamSensor`, `LevelSensor`, `SubstrateSensor`    | Explícita | Alta      | Sí — tipo de sensor de sustrato no especificado                                                         |
| E06    | BIOSTAT B admite cuatro gases: aire, O₂, CO₂, N₂ con caudal máximo 20 lpm                                  | "Gas flow: air, O2, CO2\*, N2 (max. total flow rate 20 lpm)"                                                                                                                                    | SRC-005 / Technical features        | `SartoriusBioreactor hasOperatingVariable GasFlowRate` ; `GasFlowRate hasMaxValue 20 lpm`                                    | Explícita | Alta      | No                                                                                                      |
| E07    | BIOSTAT B tiene hasta cuatro MFCs para control de gases                                                    | "Gassing system comparable to our Biostat STR® with up to four mass flow controller"                                                                                                            | SRC-003 / Descripción producto      | `SartoriusBioreactor hasActuator MassFlowController`                                                                         | Explícita | Alta      | No                                                                                                      |
| E08    | El controlador avanzado de DO del BIOSTAT B ajusta simultáneamente velocidad de agitador y caudales de gas | "The advanced DO controller supports parallel adjustment of all DO affecting parameter settings like stirrer speed and gas flow rates of air and pure oxygen, automatically and simultaneously" | SRC-003 / DO cascade                | `AgitatorMotor controls AgitationSpeed` ; `MassFlowController controls GasFlowRate` ; ambos `regulatedBy DOController`       | Explícita | Alta      | No                                                                                                      |
| E09    | BIOSTAT B opera en modos batch, fed-batch, continuo y perfusión                                            | "This enables you to run your Biostat® B in batch, fed-batch, continuous or perfusion mode"                                                                                                     | SRC-003 / Modos de proceso          | `SartoriusBioreactor hasFeedingMode BatchMode`, `FedBatchMode`, `ContinuousMode`, `PerfusionMode`                            | Explícita | Alta      | No                                                                                                      |
| E10    | Un flujo >0,5 L/min en reposo en BioLector XT indica posible fuga y constituye alarma de proceso           | "A flow rate above 0.5 L/min at rest with the microtiter plate clamped could indicate leakage. This may impact your experiment results"                                                         | SRC-002 / p.8 System Configuration  | `BioLectorXT hasEvent LeakageAlarmEvent` ; `LeakageAlarmEvent triggeredBy AbnormalGasFlowRate`                               | Explícita | Alta      | No                                                                                                      |
| E11    | El almacenamiento incorrecto de optodes genera lecturas erróneas de pH y DO en BioLector XT                | "Storing microtiter plates and optodes in sunlight and at the incorrect temperature can cause the optodes to bleach resulting in incorrect readings for pH and DO measurements"                 | SRC-002 / p.8                       | `BioLectorXT hasEvent OptodeDegradationEvent` ; `OptodeDegradationEvent affects pHSensor`, `DOSensor`                        | Explícita | Alta      | No                                                                                                      |
| E12    | El BIOSTAT B-DCU se integra con software supervisorio Biobrain® o DeltaV™                                  | "Easily connect your Biostat® B-DCU to our Biobrain® Supervise or third party supervisory software like DeltaV™"                                                                                | SRC-004 / Descripción general       | `SartoriusBioreactor connectedTo SupervisorySystem` (relación candidata de integración)                                      | Explícita | Alta      | No                                                                                                      |
| E13    | El bioproceso tiene cuatro fases biológicas: lag, exponencial, estacionaria y muerte                       | "Cultures typically pass through four growth phases. In the lag phase [...] organisms do not multiply or multiply only slowly"                                                                  | SRC-008 / pp. 4–5                   | `ProcessPhase subclasses: LagPhase, ExponentialPhase, StationaryPhase, DeathPhase`                                           | Explícita | Alta      | No                                                                                                      |
| E14    | La inoculación marca el inicio del bioproceso; el inóculo se prepara previamente                           | "inoculation, marks the start of the bioprocess. The inoculum (starter culture) is carefully prepared in advance"                                                                               | SRC-009 / Paso 2                    | `InoculationEvent startsProcess BioprocessRun` ; `InoculationPhase precedes LagPhase`                                        | Explícita | Alta      | No                                                                                                      |
| E15    | Durante el cultivo, temperatura, pH, DO y nutrientes son monitoreados y ajustados continuamente            | "Parameters such as temperature, pH, dissolved oxygen, and nutrient levels are constantly monitored and adjusted"                                                                               | SRC-009 / Paso 3                    | `CultivationPhase isCharacterizedBy Temperature`, `pH`, `DissolvedOxygen`, `NutrientLevel`                                   | Explícita | Alta      | No                                                                                                      |
| E16    | La cosecha ocurre cuando el cultivo alcanza la densidad deseada o la concentración de producto es óptima   | "Once the culture has reached the desired density or the product concentration is optimal, it is time to harvest"                                                                               | SRC-009 / Paso 4                    | `HarvestEvent triggeredBy TargetBiomassCondition` OR `TargetProductConcentration`                                            | Explícita | Alta      | No                                                                                                      |
| E17    | Las fases batch y fed-batch son seguidas por una fase de inducción en producción de proteína recombinante  | "batch and fed-batch phases of fermentation are usually followed by an induction phase, where chemical or thermal induction initiates the expression of a target protein"                       | SRC-010 / Abstract                  | `BatchPhase precedes FedBatchPhase` ; `FedBatchPhase precedes InductionPhase`                                                | Explícita | Alta      | Sí — aplica a procesos microbianos específicos; validar si aplica a los tres biorreactores del proyecto |
| E18    | La fase fed-batch se automatiza con control de DO o pH como señales de retroalimentación                   | "The fed-batch phase is typically automated using predetermined feed profiles, dynamic feedback control based on dissolved oxygen (DO) or pH"                                                   | SRC-010 / Introducción              | `FedBatchPhase isControlledBy DOFeedbackControl` OR `pHFeedbackControl`                                                      | Explícita | Alta      | No                                                                                                      |
| E19    | SOSA define Sensor, Actuator, Observation, Actuation y Result como clases con relaciones análogas          | "An Actuation is performed by an Actuator and yields a Result [...] modelling of actuations is analogous to the modelling of observations"                                                      | SRC-007 / Sección 2.4               | Clases SOSA candidatas: `Sensor`, `Actuator`, `Observation`, `Actuation`, `Result`, `ObservableProperty`                     | Explícita | Alta      | No                                                                                                      |
| E20    | SSN/SOSA usa superclases Execution y System comunes a sensores y actuadores                                | "actuations using actuators are described using essentially the same terminology and relationships [...] with common superclasses Execution and System"                                         | SRC-006 / Introducción              | Alineación candidata: `Sensor` y `Actuator` son subclases de `System` en SSN                                                 | Explícita | Alta      | No                                                                                                      |
| E21    | El software de control regula adición de CO₂, agentes de pH y dispositivos de atemperado                   | "bioprocess control software which regulates the addition of CO2 and liquid pH agents, the activity of tempering devices"                                                                       | SRC-008 / pp. 4–5                   | `ControlSoftware controls CO2Addition`, `pHAgentAddition`, `TemperingDevice`                                                 | Explícita | Media     | Sí — no especifica marca/sistema para los biorreactores del proyecto                                    |
| E22    | BIOSTAT B tiene contacto de alarma potencial-libre en el panel trasero                                     | "potential-free alarm contact are located on the rear panel of the control tower"                                                                                                               | SRC-003 / Descripción producto      | `SartoriusBioreactor hasAlarmContact PotentialFreeAlarmContact`                                                              | Explícita | Alta      | Sí — tipo de eventos activados no especificado en el corpus                                             |
| E23    | La esterilización precede a la inoculación como etapa operativa                                            | "Once the system is sterilized, the desired cells or microorganisms are introduced into the vessel"                                                                                             | SRC-009 / Paso 2                    | `SterilizationPhase precedes InoculationPhase`                                                                               | Inferida  | Alta      | No                                                                                                      |

---

## 4. Conceptos candidatos

| Concepto candidato       | Tipo sugerido                         | Definición basada en corpus                                                                                             | Fuente(s)                 | Estado                                                     |
| ------------------------ | ------------------------------------- | ----------------------------------------------------------------------------------------------------------------------- | ------------------------- | ---------------------------------------------------------- |
| `Bioreactor`             | Clase                                 | Sistema de cultivo microbiano o celular equipado con sensores, actuadores y sistema de control de parámetros de proceso | SRC-003, SRC-005, SRC-009 | Candidato                                                  |
| `BioLectorXT`            | Individuo / Subclase                  | Microbiorreactor de 48 pocillos en formato MTP con sensores ópticos pre-calibrados y módulo microfluidico opcional      | SRC-001                   | Candidato                                                  |
| `SartoriusBioreactor5L`  | Individuo / Subclase                  | Biorreactor BIOSTAT B con volumen de trabajo 0,6–5 L, agitación 20–1500 rpm                                             | SRC-005                   | Candidato                                                  |
| `SartoriusBioreactor10L` | Individuo / Subclase                  | Biorreactor BIOSTAT B con volumen de trabajo 1,5–10 L, agitación 20–800 rpm                                             | SRC-005                   | Candidato                                                  |
| `Sensor`                 | Clase                                 | Dispositivo que mide una propiedad observable del cultivo o del proceso                                                 | SRC-006, SRC-007          | Candidato                                                  |
| `OpticalSensor`          | Subclase de Sensor                    | Sensor que usa módulos LED para medir biomasa, pH, DO o fluorescencia                                                   | SRC-001                   | Candidato                                                  |
| `pHSensor`               | Subclase de Sensor                    | Sensor que mide el pH de la fase líquida del cultivo                                                                    | SRC-001, SRC-005          | Candidato                                                  |
| `DOSensor`               | Subclase de Sensor                    | Sensor que mide el oxígeno disuelto en la fase líquida                                                                  | SRC-001, SRC-005          | Candidato                                                  |
| `OxygenSensor`           | Subclase de Sensor                    | Sensor que mide el nivel de O₂ en la fase gaseosa de la cámara (BioLector XT)                                           | SRC-001                   | Candidato                                                  |
| `TemperatureSensor`      | Subclase de Sensor                    | Sensor que mide la temperatura del medio de cultivo                                                                     | SRC-005                   | Candidato                                                  |
| `FoamSensor`             | Subclase de Sensor                    | Sensor detector de espuma en el biorreactor                                                                             | SRC-005                   | Candidato                                                  |
| `LevelSensor`            | Subclase de Sensor                    | Sensor de nivel de líquido en el biorreactor                                                                            | SRC-005                   | Candidato                                                  |
| `SubstrateSensor`        | Subclase de Sensor                    | Sensor de concentración de sustrato; tipo exacto no especificado en el corpus                                           | SRC-005                   | Candidato — requiere validación                            |
| `BiomassSensor`          | Subclase de Sensor                    | Sensor óptico de dispersión de luz para estimación de biomasa                                                           | SRC-001                   | Candidato                                                  |
| `Actuator`               | Clase                                 | Dispositivo que modifica el estado del proceso en respuesta a una señal de control                                      | SRC-006, SRC-007          | Candidato                                                  |
| `MassFlowController`     | Subclase de Actuator                  | Controlador de flujo másico para regulación de gases (aire, O₂, CO₂, N₂)                                                | SRC-003, SRC-005          | Candidato                                                  |
| `AgitatorMotor`          | Subclase de Actuator                  | Motor que controla la velocidad de agitación del cultivo                                                                | SRC-003, SRC-005          | Candidato                                                  |
| `MicrofluidicModule`     | Subclase de Actuator (o clase propia) | Módulo integrado en la MTP del BioLector XT que controla pH y alimentación por pocillo                                  | SRC-001                   | Candidato — clasificación ambigua                          |
| `GasingModule`           | Subclase de Actuator                  | Módulo de regulación de composición gaseosa (O₂ up/down, CO₂) en BioLector XT                                           | SRC-001                   | Candidato                                                  |
| `TemperingDevice`        | Subclase de Actuator                  | Dispositivo de control de temperatura del cultivo                                                                       | SRC-008                   | Candidato — no especificado por fabricante en el corpus    |
| `OperatingVariable`      | Clase                                 | Parámetro del proceso medible o controlable durante el cultivo                                                          | SRC-003, SRC-005, SRC-009 | Candidato                                                  |
| `pH`                     | Individuo de OperatingVariable        | Concentración de iones hidrógeno del medio de cultivo                                                                   | SRC-001, SRC-005, SRC-009 | Candidato                                                  |
| `DissolvedOxygen`        | Individuo de OperatingVariable        | Concentración de oxígeno disuelto en la fase líquida                                                                    | SRC-001, SRC-005, SRC-010 | Candidato                                                  |
| `Temperature`            | Individuo de OperatingVariable        | Temperatura del medio de cultivo                                                                                        | SRC-005, SRC-009          | Candidato                                                  |
| `AgitationSpeed`         | Individuo de OperatingVariable        | Velocidad de agitación en rpm                                                                                           | SRC-003, SRC-005          | Candidato                                                  |
| `GasFlowRate`            | Individuo de OperatingVariable        | Caudal de gas suministrado al biorreactor                                                                               | SRC-003, SRC-005          | Candidato                                                  |
| `Biomass`                | Individuo de OperatingVariable        | Masa celular en el cultivo, medida ópticamente                                                                          | SRC-001, SRC-010          | Candidato                                                  |
| `NutrientLevel`          | Individuo de OperatingVariable        | Concentración de nutrientes en el medio                                                                                 | SRC-009                   | Candidato                                                  |
| `ProcessPhase`           | Clase                                 | Etapa temporal distinguible dentro del proceso de cultivo                                                               | SRC-008, SRC-009, SRC-010 | Candidato                                                  |
| `SterilizationPhase`     | Subclase de ProcessPhase              | Fase de esterilización previa a la inoculación                                                                          | SRC-009                   | Candidato (inferida)                                       |
| `InoculationPhase`       | Subclase de ProcessPhase              | Fase de introducción del inóculo; marca el inicio del bioproceso                                                        | SRC-009                   | Candidato                                                  |
| `LagPhase`               | Subclase de ProcessPhase              | Fase de adaptación celular sin multiplicación activa                                                                    | SRC-008                   | Candidato                                                  |
| `ExponentialPhase`       | Subclase de ProcessPhase              | Fase de crecimiento rápido de biomasa                                                                                   | SRC-008, SRC-010          | Candidato                                                  |
| `StationaryPhase`        | Subclase de ProcessPhase              | Fase de equilibrio entre crecimiento y muerte celular                                                                   | SRC-008                   | Candidato                                                  |
| `DeathPhase`             | Subclase de ProcessPhase              | Fase de agotamiento de nutrientes y declive celular                                                                     | SRC-008                   | Candidato                                                  |
| `HarvestPhase`           | Subclase de ProcessPhase              | Fase de recuperación del cultivo o producto                                                                             | SRC-009                   | Candidato                                                  |
| `BatchPhase`             | Subclase de ProcessPhase              | Modo de proceso con medio inicial sin adición continua                                                                  | SRC-009, SRC-010          | Candidato                                                  |
| `FedBatchPhase`          | Subclase de ProcessPhase              | Modo de proceso con adición controlada de substrato; controlado por DO o pH                                             | SRC-003, SRC-010          | Candidato                                                  |
| `InductionPhase`         | Subclase de ProcessPhase              | Fase post-fed-batch de inducción de expresión de proteína recombinante                                                  | SRC-010                   | Candidato — validar aplicabilidad a los tres biorreactores |
| `ProcessEvent`           | Clase                                 | Ocurrencia discreta durante el bioproceso                                                                               | SRC-009, SRC-002          | Candidato                                                  |
| `InoculationEvent`       | Subclase de ProcessEvent              | Evento de adición del inóculo al inicio del proceso                                                                     | SRC-009                   | Candidato                                                  |
| `HarvestEvent`           | Subclase de ProcessEvent              | Evento de cosecha activado por condición de biomasa o producto                                                          | SRC-009                   | Candidato                                                  |
| `FeedAdditionEvent`      | Subclase de ProcessEvent              | Evento de adición de substrato en fase fed-batch                                                                        | SRC-003, SRC-010          | Candidato                                                  |
| `AlarmEvent`             | Subclase de ProcessEvent              | Evento de condición anormal detectada durante el proceso                                                                | SRC-002, SRC-003          | Candidato                                                  |
| `LeakageAlarmEvent`      | Subclase de AlarmEvent                | Alarma por flujo de gas superior a 0,5 L/min en reposo en BioLector XT                                                  | SRC-002                   | Candidato                                                  |
| `OptodeDegradationEvent` | Subclase de ProcessEvent              | Evento de degradación de optode por exposición a luz solar                                                              | SRC-002                   | Candidato                                                  |
| `SupervisorySystem`      | Clase                                 | Sistema de software supervisorio conectado al biorreactor para monitoreo y control                                      | SRC-004                   | Candidato                                                  |

---

## 5. Relaciones candidatas con dominio y rango sugeridos

| Relación candidata     | Dominio sugerido    | Rango sugerido      | Significado                                                          | Evidencia (ID ev.)   | Estado                                           |
| ---------------------- | ------------------- | ------------------- | -------------------------------------------------------------------- | -------------------- | ------------------------------------------------ |
| `hasSensor`            | `Bioreactor`        | `Sensor`            | El biorreactor está equipado con el sensor indicado                  | E01, E02, E05        | Candidato                                        |
| `hasActuator`          | `Bioreactor`        | `Actuator`          | El biorreactor está equipado con el actuador indicado                | E07, E08, E04        | Candidato                                        |
| `observes`             | `Sensor`            | `OperatingVariable` | El sensor mide la variable operativa indicada                        | E01, E05 (+ SRC-006) | Candidato — alineación con SOSA `observes`       |
| `controls`             | `Actuator`          | `OperatingVariable` | El actuador regula la variable operativa indicada                    | E08, E04             | Candidato                                        |
| `hasOperatingVariable` | `Bioreactor`        | `OperatingVariable` | El biorreactor opera con la variable de proceso indicada             | E05, E06, E15        | Candidato                                        |
| `hasProcessPhase`      | `Bioreactor`        | `ProcessPhase`      | El biorreactor ejecuta la fase de proceso indicada                   | E09, E13, E15        | Candidato                                        |
| `precedes`             | `ProcessPhase`      | `ProcessPhase`      | Una fase antecede a otra en el tiempo                                | E14, E23, E17        | Candidato                                        |
| `isCharacterizedBy`    | `ProcessPhase`      | `OperatingVariable` | La fase está caracterizada por el comportamiento de la variable      | E15, E18             | Candidato                                        |
| `triggersEvent`        | `ProcessPhase`      | `ProcessEvent`      | Una fase de proceso desencadena el evento indicado                   | E14, E16, E18        | Candidato                                        |
| `hasEvent`             | `Bioreactor`        | `ProcessEvent`      | El biorreactor es el contexto donde ocurre el evento                 | E10, E11, E22        | Candidato                                        |
| `generatesObservation` | `Sensor`            | `Observation`       | El sensor genera una observación con valor y marca de tiempo         | SRC-006, SRC-007     | Candidato — alineación SOSA                      |
| `performsActuation`    | `Actuator`          | `Actuation`         | El actuador realiza una actuación que modifica el proceso            | SRC-007 / E19        | Candidato — alineación SOSA                      |
| `isHostedBy`           | `Sensor`            | `Bioreactor`        | El sensor está alojado en el biorreactor                             | SRC-006              | Candidato — propiedad SSN                        |
| `hasFeedingMode`       | `Bioreactor`        | `FeedingMode`       | El biorreactor opera bajo una estrategia de alimentación definida    | E09                  | Candidato                                        |
| `triggeredBy`          | `AlarmEvent`        | `OperatingVariable` | El evento de alarma es activado por condición anormal de la variable | E10                  | Candidato                                        |
| `connectedTo`          | `Bioreactor`        | `SupervisorySystem` | El biorreactor está conectado a un sistema de supervisión externo    | E12                  | Candidato                                        |
| `regulatedBy`          | `OperatingVariable` | `ControlLoop`       | La variable es regulada por un lazo de control específico            | E08                  | Candidato — ControlLoop no definido en el corpus |

---

## 6. Triadas RDF candidatas

```
# GRUPO A — Biorreactor → Sensor

BioLectorXT -> hasSensor -> BiomassSensor
Fuente: SRC-001 | Estado: Soportada

BioLectorXT -> hasSensor -> pHSensor
Fuente: SRC-001 | Estado: Soportada

BioLectorXT -> hasSensor -> DOSensor
Fuente: SRC-001 | Estado: Soportada

BioLectorXT -> hasSensor -> OxygenSensor
Fuente: SRC-001 (módulo O₂) | Estado: Soportada

SartoriusBioreactor5L -> hasSensor -> pHSensor
Fuente: SRC-005 | Estado: Soportada

SartoriusBioreactor5L -> hasSensor -> DOSensor
Fuente: SRC-005 | Estado: Soportada

SartoriusBioreactor5L -> hasSensor -> TemperatureSensor
Fuente: SRC-005 | Estado: Soportada

SartoriusBioreactor5L -> hasSensor -> FoamSensor
Fuente: SRC-005 | Estado: Soportada

SartoriusBioreactor5L -> hasSensor -> LevelSensor
Fuente: SRC-005 | Estado: Soportada

SartoriusBioreactor5L -> hasSensor -> SubstrateSensor
Fuente: SRC-005 | Estado: Soportada — tipo exacto requiere validación

SartoriusBioreactor10L -> hasSensor -> pHSensor
Fuente: SRC-005 | Estado: Soportada

SartoriusBioreactor10L -> hasSensor -> DOSensor
Fuente: SRC-005 | Estado: Soportada

SartoriusBioreactor10L -> hasSensor -> TemperatureSensor
Fuente: SRC-005 | Estado: Soportada

SartoriusBioreactor10L -> hasSensor -> FoamSensor
Fuente: SRC-005 | Estado: Soportada

SartoriusBioreactor10L -> hasSensor -> LevelSensor
Fuente: SRC-005 | Estado: Soportada

# GRUPO B — Sensor → Variable observable

pHSensor -> observes -> pH
Fuente: SRC-001, SRC-005, SRC-006 | Estado: Soportada

DOSensor -> observes -> DissolvedOxygen
Fuente: SRC-001, SRC-005, SRC-006 | Estado: Soportada

BiomassSensor -> observes -> Biomass
Fuente: SRC-001, SRC-006 | Estado: Soportada

TemperatureSensor -> observes -> Temperature
Fuente: SRC-005 | Estado: Soportada

FoamSensor -> observes -> FoamLevel
Fuente: SRC-005 | Estado: Soportada

OxygenSensor -> observes -> GasPhaseoxygenLevel
Fuente: SRC-001 | Estado: Soportada

# GRUPO C — Biorreactor → Actuador

BioLectorXT -> hasActuator -> GasingModule
Fuente: SRC-001 (módulos O₂ up/down) | Estado: Soportada

BioLectorXT -> hasActuator -> MicrofluidicModule
Fuente: SRC-001 | Estado: Soportada — clasificación como actuador requiere validación

SartoriusBioreactor5L -> hasActuator -> MassFlowController
Fuente: SRC-003, SRC-005 | Estado: Soportada

SartoriusBioreactor5L -> hasActuator -> AgitatorMotor
Fuente: SRC-003, SRC-005 | Estado: Soportada

SartoriusBioreactor10L -> hasActuator -> MassFlowController
Fuente: SRC-003, SRC-005 | Estado: Soportada

SartoriusBioreactor10L -> hasActuator -> AgitatorMotor
Fuente: SRC-005 | Estado: Soportada

# GRUPO D — Actuador → Variable controlada

MassFlowController -> controls -> GasFlowRate
Fuente: SRC-003, SRC-005 | Estado: Soportada

AgitatorMotor -> controls -> AgitationSpeed
Fuente: SRC-003, SRC-005 | Estado: Soportada

MicrofluidicModule -> controls -> pH
Fuente: SRC-001 | Estado: Soportada

MicrofluidicModule -> controls -> FeedAddition
Fuente: SRC-001 | Estado: Soportada

GasingModule -> controls -> OxygenLevel
Fuente: SRC-001 | Estado: Soportada

# GRUPO E — Biorreactor → Modo de proceso

SartoriusBioreactor5L -> hasFeedingMode -> BatchMode
Fuente: SRC-003 | Estado: Soportada

SartoriusBioreactor5L -> hasFeedingMode -> FedBatchMode
Fuente: SRC-003 | Estado: Soportada

SartoriusBioreactor5L -> hasFeedingMode -> ContinuousMode
Fuente: SRC-003 | Estado: Soportada

SartoriusBioreactor5L -> hasFeedingMode -> PerfusionMode
Fuente: SRC-003 | Estado: Soportada

BioLectorXT -> hasFeedingMode -> FedBatchMode
Fuente: SRC-001 | Estado: Soportada

# GRUPO F — Fases del proceso (secuencia)

SterilizationPhase -> precedes -> InoculationPhase
Fuente: SRC-009 | Estado: Parcialmente soportada (inferida de descripción secuencial)

InoculationPhase -> precedes -> LagPhase
Fuente: SRC-008, SRC-009 | Estado: Parcialmente soportada

LagPhase -> precedes -> ExponentialPhase
Fuente: SRC-008 | Estado: Soportada

ExponentialPhase -> precedes -> StationaryPhase
Fuente: SRC-008 | Estado: Soportada

StationaryPhase -> precedes -> HarvestPhase
Fuente: SRC-008, SRC-009 | Estado: Parcialmente soportada

BatchPhase -> precedes -> FedBatchPhase
Fuente: SRC-010 | Estado: Soportada

FedBatchPhase -> precedes -> InductionPhase
Fuente: SRC-010 | Estado: Soportada — aplicabilidad a los tres biorreactores requiere validación

# GRUPO G — Fases → Variables características

ExponentialPhase -> isCharacterizedBy -> Biomass
Fuente: SRC-008 | Estado: Parcialmente soportada (inferida del texto)

CultivationPhase -> isCharacterizedBy -> pH
Fuente: SRC-009 | Estado: Soportada

CultivationPhase -> isCharacterizedBy -> DissolvedOxygen
Fuente: SRC-009, SRC-010 | Estado: Soportada

CultivationPhase -> isCharacterizedBy -> Temperature
Fuente: SRC-009 | Estado: Soportada

FedBatchPhase -> isCharacterizedBy -> DissolvedOxygen
Fuente: SRC-003, SRC-010 | Estado: Soportada

FedBatchPhase -> isCharacterizedBy -> pH
Fuente: SRC-010 | Estado: Soportada

# GRUPO H — Fases / Biorreactores → Eventos

InoculationPhase -> triggersEvent -> InoculationEvent
Fuente: SRC-009 | Estado: Soportada

HarvestPhase -> triggersEvent -> HarvestEvent
Fuente: SRC-009 | Estado: Soportada

FedBatchPhase -> triggersEvent -> FeedAdditionEvent
Fuente: SRC-003, SRC-010 | Estado: Soportada

BioLectorXT -> hasEvent -> LeakageAlarmEvent
Fuente: SRC-002 | Estado: Soportada

BioLectorXT -> hasEvent -> OptodeDegradationEvent
Fuente: SRC-002 | Estado: Soportada

SartoriusBioreactor5L -> hasEvent -> AlarmEvent
Fuente: SRC-003 (contacto de alarma) | Estado: Parcialmente soportada — tipo de eventos no especificado

# GRUPO I — Alineación SOSA/SSN

Sensor -> rdf:type -> sosa:Sensor
Fuente: SRC-006, SRC-007 | Estado: Soportada

Actuator -> rdf:type -> sosa:Actuator
Fuente: SRC-006, SRC-007 | Estado: Soportada

Observation -> rdf:type -> sosa:Observation
Fuente: SRC-006 | Estado: Soportada

Actuation -> rdf:type -> sosa:Actuation
Fuente: SRC-007 | Estado: Soportada

Bioreactor -> rdf:type -> sosa:Platform
Fuente: SRC-006 (inferida — Platform como host de sensores) | Estado: Parcialmente soportada — requiere validación
```

---

## 7. Sinónimos documentados

| Término principal    | Sinónimos en el corpus                                                 | Idioma | Fuente                             |
| -------------------- | ---------------------------------------------------------------------- | ------ | ---------------------------------- |
| `DissolvedOxygen`    | DO, pO₂, dissolved O₂, oxygen concentration                            | Inglés | SRC-001, SRC-003, SRC-005, SRC-010 |
| `pH`                 | acid-base, hydrogen ion concentration, pH set point                    | Inglés | SRC-001, SRC-003, SRC-005, SRC-009 |
| `AgitationSpeed`     | stirrer speed, RPM, mixing speed                                       | Inglés | SRC-003, SRC-005                   |
| `GasFlowRate`        | flow rate, total gas flow, aeration rate                               | Inglés | SRC-003, SRC-005                   |
| `MassFlowController` | MFC, mass flow controller, gas flow controller                         | Inglés | SRC-003, SRC-005                   |
| `InoculationPhase`   | inoculation step, inoculum addition, seeding                           | Inglés | SRC-009                            |
| `FedBatchPhase`      | fed-batch mode, fed-batch phase, feeding phase                         | Inglés | SRC-003, SRC-009, SRC-010          |
| `HarvestPhase`       | harvesting, cell harvest, harvest step                                 | Inglés | SRC-009                            |
| `BiomassSensor`      | optical sensor (biomass), backscatter sensor, turbidity sensor         | Inglés | SRC-001                            |
| `OpticalSensor`      | optode, fluorescence sensor, LED filter module                         | Inglés | SRC-001, SRC-002                   |
| `Bioreactor`         | fermenter, fermentor, fermentation vessel, cultivation vessel          | Inglés | SRC-003, SRC-004, SRC-009          |
| `FoamSensor`         | foam detector, antifoam sensor                                         | Inglés | SRC-005                            |
| `GasingModule`       | O₂ up-regulation module, O₂ down-regulation module, gas control module | Inglés | SRC-001                            |
| `SupervisorySystem`  | supervisory software, SCADA, Biobrain®, DeltaV™, MFCS                  | Inglés | SRC-004                            |
| `InductionPhase`     | induction step, expression phase, chemical/thermal induction           | Inglés | SRC-010                            |

---

## 8. Vacíos del corpus

| N°  | Vacío identificado                                                                                                                                                                                              | Impacto ontológico                                                                                                     | Fuente que podría resolverlo                                                                        |
| --- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- |
| V01 | El tipo exacto del `SubstrateSensor` en BIOSTAT B no está especificado (¿electroquímico, gravimétrico, espectroscópico?)                                                                                        | La subclase y sus propiedades no pueden definirse sin esta información                                                 | Manual técnico oficial BIOSTAT B (Sartorius)                                                        |
| V02 | El corpus no documenta qué eventos de alarma específicos activa el contacto potencial-libre del BIOSTAT B                                                                                                       | La triada `SartoriusBioreactor hasEvent AlarmEvent` queda sin tipo concreto                                            | Manual técnico BIOSTAT B / SOP de laboratorio                                                       |
| V03 | El módulo microfluidico del BioLector XT actúa simultáneamente como sensor de retroalimentación y como actuador; su clasificación ontológica es ambigua                                                         | Requiere decisión de diseño: ¿clase propia, doble rol, o composición de clases?                                        | Consulta con experto de ontología + manual BioLector XT completo                                    |
| V04 | No se especifica en el corpus si las fases biológicas (lag, exponencial, estacionaria) son detectadas y registradas automáticamente como estados discretos por el software de control de los tres biorreactores | Determina si `ProcessPhase` puede ser una clase de estado en el sistema de control o solo una clasificación conceptual | Software BioLection (m2p-labs) y MFCS/BioPAT (Sartorius) — documentación no disponible en el corpus |
| V05 | La `InductionPhase` (SRC-010) está documentada para procesos microbianos de proteína recombinante; no se verifica si aplica a los procesos específicos de los tres biorreactores del proyecto                   | Podría resultar en una subclase inaplicable o una instancia incorrecta en la ontología                                 | SOP del laboratorio usuario                                                                         |
| V06 | El corpus no describe relaciones entre el `BioLectorXT` y el software BioLection más allá de la configuración de perfiles de fed-batch                                                                          | No se puede modelar la arquitectura completa de adquisición de datos y control de eventos                              | Manual completo BioLector XT / documentación BioLection                                             |
| V07 | No se documenta la relación entre `ControlSoftware` (SRC-008) y los biorreactores específicos del proyecto                                                                                                      | La cadena `Bioreactor → hasControlSystem → ControlSoftware` no puede instanciarse                                      | Documentación de software de fabricantes                                                            |
| V08 | El corpus no especifica si el BIOSTAT B 10L usa MFC o medidor de área variable para N₂ de forma estándar o configurable                                                                                         | Determina si `hasActuator MassFlowController` aplica universalmente para N₂                                            | Manual técnico BIOSTAT B completo                                                                   |
| V09 | No hay evidencia en el corpus sobre cómo se registran las fases de proceso en el modelo de datos temporal                                                                                                       | No se puede modelar la relación `ProcessPhase hasTimeInterval Interval`                                                | Publicaciones sobre modelos de datos de bioprocesos; estándar ISO 11179 o ISA-88                    |
| V10 | La relación `Bioreactor -> rdf:type -> sosa:Platform` es una inferencia razonable pero no está explícitamente validada en el corpus                                                                             | La alineación con SSN/SOSA queda parcialmente sin soporte para este dominio                                            | Revisión directa de la especificación SSN/SOSA + decisión del grupo de ontología                    |

---

## 9. Estado final

| Dimensión                                         | Estado                                                                                                                                                              | Justificación                                                                                                                                                                                                                        |
| ------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **Respuesta a la pregunta**                       | **Parcialmente soportada**                                                                                                                                          | Las relaciones centrales (sensor, actuador, variable, fase, evento) están documentadas para los tres biorreactores; quedan vacíos en tipificación de alarmas, clasificación del módulo microfluidico y detección automática de fases |
| **Triadas del grupo A–D** (sensores y actuadores) | **Soportadas**                                                                                                                                                      | Evidencia explícita en SRC-001, SRC-003, SRC-005                                                                                                                                                                                     |
| **Triadas del grupo E–G** (fases y variables)     | **Parcialmente soportadas**                                                                                                                                         | Fases biológicas y operativas documentadas; vínculos fase→variable inferidos en algunos casos                                                                                                                                        |
| **Triadas del grupo H** (eventos)                 | **Parcialmente soportadas**                                                                                                                                         | InoculationEvent y HarvestEvent soportados; AlarmEvents del BIOSTAT B insuficientemente especificados                                                                                                                                |
| **Triadas del grupo I** (alineación SOSA)         | **Parcialmente soportadas**                                                                                                                                         | Clases SOSA confirmadas; alineación `Bioreactor = sosa:Platform` es inferida, no explícita                                                                                                                                           |
| **Corpus**                                        | **Parcial**                                                                                                                                                         | Suficiente para el esquema relacional básico; faltan manuales completos de fabricante y SOPs de laboratorio                                                                                                                          |
| **Próxima acción**                                | Obtener manual técnico completo BIOSTAT B y BioLector XT; consultar experto para clasificar módulo microfluidico y validar alcance de InductionPhase en el proyecto | —                                                                                                                                                                                                                                    |
