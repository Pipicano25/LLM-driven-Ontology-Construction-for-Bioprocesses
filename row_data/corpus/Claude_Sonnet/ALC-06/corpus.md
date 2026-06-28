# Extracción ontológica condicionada por corpus — ALC-06

---

## 1. ID y pregunta

**ID:** ALC-06
**Pregunta:** ¿Qué propiedades generales deben describir cualquier biorreactor del proyecto, independientemente de su escala o volumen?

---

## 2. Respuesta basada en evidencia

A partir exclusivamente de los fragmentos documentales suministrados, las propiedades generales que deben describir cualquier biorreactor del proyecto se organizan en ocho categorías verificables:

**A. Identificación del sistema**
Todo biorreactor posee un nombre de modelo y una entidad fabricante identificables. [SRC-001] identifica "BioLector XT" y "m2p-labs GmbH / Beckman Coulter, Inc." [SRC-002] identifica "BIOSTAT® Bplus" y "Sartorius Stedim Biotech".

**B. Volumen**
Todo biorreactor expone un volumen operativo. [SRC-001] lo denomina _filling volume_ (800–2.400 µL según placa y rpm). [SRC-002] lo denomina _working volume_ (0,6–5 L para el vaso de 5 L; 1,5–10 L para el de 10 L) y adicionalmente un _total volume_ (6,6 L y 13 L respectivamente).

**C. Temperatura**
Propiedad operativa medida y controlada en ambos sistemas. [SRC-001]: 10–50 °C. [SRC-002]: medición 0–150 °C; control 8 °C sobre agua de enfriamiento hasta 60 °C. [SRC-003] la incluye como parámetro de mantenimiento obligatorio. [SRC-004] la clasifica como parámetro físico.

**D. pH**
Medido y controlado en ambos sistemas mediante tecnologías distintas. [SRC-001]: optodo óptico, rango 4,0–7,5. [SRC-002]: electrodo de gel, rango 2–12. [SRC-003]: parámetro de mantenimiento. [SRC-004]: parámetro químico.

**E. Oxígeno disuelto (DO / pO₂)**
[SRC-001]: optodo óptico, 0–100 % saturación O₂. [SRC-002]: electrodo polarográfico, 0–100 %. [SRC-003] y [SRC-004]: incluido en parámetros monitoreados obligatoriamente.

**F. Agitación / mezcla**
[SRC-001]: agitación orbital 100–1.500 rpm (diámetro 3 mm). [SRC-002]: agitación mecánica 20–800 rpm (10 L) a 20–2.000 rpm (1 L y 2 L). [SRC-003] y [SRC-004]: agitation rate/speed como parámetro físico universal.

**G. Composición del gas de entrada**
[SRC-001]: O₂ 1–100 %, CO₂ 0–12 % (módulos opcionales), N₂ para anaerobiosis. [SRC-002]: mezcla de cuatro gases — Aire, O₂, N₂, CO₂ — para sparger; Aire para overlay. [SRC-003]: "flow rates of gas (air, oxygen, nitrogen, carbon dioxide)". [SRC-004]: "gas concentration like dissolved oxygen (DO)".

**H. Modo de operación del cultivo**
[SRC-001]: batch, fed-batch, bolus, continuo (estrategias de alimentación). [SRC-002]: "Batch, fed batch and continuous culture / Perfusion operation". [SRC-003]: "batch, fed batch, or continuous".

**Propiedades adicionales documentadas en uno o ambos sistemas:**

- Tipo y desechabilidad del vaso: [SRC-001] tecnología desechable (disposable); [SRC-002] vaso de vidrio reutilizable (multi-use).
- Sistema de control en lazo cerrado con set-point: [SRC-001] "closed loop controller" para pH; [SRC-002] "integrated digital control loops for Temperature, pH, DO, agitation".
- Tipo de sensor: [SRC-001] sensores ópticos pre-calibrados (optodos); [SRC-002] polarográfico (pO₂), gel (pH), Pt100 (temperatura).
- Protocolo de comunicación: [SRC-001] Ethernet; [SRC-002] Ethernet, RS422, RS232.
- Presión del gas suministrado: [SRC-002] "Gasses: Controlled @ 1.5 barg dry, particle and oil-free".
- Espuma y nivel: [SRC-002] amplificadores de Foam y Level integrados; no establecido en [SRC-001].
- Turbidez y Redox: [SRC-002] opcionales; no establecido en [SRC-001].

---

## 3. Tabla de afirmaciones y evidencia

| ID ev | Afirmación                                                                                                          | Fragmento de evidencia                                                                                                                                                                         | Fuente / sección                                                                               | Concepto/relación/triada candidata                                                     | Tipo      | Confianza | Validación experta |
| ----- | ------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- | --------- | --------- | ------------------ |
| EV-01 | Todo biorreactor del proyecto tiene un nombre de modelo identificable                                               | "BioLector XT Microbioreactor" / "BIOSTAT® Bplus"                                                                                                                                              | SRC-001 encabezado; SRC-002 encabezado                                                         | `Bioreactor` → `hasModelName` → xsd:string                                             | Explícita | Alta      | No                 |
| EV-02 | Todo biorreactor del proyecto tiene una entidad fabricante identificable                                            | "m2p-labs GmbH / Beckman Coulter" / "Sartorius Stedim Biotech"                                                                                                                                 | SRC-001 pie de página; SRC-002 encabezado                                                      | `Bioreactor` → `hasManufacturer` → `Manufacturer`                                      | Explícita | Alta      | No                 |
| EV-03 | Todo biorreactor expone un volumen operativo nominal                                                                | "Filling volume: 800–1900 μL (rpm dependent)" / "Working volume: 0.6–5 / 1.5–10 [L]"                                                                                                           | SRC-001 MICROTITER PLATES; SRC-002 Culture Vessel                                              | `Bioreactor` → `hasWorkingVolume` → xsd:float                                          | Explícita | Alta      | No                 |
| EV-04 | El BIOSTAT® Bplus expone adicionalmente un volumen total del vaso                                                   | "Total volume 1 L\|2 L\|5 L\|10 L: 1.6\|3\|6.6\|13 [L]"                                                                                                                                        | SRC-002 Culture Vessel                                                                         | `Bioreactor` → `hasTotalVolume` → xsd:float                                            | Explícita | Alta      | No                 |
| EV-05 | La temperatura es propiedad operativa medida y controlada en todo biorreactor del proyecto                          | "TEMPERATURE: 10–50 °C" / "Temperature: 0–150°C" / "temperature, pH, foam control, and agitation rate"                                                                                         | SRC-001 CULTIVATION CONDITIONS; SRC-002 Measurement Ranges; SRC-003 párr. 1                    | `Bioreactor` → `hasTemperatureRange` → `TemperatureRange`                              | Explícita | Alta      | No                 |
| EV-06 | El pH es propiedad operativa medida y controlada en todo biorreactor del proyecto                                   | "pH OPTODES: pH 4–7.5" / "pH: 2–12" / parámetro de mantenimiento                                                                                                                               | SRC-001 pH OPTODES; SRC-002 Measurement Ranges; SRC-003 párr. 1; SRC-004 grupo (2)             | `Bioreactor` → `haspHRange` → `pHRange`                                                | Explícita | Alta      | No                 |
| EV-07 | El pH se controla en lazo cerrado con set-point configurable                                                        | "Triggered pH control (closed loop controller)" / "Integrated digital control loops for … pH"                                                                                                  | SRC-001 MICROFLUIDIC FEATURES; SRC-002 Digital Controller                                      | `ControlLoop` → `controlsParameter` → `pH`                                             | Explícita | Alta      | No                 |
| EV-08 | El oxígeno disuelto (DO/pO₂) es propiedad medida en todo biorreactor del proyecto                                   | "OXYGEN OPTODES: 0–100 % dissolved oxygen" / "pO2: 0–100%" / "dissolved oxygen levels"                                                                                                         | SRC-001 OXYGEN OPTODES; SRC-002 Measurement Ranges; SRC-003 párr. 3; SRC-004 grupo (2)         | `Bioreactor` → `hasDORange` → `DORange`                                                | Explícita | Alta      | No                 |
| EV-09 | La velocidad de agitación/mezcla es propiedad operativa de todo biorreactor del proyecto                            | "SHAKING SPEED: 100–1500 rpm (3 mm diameter)" / "Agitation motor speed … 20–800 rpm"                                                                                                           | SRC-001 CULTIVATION CONDITIONS; SRC-002 Measurement Ranges; SRC-003 párr. 3; SRC-004 grupo (1) | `Bioreactor` → `hasAgitationSpeedRange` → `AgitationSpeedRange`                        | Explícita | Alta      | No                 |
| EV-10 | La temperatura se controla con sistema de calefacción y enfriamiento activos                                        | "Dry heating system via heating blanket and automatic cooling water control valve / Temperature control range: 8°C above cooling water to 60°C"                                                | SRC-002 Temperature Control System                                                             | `Bioreactor` → `hasControlLoop` → `TemperatureControlLoop`                             | Explícita | Alta      | No                 |
| EV-11 | La composición del gas de entrada (O₂, CO₂, N₂, aire) es propiedad operable de todo biorreactor                     | "1–100 % O2 (optional) / 0–12 % CO2 (optional)" / "Gas mixing of Air, O2, N2, CO2 for Sparger" / "flow rates of gas (air, oxygen, nitrogen, carbon dioxide)"                                   | SRC-001 ENVIRONMENTAL CONDITIONS y módulos; SRC-002 Gassing System; SRC-003 párr. 3            | `Bioreactor` → `hasGasComposition` → `GasComposition`                                  | Explícita | Alta      | No                 |
| EV-12 | El modo de operación del cultivo es propiedad clasificatoria de todo biorreactor del proyecto                       | "batch, fed-batch, bolus, continuous" / "Batch, fed batch and continuous culture / Perfusion operation" / "batch, fed batch, or continuous"                                                    | SRC-001 FEEDING PROFILES; SRC-002 Applicable for; SRC-003 clasificación                        | `Bioreactor` → `hasOperationMode` → `OperationMode`                                    | Explícita | Alta      | No                 |
| EV-13 | Los biorreactores del proyecto difieren en tecnología de vaso: desechable vs. reutilizable                          | "Application mode: Disposable technology" / "Multi-Use Bioreactors … Single wall glass vessel"                                                                                                 | SRC-001 LAB SPACE; SRC-002 encabezado y Culture Vessel                                         | `Bioreactor` → `hasDisposabilityClass` → `DisposabilityClass`                          | Explícita | Alta      | No                 |
| EV-14 | El BioLector XT usa sensores ópticos pre-calibrados (optodos) para pH y DO                                          | "operates with online, pre-calibrated optical sensors" / "OXYGEN OPTODES" / "pH OPTODES"                                                                                                       | SRC-001 OXYGEN OPTODES; SRC-001 pH OPTODES                                                     | `SensorSystem` → `hasSensorTechnology` → `OpticalSensor`                               | Explícita | Alta      | No                 |
| EV-15 | El BIOSTAT® Bplus usa sensores electroquímicos y resistivos para pO₂, pH y temperatura                              | "pO2 electrode: Polarographic / pH electrode: Gel-filled / Temperature probe: Pt 100"                                                                                                          | SRC-002 Culture Vessel                                                                         | `SensorSystem` → `hasSensorTechnology` → `ElectrochemicalSensor` / `ResistiveSensor`   | Explícita | Alta      | No                 |
| EV-16 | El protocolo de comunicación con sistemas externos es una propiedad de todo biorreactor del proyecto                | "Interface: Ethernet" / "Host communication: Ethernet \| RS422 \| RS232"                                                                                                                       | SRC-001 LAB SPACE; SRC-002 Basic Unit                                                          | `Bioreactor` → `hasCommunicationProtocol` → xsd:string                                 | Explícita | Alta      | No                 |
| EV-17 | Los parámetros operativos se agrupan en físicos y químicos                                                          | "(1) physical, such as temperature, vessel pressure, agitation rate, and medium viscosity, (2) chemical, such as pH, nutrient concentration, and gas concentration like dissolved oxygen (DO)" | SRC-004 sección clasificación                                                                  | `OperativeParameter` → subclases `PhysicalParameter` / `ChemicalParameter`             | Explícita | Alta      | No                 |
| EV-18 | El control de lazo cerrado para DO opera en cascada con ajuste de agitación y flujo de gas                          | "Multi-stage DO cascade control" / "Integrated digital control loops for Temperature, pH, DO, agitation, gas mixing"                                                                           | SRC-002 Digital Controller                                                                     | `DOControlLoop` → `hasControlStrategy` → `CascadeControl`                              | Explícita | Alta      | No                 |
| EV-19 | El BIOSTAT® Bplus incluye control de espuma y nivel; el BioLector XT no lo documenta                                | "Integrated amplifiers for Temperature, pH, DO, Foam & Level"                                                                                                                                  | SRC-002 Digital Controller; ausencia en SRC-001                                                | `Bioreactor` → `hasFoamSensor` → `FoamSensor` (propiedad opcional)                     | Inferida  | Media     | Sí                 |
| EV-20 | La presión del gas suministrado es una propiedad de utilidades de los sistemas biorreactor                          | "Gasses: Controlled @ 1.5 barg dry, particle and oil-free"                                                                                                                                     | SRC-002 Utilities Requirements                                                                 | `Bioreactor` → `hasGasSupplyPressure` → xsd:float                                      | Explícita | Media     | Sí                 |
| EV-21 | La turbidez y el potencial redox son parámetros opcionales no universales en el proyecto                            | "Turbidity (option): 0–6 AU / Redox (optional): –1,000–1,000 mV" / ausencia en SRC-001                                                                                                         | SRC-002 Measurement Ranges; ausencia en SRC-001                                                | `Bioreactor` → `hasTurbidityMeasurement` / `hasRedoxMeasurement` (opcionales)          | Inferida  | Media     | Sí                 |
| EV-22 | El tipo de vaso de cultivo (placa microtiter vs. vaso cilíndrico) es propiedad estructural del biorreactor          | "48 cultivation wells / Filling volume: 800–1900 μL" / "Single wall glass vessel with stainless steel head"                                                                                    | SRC-001 MICROTITER PLATES; SRC-002 Culture Vessel                                              | `Bioreactor` → `hasVesselType` → `VesselType`                                          | Explícita | Alta      | No                 |
| EV-23 | Los biorreactores pueden clasificarse como submerged (fermentación sumergida) según el modo de contacto gas-líquido | "In submerged fermentation, the substrate to be fermented is always in a liquid phase along with the nutrients required for microorganism growth, and gas exchange occurs via mixing"          | SRC-004 sección clasificación                                                                  | `Bioreactor` → `hasFermentationMode` → `SubmergedFermentation`                         | Explícita | Alta      | No                 |
| EV-24 | El número de parámetros monitoreables depende del número de sensores y elementos de control instalados              | "The number of parameters that can be monitored and controlled is limited by the number of sensors and control elements incorporated into a given bioreactor"                                  | SRC-003 párr. 1                                                                                | `Bioreactor` → `hasInstrumentationCapacity` → `SensorCount` (propiedad de restricción) | Explícita | Media     | Sí                 |
| EV-25 | El software de supervisión (SCADA/MES) es un componente de conectividad asociado al biorreactor                     | "BioPAT® MFCS/DA for data storage" / "BioLection software"                                                                                                                                     | SRC-002 SCADA Software; SRC-001 (software mencionado en documentación general)                 | `Bioreactor` → `hasSupervisorySystem` → `SCADASystem`                                  | Inferida  | Media     | Sí                 |

---

## 4. Conceptos ontológicos candidatos

| Concepto candidato       | Tipo OWL sugerido                          | Definición basada exclusivamente en el corpus                                                                                                             | Fuente(s)                 | Estado    |
| ------------------------ | ------------------------------------------ | --------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------- | --------- |
| `Bioreactor`             | Clase                                      | Sistema controlado que aloja un cultivo biológico y expone propiedades de volumen, temperatura, pH, DO, agitación, composición de gas y modo de operación | SRC-001, SRC-002, SRC-003 | Candidato |
| `WorkingVolume`          | Propiedad de dato (xsd:float)              | Volumen efectivo del medio de cultivo en el pozo o vaso durante operación; expresado en µL o L                                                            | SRC-001, SRC-002          | Candidato |
| `FillingVolume`          | Propiedad de dato (xsd:float)              | Volumen de llenado del pozo de placa microtiter, dependiente de rpm; expresado en µL                                                                      | SRC-001                   | Candidato |
| `TotalVolume`            | Propiedad de dato (xsd:float)              | Volumen total del vaso de cultivo incluyendo espacio de cabeza; expresado en L                                                                            | SRC-002                   | Candidato |
| `TemperatureRange`       | Clase                                      | Intervalo operativo de temperatura (mínimo y máximo) del biorreactor                                                                                      | SRC-001, SRC-002          | Candidato |
| `pHRange`                | Clase                                      | Intervalo de medición y control de pH del biorreactor                                                                                                     | SRC-001, SRC-002          | Candidato |
| `DORange`                | Clase                                      | Intervalo de medición del oxígeno disuelto expresado en % saturación O₂                                                                                   | SRC-001, SRC-002          | Candidato |
| `AgitationSpeedRange`    | Clase                                      | Intervalo de velocidad de agitación orbital o mecánica del biorreactor en rpm                                                                             | SRC-001, SRC-002          | Candidato |
| `GasComposition`         | Clase                                      | Descripción de la mezcla de gases de entrada al biorreactor: porcentajes de O₂, CO₂, N₂ y/o aire                                                          | SRC-001, SRC-002, SRC-003 | Candidato |
| `OperationMode`          | Individuo / Enumeración                    | Modo de operación del cultivo: batch, fed-batch, bolus, continuo, perfusión                                                                               | SRC-001, SRC-002, SRC-003 | Candidato |
| `VesselType`             | Clase                                      | Tipo estructural del recipiente de cultivo: placa microtiter (48 pozos), vaso cilíndrico de vidrio                                                        | SRC-001, SRC-002          | Candidato |
| `DisposabilityClass`     | Propiedad de dato (xsd:string) o Individuo | Clasificación del recipiente como desechable (single-use) o reutilizable (multi-use)                                                                      | SRC-001, SRC-002          | Candidato |
| `SensorSystem`           | Clase                                      | Sistema de instrumentación del biorreactor que incluye uno o más sensores para parámetros operativos                                                      | SRC-001, SRC-002          | Candidato |
| `OpticalSensor`          | Subclase de `SensorSystem`                 | Sensor basado en medición óptica pre-calibrada (optodo); usado para pH y DO en BioLector XT                                                               | SRC-001                   | Candidato |
| `PolarographicElectrode` | Subclase de `SensorSystem`                 | Electrodo polarográfico para medición de pO₂; presente en BIOSTAT® Bplus                                                                                  | SRC-002                   | Candidato |
| `GelFilledElectrode`     | Subclase de `SensorSystem`                 | Electrodo de gel para medición de pH; presente en BIOSTAT® Bplus                                                                                          | SRC-002                   | Candidato |
| `Pt100Probe`             | Subclase de `SensorSystem`                 | Sonda resistiva Pt100 para medición de temperatura; presente en BIOSTAT® Bplus                                                                            | SRC-002                   | Candidato |
| `ControlLoop`            | Clase                                      | Lazo de control automático que regula un parámetro operativo con set-point configurable                                                                   | SRC-001, SRC-002          | Candidato |
| `CascadeControl`         | Subclase de `ControlLoop`                  | Estrategia de control en cascada multi-etapa; documentada para DO en BIOSTAT® Bplus                                                                       | SRC-002                   | Candidato |
| `PhysicalParameter`      | Subclase de `OperativeParameter`           | Parámetro operativo de naturaleza física: temperatura, presión, velocidad de agitación, viscosidad                                                        | SRC-004                   | Candidato |
| `ChemicalParameter`      | Subclase de `OperativeParameter`           | Parámetro operativo de naturaleza química: pH, concentración de nutrientes, DO                                                                            | SRC-004                   | Candidato |
| `ManufacturerName`       | Propiedad de dato (xsd:string)             | Nombre de la entidad fabricante del biorreactor                                                                                                           | SRC-001, SRC-002          | Candidato |
| `ModelName`              | Propiedad de dato (xsd:string)             | Denominación comercial del modelo del biorreactor                                                                                                         | SRC-001, SRC-002          | Candidato |
| `CommunicationProtocol`  | Propiedad de dato (xsd:string)             | Protocolo de comunicación del sistema con equipos externos: Ethernet, RS422, RS232                                                                        | SRC-001, SRC-002          | Candidato |
| `FermentationMode`       | Clase                                      | Modo de contacto gas-líquido del sistema: fermentación sumergida o en estado sólido                                                                       | SRC-004                   | Candidato |
| `SCADASystem`            | Clase                                      | Sistema supervisor de adquisición y control de datos asociado al biorreactor                                                                              | SRC-002                   | Candidato |

---

## 5. Relaciones ontológicas candidatas

| Relación candidata         | Dominio sugerido                          | Rango sugerido        | Significado                                                                  | Evidencia asociada  | Estado    |
| -------------------------- | ----------------------------------------- | --------------------- | ---------------------------------------------------------------------------- | ------------------- | --------- |
| `hasModelName`             | `Bioreactor`                              | xsd:string            | Un biorreactor tiene una denominación comercial de modelo                    | EV-01               | Candidata |
| `hasManufacturer`          | `Bioreactor`                              | `Manufacturer`        | Un biorreactor es producido por una entidad fabricante                       | EV-02               | Candidata |
| `hasWorkingVolume`         | `Bioreactor`                              | xsd:float             | Un biorreactor tiene un volumen de trabajo operativo                         | EV-03               | Candidata |
| `hasTotalVolume`           | `Bioreactor`                              | xsd:float             | Un biorreactor tiene un volumen total de su vaso                             | EV-04               | Candidata |
| `hasTemperatureRange`      | `Bioreactor`                              | `TemperatureRange`    | Un biorreactor opera dentro de un rango de temperatura definido              | EV-05               | Candidata |
| `haspHRange`               | `Bioreactor`                              | `pHRange`             | Un biorreactor mide y controla pH en un rango definido                       | EV-06               | Candidata |
| `hasDORange`               | `Bioreactor`                              | `DORange`             | Un biorreactor mide oxígeno disuelto en un rango definido                    | EV-08               | Candidata |
| `hasAgitationSpeedRange`   | `Bioreactor`                              | `AgitationSpeedRange` | Un biorreactor opera la agitación dentro de un rango de rpm                  | EV-09               | Candidata |
| `hasGasComposition`        | `Bioreactor`                              | `GasComposition`      | Un biorreactor recibe una mezcla de gases con composición definida           | EV-11               | Candidata |
| `hasOperationMode`         | `Bioreactor`                              | `OperationMode`       | Un biorreactor puede operar en uno o más modos de cultivo                    | EV-12               | Candidata |
| `hasDisposabilityClass`    | `Bioreactor`                              | `DisposabilityClass`  | Un biorreactor se clasifica como desechable o reutilizable                   | EV-13               | Candidata |
| `hasVesselType`            | `Bioreactor`                              | `VesselType`          | Un biorreactor usa un tipo estructural de recipiente de cultivo              | EV-22               | Candidata |
| `hasSensorSystem`          | `Bioreactor`                              | `SensorSystem`        | Un biorreactor está equipado con un sistema de sensores                      | EV-14, EV-15        | Candidata |
| `hasSensorTechnology`      | `SensorSystem`                            | `SensorTechnology`    | Un sistema de sensores usa una tecnología específica de medición             | EV-14, EV-15        | Candidata |
| `hasControlLoop`           | `Bioreactor`                              | `ControlLoop`         | Un biorreactor posee lazos de control automático para parámetros operativos  | EV-07, EV-10, EV-18 | Candidata |
| `controlsParameter`        | `ControlLoop`                             | `OperativeParameter`  | Un lazo de control regula un parámetro operativo específico                  | EV-07, EV-10, EV-18 | Candidata |
| `hasControlStrategy`       | `ControlLoop`                             | `ControlStrategy`     | Un lazo de control implementa una estrategia (PI, cascada, etc.)             | EV-07, EV-18        | Candidata |
| `hasCommunicationProtocol` | `Bioreactor`                              | xsd:string            | Un biorreactor se conecta a sistemas externos mediante un protocolo definido | EV-16               | Candidata |
| `hasFermentationMode`      | `Bioreactor`                              | `FermentationMode`    | Un biorreactor opera bajo un modo de contacto gas-líquido                    | EV-23               | Candidata |
| `isSubclassOf`             | `PhysicalParameter` / `ChemicalParameter` | `OperativeParameter`  | Los parámetros operativos se especializan en físicos y químicos              | EV-17               | Candidata |
| `hasSupervisorySystem`     | `Bioreactor`                              | `SCADASystem`         | Un biorreactor se conecta a un sistema SCADA/MES para supervisión            | EV-25               | Candidata |

---

## 6. Triadas RDF candidatas

```
# — IDENTIFICACIÓN —
BioLectorXT        rdf:type                    Bioreactor
BioLectorXT        hasModelName                "BioLector XT"
BioLectorXT        hasManufacturer             Beckman_Coulter_m2p_labs
SartoriusBplus5L   rdf:type                    Bioreactor
SartoriusBplus5L   hasModelName                "BIOSTAT Bplus 5L"
SartoriusBplus5L   hasManufacturer             Sartorius_Stedim_Biotech
SartoriusBplus10L  rdf:type                    Bioreactor
SartoriusBplus10L  hasModelName                "BIOSTAT Bplus 10L"
SartoriusBplus10L  hasManufacturer             Sartorius_Stedim_Biotech

# — VOLUMEN —
BioLectorXT        hasWorkingVolume_min         "800"       # µL, FlowerPlate
BioLectorXT        hasWorkingVolume_max         "2400"      # µL, Round Well
SartoriusBplus5L   hasWorkingVolume_min         "0.6"       # L
SartoriusBplus5L   hasWorkingVolume_max         "5.0"       # L
SartoriusBplus5L   hasTotalVolume               "6.6"       # L
SartoriusBplus10L  hasWorkingVolume_min         "1.5"       # L
SartoriusBplus10L  hasWorkingVolume_max         "10.0"      # L
SartoriusBplus10L  hasTotalVolume               "13.0"      # L

# — TEMPERATURA —
BioLectorXT        hasTemperatureRange          TemperatureRange_10_50C
TemperatureRange_10_50C   hasMinValue          "10"
TemperatureRange_10_50C   hasMaxValue          "50"
TemperatureRange_10_50C   hasUnit              "°C"
SartoriusBplus5L   hasTemperatureRange          TemperatureRange_Meas_0_150C
SartoriusBplus5L   hasTemperatureControlRange   TemperatureControlRange_Sartorius
TemperatureControlRange_Sartorius  hasMaxValue  "60"
TemperatureControlRange_Sartorius  hasUnit      "°C"

# — pH —
BioLectorXT        haspHRange                   pHRange_4_7p5
pHRange_4_7p5      hasMinValue                  "4.0"
pHRange_4_7p5      hasMaxValue                  "7.5"
SartoriusBplus5L   haspHRange                   pHRange_2_12
pHRange_2_12       hasMinValue                  "2"
pHRange_2_12       hasMaxValue                  "12"

# — OXÍGENO DISUELTO —
BioLectorXT        hasDORange                   DORange_0_100pct
SartoriusBplus5L   hasDORange                   DORange_0_100pct
DORange_0_100pct   hasMinValue                  "0"
DORange_0_100pct   hasMaxValue                  "100"
DORange_0_100pct   hasUnit                      "% O2 saturation"

# — AGITACIÓN —
BioLectorXT        hasAgitationSpeedRange        AgitationRange_100_1500rpm
AgitationRange_100_1500rpm  hasMinValue         "100"
AgitationRange_100_1500rpm  hasMaxValue         "1500"
AgitationRange_100_1500rpm  hasUnit             "rpm"
AgitationRange_100_1500rpm  hasAgitationType    "orbital_3mm_diameter"
SartoriusBplus5L   hasAgitationSpeedRange        AgitationRange_20_1500rpm
SartoriusBplus10L  hasAgitationSpeedRange        AgitationRange_20_800rpm

# — COMPOSICIÓN DE GAS —
BioLectorXT        hasGasComposition             GasComp_BioLectorXT
GasComp_BioLectorXT  includesGas               "O2_1_100pct"
GasComp_BioLectorXT  includesGas               "CO2_0_12pct"
GasComp_BioLectorXT  includesGas               "N2_anaerobic"
SartoriusBplus5L   hasGasComposition             GasComp_Sartorius
GasComp_Sartorius  includesGas                  "Air"
GasComp_Sartorius  includesGas                  "O2"
GasComp_Sartorius  includesGas                  "N2"
GasComp_Sartorius  includesGas                  "CO2"

# — MODO DE OPERACIÓN —
BioLectorXT        hasOperationMode              BatchMode
BioLectorXT        hasOperationMode              FedBatchMode
BioLectorXT        hasOperationMode              BolusFeedMode
BioLectorXT        hasOperationMode              ContinuousMode
SartoriusBplus5L   hasOperationMode              BatchMode
SartoriusBplus5L   hasOperationMode              FedBatchMode
SartoriusBplus5L   hasOperationMode              ContinuousMode
SartoriusBplus5L   hasOperationMode              PerfusionMode

# — VASO Y DESECHABILIDAD —
BioLectorXT        hasVesselType                 MicrotiterPlate_48wells
BioLectorXT        hasDisposabilityClass         SingleUse
SartoriusBplus5L   hasVesselType                 CylindricalGlassVessel
SartoriusBplus5L   hasDisposabilityClass         MultiUse

# — SENSORES —
BioLectorXT        hasSensorSystem               SensorSys_BioLectorXT
SensorSys_BioLectorXT  hasSensorTechnology      OpticalSensor
SensorSys_BioLectorXT  measuresParameter         pH
SensorSys_BioLectorXT  measuresParameter         DO
SensorSys_BioLectorXT  measuresParameter         Biomass
SartoriusBplus5L   hasSensorSystem               SensorSys_SartoriusBplus
SensorSys_SartoriusBplus  hasSensorTechnology    PolarographicElectrode   # para pO2
SensorSys_SartoriusBplus  hasSensorTechnology    GelFilledElectrode        # para pH
SensorSys_SartoriusBplus  hasSensorTechnology    Pt100Probe                # para Temp
SensorSys_SartoriusBplus  measuresParameter      pH
SensorSys_SartoriusBplus  measuresParameter      DO
SensorSys_SartoriusBplus  measuresParameter      Temperature
SensorSys_SartoriusBplus  measuresParameter      Foam
SensorSys_SartoriusBplus  measuresParameter      Level

# — LAZOS DE CONTROL —
BioLectorXT        hasControlLoop                CLpH_BioLectorXT
CLpH_BioLectorXT   controlsParameter             pH
CLpH_BioLectorXT   hasControlStrategy            PIControl
SartoriusBplus5L   hasControlLoop                CLTemp_Sartorius
CLTemp_Sartorius   controlsParameter             Temperature
SartoriusBplus5L   hasControlLoop                CLpH_Sartorius
CLpH_Sartorius     controlsParameter             pH
SartoriusBplus5L   hasControlLoop                CLDO_Sartorius
CLDO_Sartorius     controlsParameter             DO
CLDO_Sartorius     hasControlStrategy            CascadeControl
SartoriusBplus5L   hasControlLoop                CLAgitation_Sartorius
CLAgitation_Sartorius  controlsParameter         AgitationSpeed

# — COMUNICACIÓN —
BioLectorXT        hasCommunicationProtocol      "Ethernet"
SartoriusBplus5L   hasCommunicationProtocol      "Ethernet"
SartoriusBplus5L   hasCommunicationProtocol      "RS422"
SartoriusBplus5L   hasCommunicationProtocol      "RS232"

# — CLASIFICACIÓN DE PARÁMETROS —
Temperature        rdf:type                      PhysicalParameter
AgitationSpeed     rdf:type                      PhysicalParameter
VesselPressure     rdf:type                      PhysicalParameter
pH                 rdf:type                      ChemicalParameter
DO                 rdf:type                      ChemicalParameter
NutrientConcentration  rdf:type                  ChemicalParameter

# — MODO DE FERMENTACIÓN —
BioLectorXT        hasFermentationMode           SubmergedFermentation
SartoriusBplus5L   hasFermentationMode           SubmergedFermentation
```

**Estado de triadas por grupo:**

| Grupo                       | Estado                                         |
| --------------------------- | ---------------------------------------------- |
| Identificación              | Soportada — SRC-001, SRC-002                   |
| Volumen                     | Soportada — SRC-001, SRC-002                   |
| Temperatura                 | Soportada — SRC-001, SRC-002, SRC-003          |
| pH                          | Soportada — SRC-001, SRC-002, SRC-003          |
| DO                          | Soportada — SRC-001, SRC-002, SRC-003          |
| Agitación                   | Soportada — SRC-001, SRC-002, SRC-003, SRC-004 |
| Composición de gas          | Soportada — SRC-001, SRC-002, SRC-003          |
| Modo de operación           | Soportada — SRC-001, SRC-002, SRC-003          |
| Vaso y desechabilidad       | Soportada — SRC-001, SRC-002                   |
| Sensores                    | Soportada — SRC-001, SRC-002                   |
| Lazos de control            | Soportada — SRC-001, SRC-002                   |
| Comunicación                | Soportada — SRC-001, SRC-002                   |
| Clasificación de parámetros | Soportada — SRC-004                            |
| Fermentación sumergida      | Soportada — SRC-004                            |

---

## 7. Sinónimos documentados en el corpus

| Término principal   | Sinónimos o variantes documentadas en el corpus               | Fuente(s)                                                                                                    |
| ------------------- | ------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------ |
| `workingVolume`     | filling volume                                                | SRC-001 (filling volume), SRC-002 (working volume)                                                           |
| `dissolvedOxygen`   | DO, pO₂, oxygen saturation, dissolved oxygen                  | SRC-001 (DO, dissolved oxygen), SRC-002 (pO2), SRC-003 (dissolved oxygen levels), SRC-004 (DO)               |
| `agitationSpeed`    | shaking speed, stirring speed, stirrer speed, agitation rate  | SRC-001 (shaking speed), SRC-002 (agitation motor speed), SRC-003 (agitation rate), SRC-004 (agitation rate) |
| `operationMode`     | culture mode, process mode, feeding strategy                  | SRC-001 (feeding options/profiles), SRC-002 (applicable for), SRC-003 (mode of operation)                    |
| `singleUse`         | disposable, disposable technology                             | SRC-001 (disposable technology)                                                                              |
| `multiUse`          | reusable, multi-use bioreactors                               | SRC-002 (Multi-Use Bioreactors)                                                                              |
| `opticalSensor`     | optode, pre-calibrated optical sensor, fluorescence sensor    | SRC-001 (optical sensors, optodes)                                                                           |
| `gasComposition`    | gas mixing, gas mixture, environmental conditions             | SRC-001 (Environmental Conditions), SRC-002 (Gassing System), SRC-003 (flow rates of gas)                    |
| `controlLoop`       | closed loop controller, digital control loop, cascade control | SRC-001 (closed loop controller), SRC-002 (digital control loops, cascade control)                           |
| `supervisorySystem` | SCADA, BioPAT® MFCS/DA, BioLection software                   | SRC-002 (BioPAT® MFCS/DA)                                                                                    |
| `vesselPressure`    | barg, gas supply pressure                                     | SRC-002 (1.5 barg)                                                                                           |

---

## 8. Vacíos del corpus

| Vacío identificado | Descripción                                                           | Impacto ontológico                                                                                                                                                         | Acción recomendada                                                                         | |
| ------------------ | --------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------ | -------------------------------------------------------------------------- |
| V-01               | Denominación exacta del modelo Sartorius instalado en el proyecto     | El corpus usa "BIOSTAT® Bplus" pero el proyecto menciona "Sartorius 5 L" y "Sartorius 10 L" sin especificar modelo; pueden corresponder al B-DCU u otra variante           | Alto — afecta la identidad del individuo OWL                                               | Confirmar modelo con investigador o laboratorio responsable                |
| V-02               | Propiedades de biomasa en línea en el BioLector XT                    | SRC-001 menciona medición de biomasa por dispersión de luz pero no en los fragmentos suministrados al corpus; no hay rango ni unidad explícita en los fragmentos incluidos | Medio — la biomasa aparece en triadas pero sin soporte numérico verificable en este corpus | Suministrar fragmento específico de SRC-001 que contenga rangos de biomasa |
| V-03               | Ausencia de sensor de espuma y nivel en BioLector XT                  | SRC-001 no documenta estos sensores; SRC-002 sí los incluye; no es posible determinar si su ausencia es estructural o solo documental                                      | Medio — propiedad no puede asignarse como general; solo como específica de Sartorius       | Validar con experto o consultar manual completo de BioLector XT            |
| V-04               | Presión interna del vaso de cultivo como variable monitorizada online | SRC-002 menciona "vessel pressure" en contexto de diseño (barg) pero no como parámetro monitoreado en línea; SRC-004 la clasifica como parámetro físico                    | Medio — no puede afirmarse como propiedad medida universalmente                            | Validar si existe sensor de presión instalado en los sistemas del proyecto |
| V-05               | SOPs institucionales y restricciones operativas del laboratorio       | El corpus no incluye procedimientos operativos propios del laboratorio que puedan añadir propiedades contextuales o restricciones de set-point                             | Alto — las propiedades pueden tener restricciones de rango distintas a las del fabricante  | Solicitar SOPs al equipo del proyecto                                      |
| V-06               | Propiedades de turbidez y redox como opcionales no universales        | Presentes opcionalmente en SRC-002; completamente ausentes en SRC-001; no pueden modelarse como propiedades generales sin validación                                       | Medio — deben modelarse con cardinalidad 0..1 (opcional)                                   | Validar con experto la relevancia para el proyecto                         |
| V-07               | Unidad de volumen homologada entre escalas                            | SRC-001 usa µL; SRC-002 usa L; el corpus no define una unidad canónica de conversión                                                                                       | Medio — impacta comparabilidad semántica entre individuos                                  | Definir unidad base (recomendación: L con conversión µL→L) en el modelo    |
| V-08               | Definición de "escala operativa" como propiedad formal                | El corpus no provee una taxonomía explícita de escalas (micro, laboratorio, piloto, producción) como categoría documentada                                                 | Medio — escala puede inferirse pero no afirmarse explícitamente                            | Buscar fuente adicional con clasificación de escalas de bioproceso         |

---

## 9. Estado final

| Dimensión                                        | Estado                                                                                                                                                                                                |
| ------------------------------------------------ | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Respuesta a la pregunta ALC-06**               | **Soportada**                                                                                                                                                                                         |
| **Cobertura del corpus**                         | Las cuatro fuentes proveen evidencia explícita suficiente para las propiedades fundamentales (volumen, temperatura, pH, DO, agitación, gas, modo de operación, vaso, sensores, control, comunicación) |
| **Propiedades con soporte total**                | 22 de 25 afirmaciones con evidencia explícita de alta confianza                                                                                                                                       |
| **Propiedades que requieren validación experta** | EV-19 (espuma/nivel), EV-20 (presión de gas), EV-21 (turbidez/redox), EV-24 (capacidad de instrumentación), EV-25 (SCADA)                                                                             |
| **Vacíos críticos**                              | V-01 (confirmación de modelo Sartorius), V-02 (biomasa en línea sin rango numérico), V-05 (SOPs institucionales)                                                                                      |
| **Próxima acción recomendada**                   | Confirmar modelo Sartorius exacto → suministrar fragmento de biomasa de SRC-001 → validar propiedades opcionales con experto → definir unidad de volumen canónica                                     |
