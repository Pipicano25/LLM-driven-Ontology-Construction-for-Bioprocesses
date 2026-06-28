**Extracción condicionada por corpus – ALC-05**

### 1) ID y pregunta

**ALC-05:** ¿Cómo se separan ontológicamente el equipo físico, el proceso biológico, el sistema de control, las variables medidas y los datos generados?

### 2) Respuesta basada en evidencia

Trabajando únicamente con los fragmentos:

**Equipo físico:** el corpus describe artefactos tangibles. SRC-002 documenta "culture vessel" con volúmenes "1 L, 2 L, 5 L and 10 L" y "control tower" que "contains both the aeration, pump and temperature control modules". SRC-001 añade un volumen de trabajo "Filling volume: 800 – 1900 μL". SRC-005 nombra la clase "Vessel".

**Proceso biológico:** SRC-006 define explícitamente: "The bioprocess, generally associated with cultivation in appropriate bioreactors (fermenters), includes the cultivation of the living biocatalyst to a high density". SRC-002 menciona "your culture", SRC-004 menciona evaluación de "biomass".

**Sistema de control:** el corpus distingue componentes de regulación. SRC-002: "Control the pH of your culture by automatic acid and base addition" y "advanced DO controller". SRC-003: "Setting the 'P', 'I', or 'D' Controller Parameters". SRC-001: "Fully editable PI control". SRC-005 tipifica "Control Protocol data: deadband (int), duration (ind), setpoint (int)".

**Variables medidas:** SRC-001 lista "0 – 100 % dissolved oxygen", "pH 4 – 7.5", "10 – 50 °C", "100 – 1500 rpm". SRC-004 lista "biomass, pH, dissolved oxygen (DO), fluorescence". SRC-006 generaliza: "physical (temperature, weight, pressure, conductivity, gas and liquid flow, foam level, stirrer speed and power) and chemical measurements (pH, pO2".

**Datos generados:** SRC-002: "BioPAT® MFCS is a 'plugandplay' solution, ideally suited for capturing, storing and visualizing process data". SRC-004: "Continuous monitoring improves reproducibility".

> No establecido en el corpus suministrado: una definición formal que declare estas cinco categorías como clases disjuntas en OWL.

### 3) Tabla de afirmaciones y evidencia

| #   | Afirmación                                                             | Fragmento de evidencia                                                                                                                                                | Fuente            | Concepto/relación/triada candidata                    | Tipo      | Confianza | Validación experta |
| --- | ---------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------- | ----------------------------------------------------- | --------- | --------- | ------------------ |
| A1  | Existe un vaso de cultivo con volúmenes 1-10 L                         | > Our proven autoclavable borosilicate glass culture vessel is available in four different volumes: 1 L, 2 L, 5 L and 10 L                                            | SRC-002, brochure | BioreactorVessel – hasVolume                          | explícita | alta      | no                 |
| A2  | La torre de control contiene módulos de aireación, bomba y temperatura | > The control tower contains both the aeration, pump and temperature control modules                                                                                  | SRC-002           | ControlTower – contains – Module                      | explícita | alta      | no                 |
| A3  | El bioproceso se asocia a cultivo en biorreactor                       | > The bioprocess, generally associated with cultivation in appropriate bioreactors (fermenters), includes the cultivation of the living biocatalyst to a high density | SRC-006           | Bioprocess – associatedWith – Cultivation             | explícita | alta      | no                 |
| A4  | El sistema controla pH automáticamente                                 | > Control the pH of your culture by automatic acid and base addition or by CO₂ aeration and base addition                                                             | SRC-002           | ControlSystem – controls – pH                         | explícita | alta      | no                 |
| A5  | Existe un controlador DO avanzado                                      | > Besides classic DO cascade control, we have developed the unique advanced DO controller                                                                             | SRC-002           | DOController – rdf:type – Controller                  | explícita | alta      | no                 |
| A6  | Los controladores usan parámetros P, I, D                              | > Setting the "P", "I", or "D" Controller Parameters:                                                                                                                 | SRC-003           | PIDController – hasParameter – {P,I,D}                | explícita | alta      | no                 |
| A7  | Existe control PI editable                                             | > Fully editable PI control                                                                                                                                           | SRC-001           | PIControl – rdf:type – ControlAlgorithm               | explícita | media     | sí                 |
| A8  | Variable medida: oxígeno disuelto 0-100%                               | > 0 – 100 % dissolved oxygen\*1                                                                                                                                       | SRC-001           | DissolvedOxygen – rdf:type – MeasuredVariable         | explícita | alta      | no                 |
| A9  | Variable medida: pH 4-7.5                                              | > pH 4 – 7.5 (depending on plate)                                                                                                                                     | SRC-001           | pH – rdf:type – MeasuredVariable                      | explícita | alta      | no                 |
| A10 | Variable medida: temperatura 10-50°C                                   | > 10 – 50 °C (min. temp.: 8 °C below ambient temp.)                                                                                                                   | SRC-001           | Temperature – rdf:type – MeasuredVariable             | explícita | alta      | no                 |
| A11 | Variable medida: agitación 100-1500 rpm                                | > 100 – 1500 rpm (3 mm diameter)                                                                                                                                      | SRC-001           | StirrerSpeed – rdf:type – MeasuredVariable            | explícita | alta      | no                 |
| A12 | Variables evaluadas: biomasa, pH, DO, fluorescencia                    | > rapidly evaluate biomass, pH, dissolved oxygen (DO), fluorescence                                                                                                   | SRC-004           | System – evaluates – {Biomass, pH, DO, Fluorescence}  | explícita | alta      | no                 |
| A13 | Mediciones básicas físicas y químicas                                  | > physical (temperature, weight, pressure, conductivity, gas and liquid flow, foam level, stirrer speed and power) and chemical measurements (pH, pO2                 | SRC-006           | MeasuredVariable – includes – Physical/Chemical       | explícita | alta      | no                 |
| A14 | Los datos de proceso se capturan y visualizan                          | > BioPAT® MFCS is a "plugandplay" solution, ideally suited for capturing, storing and visualizing process data                                                        | SRC-002           | MFCS – captures – ProcessData                         | explícita | alta      | no                 |
| A15 | El monitoreo es continuo                                               | > Continuous monitoring improves reproducibility and reduces human error.                                                                                             | SRC-004           | Monitoring – hasQuality – Continuous                  | explícita | media     | no                 |
| A16 | Vessel tiene dato volume                                               | > Vessel data: volume (str)                                                                                                                                           | SRC-005           | Vessel – hasDataProperty – volume                     | explícita | alta      | no                 |
| A17 | Control Protocol tiene deadband, duration, setpoint                    | > Control Protocol data: deadband (int), duration (ind), setpoint (int)                                                                                               | SRC-005           | ControlProtocol – hasParameter – {deadband, setpoint} | explícita | alta      | no                 |
| A18 | Volumen de trabajo microescala 800-1900 µL                             | > Filling volume: 800 – 1900 μL (rpm dependent)                                                                                                                       | SRC-001           | MicroVessel – hasWorkingVolume                        | explícita | alta      | no                 |

### 4) Conceptos candidatos

- **PhysicalEquipment** (inferido de "control tower", "vessel")
- **BioreactorVessel** – de SRC-005 "Vessel"
- **ControlTower** – de SRC-002
- **Module** (AerationModule, PumpModule, TemperatureControlModule) – de SRC-002
- **Bioprocess** – de SRC-006
- **Culture** – de SRC-002 "your culture"
- **ControlSystem** – inferido de controladores
- **Controller** (PIDController, DOController, PIControl) – de SRC-002, SRC-003, SRC-001
- **ControlProtocol** – de SRC-005
- **MeasuredVariable** (pH, DissolvedOxygen/DO, Temperature, StirrerSpeed, Biomass, Fluorescence, pO2) – de SRC-001, SRC-004, SRC-006
- **ProcessData** – de SRC-002

### 5) Relaciones candidatas con dominio y rango sugeridos

| Relación         | Dominio sugerido | Rango sugerido   | Evidencia |
| ---------------- | ---------------- | ---------------- | --------- |
| contains         | ControlTower     | Module           | SRC-002   |
| hasVolume        | Vessel           | xsd:string       | SRC-005   |
| controls         | ControlSystem    | pH               | SRC-002   |
| hasParameter     | Controller       | {P,I,D}          | SRC-003   |
| implements       | System           | PIControl        | SRC-001   |
| evaluates        | System           | MeasuredVariable | SRC-004   |
| captures         | MFCS             | ProcessData      | SRC-002   |
| associatedWith   | Bioprocess       | Cultivation      | SRC-006   |
| hasWorkingVolume | Vessel           | xsd:string       | SRC-001   |

### 6) Triadas RDF candidatas

- **ControlTower -> contains -> AerationModule** – SRC-002 – explícita
- **CultureVessel -> hasVolume -> "1 L, 2 L, 5 L and 10 L"** – SRC-002 – explícita
- **Bioprocess -> associatedWith -> CultivationInBioreactor** – SRC-006 – explícita
- **PIDController -> hasParameter -> "P"** – SRC-003 – explícita
- **AdvancedDOController -> rdf:type -> Controller** – SRC-002 – inferida
- **BioPAT_MFCS -> captures -> ProcessData** – SRC-002 – explícita
- **System -> evaluates -> DissolvedOxygen** – SRC-004 – explícita
- **ControlProtocol -> hasSetpoint -> xsd:int** – SRC-005 – explícita

### 7) Sinónimos documentados

| Término          | Variante                              | Fuente                              |
| ---------------- | ------------------------------------- | ----------------------------------- |
| dissolved oxygen | DO                                    | SRC-004: "dissolved oxygen (DO)"    |
| bioreactors      | fermenters                            | SRC-006: "bioreactors (fermenters)" |
| process data     | data (en "capturing... process data") | SRC-002                             |

### 8) Vacíos del corpus

- No establecido en el corpus suministrado: definición ontológica formal que separe "equipo físico" de "sistema de control" como clases disjuntas.
- No establecido: relación explícita entre "variables medidas" y "datos generados" más allá de "capturing".
- No establecido: si "Culture" es subclase de "Bioprocess" o entidad separada.
- No establecido: equivalencia entre pO2 (SRC-006) y dissolved oxygen (SRC-001); solo co-ocurren.
- No establecido: jerarquía entre PI control y PID controller.

### 9) Estado final

**Parcialmente soportado.** El corpus permite identificar y separar con evidencia explícita los cinco dominios mediante fragmentos de equipos, cultivo, controladores, variables y datos, pero no proporciona axiomas OWL ni definiciones de disyunción. Se requiere validación experta para formalizar las clases y propiedades.
