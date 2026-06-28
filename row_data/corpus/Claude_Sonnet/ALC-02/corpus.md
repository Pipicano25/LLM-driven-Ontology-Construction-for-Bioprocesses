---
# Extracción condicionada por corpus — ALC-02
---

## 1. ID y pregunta

**ID:** ALC-02
**Pregunta:** ¿Qué características mínimas debe tener un sistema para ser considerado biorreactor y no solo un recipiente de cultivo?
**Corpus de trabajo:** SRC-001 a SRC-007
**Restricción operativa:** Toda afirmación debe ser trazable a un fragmento verificable del corpus. Cuando la evidencia sea insuficiente se indica explícitamente.

---

## 2. Respuesta basada en evidencia

### 2.1 Definición base extraída del corpus

El corpus permite reconstruir la siguiente definición operativa a partir de evidencia convergente:

Un **biorreactor** es un sistema manufacturado, cerrado, que soporta un entorno biológicamente activo mediante cuatro capacidades funcionales mínimas identificadas en el corpus:

**Capacidad 1 — Contención estéril activa**
El corpus establece que un biorreactor está diseñado para producción "controlled and sterile" (SRC-001, fragmento 1) y que la norma de referencia del sector requiere equipos "both cleanable and sterilizable" (SRC-003, fragmento 4). El BIOSTAT B opera hasta 150 °C a 2.5 barg (SRC-006, fragmento 5), condición compatible con esterilización in situ. Esto contrasta con un recipiente de cultivo ordinario, que no posee un sistema activo de esterilización incorporado. _Evidencia: explícita._

**Capacidad 2 — Monitoreo en tiempo real de variables críticas del proceso**
El corpus es explícito en que los biorreactores instrumentados poseen esta capacidad y los matraces de agitación no: "In contrast to instrumented bioreactors, reliable options for non-invasive, time-resolved monitoring of the culture status in shake flasks are lacking" (SRC-005, fragmento 1). Doran (SRC-004) especifica que el biorreactor de banco está "equipped with instruments for measuring and adjusting temperature, pH, dissolved oxygen concentration, stirrer speed". SRC-001 lista los parámetros que deben ser monitoreables: DO, pH, temperatura, velocidad de agitación, valor redox. El BioLector XT mide en línea biomasa, fluorescencias, pH y DO (SRC-002, fragmento 1). El BIOSTAT B incluye sensores de pH, pO₂, temperatura, espuma, nivel y sustrato (SRC-006, fragmento 7). _Evidencia: explícita._

**Capacidad 3 — Control activo de variables fisicoquímicas**
SRC-004 establece que el biorreactor permite no solo medir sino "adjusting" las variables de proceso. SRC-001 exige que el sistema permita "monitor and/or control reaction parameters [...] to create a controlled aseptic environment". SRC-002 confirma "Flexible process control of pH, shaking, temperature and gassing" en el BioLector XT. La diferencia con el matraz de agitación es explícita en SRC-004: "Cultures can be more closely monitored in bioreactors than in shake flasks, so better control over the process is possible." _Evidencia: explícita._

**Capacidad 4 — Gestión activa de transferencia de masa gas-líquido**
SRC-001 establece que el biorreactor está diseñado "with air inflow and outflow systems". SRC-006 especifica sparger poroso y tipo-L, flujo de gas (aire, O₂, CO₂, N₂, máx. 20 lpm) en el BIOSTAT B. SRC-002 documenta control activo de concentración de O₂ hasta 100 % y CO₂ hasta 12 % en el BioLector XT. SRC-007 cuantifica la diferencia: los STR alcanzan OTR de 100–150 mmol/L/h, frente a las capacidades significativamente menores del matraz por sus "limited gas-liquid mass transfer capacities" (SRC-007, fragmento 2). _Evidencia: explícita._

### 2.2 Distinción documentada entre biorreactor y recipiente de cultivo simple

El corpus suministra evidencia explícita de que los **matraces de agitación** son el límite inferior del espectro, identificables como recipientes de cultivo **no instrumentados**:

- SRC-005 establece que los matraces carecen de monitoreo no invasivo en tiempo real (fragmento 1)
- SRC-004 indica que el biorreactor permite mejor control que el matraz (fragmento 2)
- SRC-007 documenta que la limitación principal del matraz es la baja transferencia gas-líquido (fragmento 2) y cuantifica la diferencia en OTR respecto al STR (fragmento 3)

### 2.3 Información no establecida en el corpus suministrado

- No existe en el corpus una norma, definición formal o umbral cuantitativo mínimo unívoco que establezca el número exacto de sensores o el rango mínimo de parámetros controlados para que un sistema sea legalmente o normativamente clasificado como biorreactor.
- El contenido normativo completo de ASME BPE-2022 (sección de definiciones GR-1) no está disponible en los fragmentos suministrados de SRC-003.
- No hay en el corpus una definición de biorreactor emitida por FDA o EMA.

---

## 3. Tabla de afirmaciones y evidencia

| ID Ev      | Afirmación                                                                                                                                                                | Texto/fragmento de evidencia                                                                                                                                                                                                                                              | Fuente y sección                                           | Concepto/relación/triada candidata                                                                                                                                                       | Tipo de evidencia                                                                                                       | Confianza                                                        | Validación experta                                                    |
| ---------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------- | --------------------------------------------------------------------- |
| ALC02-EV01 | Un biorreactor es un recipiente de cultivo diseñado con sistemas de entrada y salida de aire para producción controlada y estéril                                         | "Bioreactors are culture vessels designed with air inflow and outflow systems for the controlled and sterile production of mass quantities of biological materials."                                                                                                      | SRC-001, párrafo Overview                                  | `Bioreactor` subclaseOf `CultureVessel`; `hasAerationSystem`; `hasSterileBarrier`                                                                                                        | Explícita                                                                                                               | Alta                                                             | No                                                                    |
| ALC02-EV02 | El biorreactor debe proveer en todos los casos las condiciones ambientales necesarias para el cultivo                                                                     | "In all cases, the bioreactor must provide the environmental conditions necessary for the culture."                                                                                                                                                                       | SRC-001, párrafo Overview                                  | `Bioreactor` `providesCondition` `CultureEnvironment`                                                                                                                                    | Explícita                                                                                                               | Alta                                                             | No                                                                    |
| ALC02-EV03 | Un biorreactor debe permitir monitorear/controlar DO, pH, temperatura, agitación y redox para crear un entorno aséptico controlado                                        | "Easy to monitor and/or control reaction parameters (such as dissolved oxygen concentration, pH, temperature, agitation rate, redox value, and so on) to create a controlled aseptic environment for biocatalysts."                                                       | SRC-001, sección de requisitos (cita interna a Panda 2011) | `Bioreactor` `requiresCapability` `ActiveProcessControl`; `ProcessSensor`                                                                                                                | Explícita                                                                                                               | Alta                                                             | Sí (la referencia primaria Panda 2011 no fue verificada directamente) |
| ALC02-EV04 | Un biorreactor de banco de 1–2 L está equipado con instrumentos para medir y ajustar temperatura, pH, DO y velocidad del agitador                                         | "The first stage may be a 1- or 2-litre bench-top bioreactor equipped with instruments for measuring and adjusting temperature, pH, dissolved oxygen concentration, stirrer speed, and other process variables."                                                          | SRC-004, cap. 14, Step 13                                  | `BenchTopBioreactor` `hasSensor` `TemperatureSensor`; `hasSensor` `pHSensor`; `hasSensor` `DissolvedOxygenSensor`; `hasActuator` `AgitationController`                                   | Explícita                                                                                                               | Alta                                                             | No                                                                    |
| ALC02-EV05 | Los biorreactores permiten mayor control del proceso que los matraces de agitación                                                                                        | "Cultures can be more closely monitored in bioreactors than in shake flasks, so better control over the process is possible."                                                                                                                                             | SRC-004, cap. 14, Step 13                                  | `Bioreactor` `hasCapability` `ClosedLoopControl`; `ShakeFlask` `lacksCapability` `ClosedLoopControl`                                                                                     | Explícita                                                                                                               | Alta                                                             | No                                                                    |
| ALC02-EV06 | Los matraces de agitación carecen de opciones confiables para monitoreo no invasivo en tiempo real del estado del cultivo                                                 | "In contrast to instrumented bioreactors, reliable options for non-invasive, time-resolved monitoring of the culture status in shake flasks are lacking."                                                                                                                 | SRC-005, Abstract                                          | `ShakeFlask` `lacksCapability` `RealTimeProcessMonitoring`; `InstrumentedBioreactor` `hasCapability` `RealTimeProcessMonitoring`                                                         | Explícita                                                                                                               | Alta                                                             | No                                                                    |
| ALC02-EV07 | El BioLector XT mide en línea biomasa, fluorescencias, pH y DO mediante sensores ópticos precalibrados                                                                    | "High-throughput microbioreactor enables real-time evaluation of biomass, fluorescence, pH, dissolved oxygen in the liquid phase (DO), and other key cultivation parameters." / "Disposable 48 well MTPs enable online measurement of biomass, fluorescences, pH and DO." | SRC-002, descripción del producto                          | `BioLectorXT` `hasSensor` `BiomassSensor`; `hasSensor` `FluorescenceSensor`; `hasSensor` `pHSensor`; `hasSensor` `DissolvedOxygenSensor`                                                 | Explícita                                                                                                               | Alta                                                             | No                                                                    |
| ALC02-EV08 | El BioLector XT controla activamente pH, agitación, temperatura y gaseo                                                                                                   | "Flexible process control of pH, shaking, temperature and gassing."                                                                                                                                                                                                       | SRC-002, sección características                           | `BioLectorXT` `hasActuator` `pHController`; `hasActuator` `AgitationController`; `hasActuator` `TemperatureController`; `hasActuator` `GasController`                                    | Explícita                                                                                                               | Alta                                                             | No                                                                    |
| ALC02-EV09 | El BioLector XT controla activamente la concentración de O₂ entrante hasta 100 % y de CO₂ hasta 12 %                                                                      | "Actively regulated O2 or CO2 concentration of ingoing gas can be raised to ≤ 100 % or ≤ 12 %, respectively."                                                                                                                                                             | SRC-002, sección características                           | `BioLectorXT` `hasGasControlRange` `O2_0-100pct`; `hasGasControlRange` `CO2_0-12pct`                                                                                                     | Explícita                                                                                                               | Alta                                                             | No                                                                    |
| ALC02-EV10 | El BioLector XT opera con volumen de trabajo de 800–2400 µL por pocillo                                                                                                   | "Small working volume (800 – 2400 μL)."                                                                                                                                                                                                                                   | SRC-002, sección características (módulo microfluídico)    | `BioLectorXT` `hasWorkingVolume` `800-2400_µL`                                                                                                                                           | Explícita                                                                                                               | Alta                                                             | No                                                                    |
| ALC02-EV11 | El BioLector XT permite estrategias de alimentación: batch, fed-batch, bolus, continua                                                                                    | "Fully customizable and freely combinable actively regulated feeding strategies (batch, fed-batch, bolus, continuous)."                                                                                                                                                   | SRC-002, sección características                           | `BioLectorXT` `supportsOperationMode` `BatchMode`; `FedBatchMode`; `BolusMode`; `ContinuousMode`                                                                                         | Explícita                                                                                                               | Alta                                                             | No                                                                    |
| ALC02-EV12 | El BIOSTAT B (Sartorius) tiene volúmenes de trabajo de 0.6–5 L (modelo 5 L) y 1.5–10 L (modelo 10 L)                                                                      | "Working volume: 2L (0.4-2L); 5L (0.6-5L); 10L (1.5-10L)"                                                                                                                                                                                                                 | SRC-006, tabla de especificaciones técnicas                | `SartoriusBIOSTATB_5L` `hasWorkingVolume` `0.6-5_L`; `SartoriusBIOSTATB_10L` `hasWorkingVolume` `1.5-10_L`                                                                               | Explícita                                                                                                               | Alta                                                             | Sí (verificar contra manual oficial Sartorius)                        |
| ALC02-EV13 | El BIOSTAT B tiene sensores de pH, pO₂, temperatura, espuma, nivel y sustrato                                                                                             | "Sensors: pH, pO2, Temperature, Foam, Level, Substrate"                                                                                                                                                                                                                   | SRC-006, tabla de especificaciones técnicas                | `SartoriusBIOSTATB` `hasSensor` `pHSensor`; `hasSensor` `pO2Sensor`; `hasSensor` `TemperatureSensor`; `hasSensor` `FoamSensor`; `hasSensor` `LevelSensor`; `hasSensor` `SubstrateSensor` | Explícita                                                                                                               | Alta                                                             | Sí (fuente secundaria; verificar con manual Sartorius)                |
| ALC02-EV14 | El BIOSTAT B controla temperatura en el rango 0–80 °C                                                                                                                     | "Temperature control: 0 – 80 °C"                                                                                                                                                                                                                                          | SRC-006, tabla de especificaciones técnicas                | `SartoriusBIOSTATB` `hasTemperatureControlRange` `0-80_°C`                                                                                                                               | Explícita                                                                                                               | Alta                                                             | Sí (verificar con manual oficial)                                     |
| ALC02-EV15 | El BIOSTAT B (5 L) permite agitación de 20–1500 rpm; el de 10 L de 20–800 rpm                                                                                             | "Permitted stirring speed: 5L (20-1500rpm); 10L (20-800rpm)"                                                                                                                                                                                                              | SRC-006, tabla de especificaciones técnicas                | `SartoriusBIOSTATB_5L` `hasAgitationRange` `20-1500_rpm`; `SartoriusBIOSTATB_10L` `hasAgitationRange` `20-800_rpm`                                                                       | Explícita                                                                                                               | Alta                                                             | Sí (verificar con manual oficial)                                     |
| ALC02-EV16 | El BIOSTAT B opera hasta 150 °C / 2.5 barg, condición compatible con esterilización in situ                                                                               | "Culture vessel design: -1 to + 2.5 barg @ 150 °C"                                                                                                                                                                                                                        | SRC-006, tabla de especificaciones técnicas                | `SartoriusBIOSTATB` `enablesSterilization` `SteamInPlace`; `SteamInPlace` `hasTemperature` `150_°C`                                                                                      | Inferida (la capacidad SIP se infiere del rango de presión/temperatura; el corpus no usa el término SIP explícitamente) | Media                                                            | Sí                                                                    |
| ALC02-EV17 | El BIOSTAT B utiliza sparger poroso y tipo-L para la gestión de gas                                                                                                       | "Gas spargers: Porous sparger / L-type sparger"                                                                                                                                                                                                                           | SRC-006, tabla de especificaciones técnicas                | `SartoriusBIOSTATB` `hasComponent` `PorousSparger`; `hasComponent` `LTypeSparger`                                                                                                        | Explícita                                                                                                               | Alta                                                             | Sí (verificar con manual oficial)                                     |
| ALC02-EV18 | El BIOSTAT B acepta flujos de aire, O₂, CO₂ y N₂ con caudal total máximo de 20 lpm                                                                                        | "Gas flow: air, O2, CO2\*, N2 (max. total flow rate 20 lpm)"                                                                                                                                                                                                              | SRC-006, tabla de especificaciones técnicas                | `SartoriusBIOSTATB` `hasGasSupply` `Air`; `hasGasSupply` `O2`; `hasGasSupply` `CO2`; `hasGasSupply` `N2`; `hasMaxGasFlowRate` `20_lpm`                                                   | Explícita                                                                                                               | Alta                                                             | Sí (verificar con manual oficial)                                     |
| ALC02-EV19 | Los STR alcanzan tasas de transferencia de oxígeno (OTR) de 100–150 mmol/L/h en escala relevante                                                                          | "Whereas, in stirred tank reactors OTRs of 100–150 mmol/L/h can be achieved on production relevant scales."                                                                                                                                                               | SRC-007, sección discusión comparativa                     | `StirredTankBioreactor` `achievesOTR` `100-150_mmol_L_h`; `OxygenTransferRate` (propiedad de dato)                                                                                       | Explícita                                                                                                               | Alta                                                             | No                                                                    |
| ALC02-EV20 | La limitación principal de los matraces de agitación frente al STR es su menor capacidad de transferencia gas-líquido                                                     | "The limited gas-liquid mass transfer capacities—resulting from practical operation limits regarding shaking frequency and filling volumes—are a major drawback [of shake flasks]."                                                                                       | SRC-007, Abstract                                          | `ShakeFlask` `hasLimitation` `LowGasLiquidMassTransfer`                                                                                                                                  | Explícita                                                                                                               | Alta                                                             | No                                                                    |
| ALC02-EV21 | La transferencia de masa gas-líquido es controlable con mayor facilidad y confiabilidad en un STR que en el matraz                                                        | "The gas-liquid mass transfer can be determined and controlled much easier and in a more reliable manner [in stirred tank reactors]."                                                                                                                                     | SRC-007, sección de discusión                              | `StirredTankBioreactor` `hasCapability` `ControllableGasLiquidMassTransfer`; `ShakeFlask` `lacksCapability` `ControllableGasLiquidMassTransfer`                                          | Explícita                                                                                                               | Alta                                                             | No                                                                    |
| ALC02-EV22 | ASME BPE-2022 es la norma líder para diseño y fabricación de equipos usados en producción de biofarmacéuticos, requiriendo nivel definido de pureza y control de biocarga | "The ASME BPE Standard standardizes specifications for the design and construction of new fluid processing equipment used in industries that require a defined level of purity and bioburden control."                                                                    | SRC-003, descripción oficial ASME                          | `Bioreactor` (en contexto biofarmacéutico) `conformsTo` `ASME_BPE_2022`; norma establece requisitos de limpieza, esterilización y pureza                                                 | Explícita                                                                                                               | Alta                                                             | Sí (contenido normativo completo no accedido)                         |
| ALC02-EV23 | ASME BPE requiere diseños de equipos que sean limpiables y esterilizables                                                                                                 | "The need for equipment designs that are both cleanable and sterilizable."                                                                                                                                                                                                | SRC-003, fragmento 4 (scan parcial)                        | `Bioreactor` `hasDesignRequirement` `Cleanability`; `hasDesignRequirement` `Sterilizability`                                                                                             | Explícita                                                                                                               | Media (fragmento de scan parcial, no texto completo de la norma) | Sí                                                                    |
| ALC02-EV24 | El BioLector XT soporta cultivaciones aeróbicas y anaeróbicas                                                                                                             | "High-throughput microbioreactor enables real-time evaluation [...] for aerobes and anaerobes."                                                                                                                                                                           | SRC-002, descripción del producto                          | `BioLectorXT` `supportsOrganismType` `AerobicOrganism`; `supportsOrganismType` `AnaerobicOrganism`                                                                                       | Explícita                                                                                                               | Alta                                                             | No                                                                    |
| ALC02-EV25 | El BIOSTAT B es un fermentador/biorreactor diseñado para optimización y caracterización de procesos en industria alimentaria, biotecnológica y biofarmacéutica            | "It is a fermenter / bioreactor specifically designed to accommodate the requirements of process optimization and characterization in the food, biotech and biopharmaceutical industry."                                                                                  | SRC-006, descripción del equipo                            | `SartoriusBIOSTATB` `hasApplicationDomain` `FoodIndustry`; `hasApplicationDomain` `Biotechnology`; `hasApplicationDomain` `BiopharmaceuticalIndustry`                                    | Explícita                                                                                                               | Alta                                                             | No                                                                    |

---

## 4. Conceptos candidatos

| Concepto candidato       | Tipo sugerido                                    | Definición basada exclusivamente en el corpus                                                                                                                                                                                                                                                                  | Fuente(s) de soporte                           | Estado                                  |
| ------------------------ | ------------------------------------------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------- | --------------------------------------- |
| `Bioreactor`             | Clase                                            | Sistema manufacturado, cerrado, diseñado con sistemas de entrada/salida de gas para producción controlada y estéril de materiales biológicos, que provee condiciones ambientales necesarias para el cultivo y permite monitorear y/o controlar parámetros de proceso para crear un entorno aséptico controlado | SRC-001 (EV01, EV02, EV03)                     | Candidato — requiere validación experta |
| `CultureVessel`          | Clase (superclase)                               | Recipiente capaz de contener un cultivo biológico, con o sin capacidades instrumentadas de monitoreo y control; incluye biorreactores y matraces                                                                                                                                                               | SRC-001 (EV01), SRC-005 (EV06)                 | Candidato                               |
| `InstrumentedBioreactor` | Subclase de `Bioreactor`                         | Biorreactor con instrumentos integrados para medir y ajustar al menos temperatura, pH, DO y velocidad de agitación en tiempo real                                                                                                                                                                              | SRC-004 (EV04), SRC-005 (EV06)                 | Candidato                               |
| `StirredTankBioreactor`  | Subclase de `Bioreactor`                         | Biorreactor de tanque con agitación mecánica, capaz de alcanzar OTR de 100–150 mmol/L/h y control confiable de la transferencia gas-líquido                                                                                                                                                                    | SRC-007 (EV19, EV21)                           | Candidato                               |
| `MicroBioreactor`        | Subclase de `Bioreactor`                         | Biorreactor de muy pequeño volumen de trabajo (800–2400 µL por pocillo), basado en formato de placa de microtitulación, con monitoreo óptico en línea de biomasa, pH, DO y fluorescencia                                                                                                                       | SRC-002 (EV07, EV10)                           | Candidato                               |
| `ShakeFlask`             | Subclase de `CultureVessel` (no de `Bioreactor`) | Recipiente de cultivo no instrumentado para agitación orbital; carece de monitoreo en tiempo real y de control activo de pH y DO; limitado en transferencia gas-líquido                                                                                                                                        | SRC-005 (EV06), SRC-007 (EV20, EV21)           | Candidato                               |
| `ProcessSensor`          | Clase (componente)                               | Dispositivo que mide una variable de proceso (pH, DO, temperatura, biomasa, espuma, nivel, sustrato) en tiempo real dentro del biorreactor                                                                                                                                                                     | SRC-001 (EV03), SRC-002 (EV07), SRC-006 (EV13) | Candidato                               |
| `ProcessActuator`        | Clase (componente)                               | Dispositivo que ejecuta una acción de control (ajuste de temperatura, pH, gaseo, agitación, alimentación) en respuesta a lecturas del proceso                                                                                                                                                                  | SRC-002 (EV08), SRC-004 (EV04)                 | Candidato                               |
| `AerationSystem`         | Clase (componente)                               | Sistema de entrada y salida de gas que suministra oxígeno (u otros gases) al biorreactor; incluye sparger, líneas de gas y controladores de flujo                                                                                                                                                              | SRC-001 (EV01), SRC-006 (EV17, EV18)           | Candidato                               |
| `SterilizationSystem`    | Clase (componente)                               | Sistema que garantiza la contención aséptica del biorreactor; inferido del requisito de diseño "cleanable and sterilizable" (ASME BPE) y del rango de operación a 150 °C del BIOSTAT B                                                                                                                         | SRC-003 (EV23), SRC-006 (EV16)                 | Candidato — parcialmente inferido       |
| `ControlLoop`            | Clase (proceso)                                  | Bucle que vincula un sensor con un actuador para mantener una variable de proceso dentro de un rango de consigna                                                                                                                                                                                               | SRC-004 (EV04, EV05), SRC-002 (EV08)           | Candidato                               |
| `OxygenTransferRate`     | Propiedad de dato                                | Tasa volumétrica de transferencia de oxígeno del gas al líquido (unidad: mmol/L/h); distingue cuantitativamente el biorreactor de agitación mecánica del matraz                                                                                                                                                | SRC-007 (EV19, EV20)                           | Candidato                               |
| `WorkingVolume`          | Propiedad de dato                                | Volumen operativo del cultivo dentro del biorreactor, con rango mínimo y máximo; determina la escala del sistema                                                                                                                                                                                               | SRC-002 (EV10), SRC-006 (EV12)                 | Candidato                               |
| `BioLectorXT`            | Individuo de `MicroBioreactor`                   | Microbiorreactor de m2p-labs/Beckman Coulter, formato MTP ANSI/SLAS, 48 pocillos, con sensores ópticos de biomasa, pH, DO, fluorescencia y control de pH, temperatura, gaseo y alimentación                                                                                                                    | SRC-002 (EV07–EV11)                            | Candidato                               |
| `SartoriusBIOSTATB_5L`   | Individuo de `StirredTankBioreactor`             | Biorreactor Sartorius BIOSTAT B en escala de 5 L (volumen de trabajo 0.6–5 L); con sensores de pH, pO₂, temperatura, espuma, nivel y sustrato; agitación 20–1500 rpm                                                                                                                                           | SRC-006 (EV12–EV18)                            | Candidato                               |
| `SartoriusBIOSTATB_10L`  | Individuo de `StirredTankBioreactor`             | Biorreactor Sartorius BIOSTAT B en escala de 10 L (volumen de trabajo 1.5–10 L); agitación 20–800 rpm                                                                                                                                                                                                          | SRC-006 (EV12, EV15)                           | Candidato                               |

---

## 5. Relaciones candidatas con dominio y rango sugeridos

| Relación candidata           | Dominio sugerido        | Rango sugerido                                                            | Significado                                                                        | Evidencia (ID)                                 | Tipo de evidencia                  | Estado                            |
| ---------------------------- | ----------------------- | ------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ---------------------------------------------- | ---------------------------------- | --------------------------------- |
| `hasAerationSystem`          | `Bioreactor`            | `AerationSystem`                                                          | El biorreactor tiene un sistema activo de entrada/salida de gas                    | ALC02-EV01, ALC02-EV18                         | Explícita                          | Candidato                         |
| `hasSterileBarrier`          | `Bioreactor`            | `SterilizationSystem`                                                     | El biorreactor provee contención estéril activa                                    | ALC02-EV01, ALC02-EV23                         | Explícita / Inferida               | Candidato                         |
| `hasSensor`                  | `Bioreactor`            | `ProcessSensor`                                                           | El biorreactor tiene al menos un sensor de proceso integrado                       | ALC02-EV03, ALC02-EV04, ALC02-EV07, ALC02-EV13 | Explícita                          | Candidato                         |
| `hasActuator`                | `Bioreactor`            | `ProcessActuator`                                                         | El biorreactor tiene al menos un actuador de control                               | ALC02-EV04, ALC02-EV08                         | Explícita                          | Candidato                         |
| `monitorsVariable`           | `ProcessSensor`         | `ProcessVariable` (pH, DO, temperatura, biomasa, espuma, nivel, sustrato) | Un sensor mide una variable específica de proceso en tiempo real                   | ALC02-EV07, ALC02-EV13                         | Explícita                          | Candidato                         |
| `controlsVariable`           | `ProcessActuator`       | `ProcessVariable`                                                         | Un actuador ajusta una variable de proceso en respuesta a señal del sensor         | ALC02-EV04, ALC02-EV08                         | Explícita                          | Candidato                         |
| `requiresCapability`         | `Bioreactor`            | `ActiveProcessControl`                                                    | Ser biorreactor implica la capacidad de control activo de variables fisicoquímicas | ALC02-EV03, ALC02-EV04, ALC02-EV05             | Explícita                          | Candidato                         |
| `hasCapability`              | `Bioreactor`            | `RealTimeProcessMonitoring`                                               | El biorreactor instrumentado posee monitoreo en tiempo real (el matraz no)         | ALC02-EV06                                     | Explícita                          | Candidato                         |
| `lacksCapability`            | `ShakeFlask`            | `RealTimeProcessMonitoring`                                               | El matraz de agitación carece de monitoreo en tiempo real                          | ALC02-EV06                                     | Explícita                          | Candidato                         |
| `lacksCapability`            | `ShakeFlask`            | `ControllableGasLiquidMassTransfer`                                       | El matraz carece de control confiable de transferencia gas-líquido                 | ALC02-EV20, ALC02-EV21                         | Explícita                          | Candidato                         |
| `hasLimitation`              | `ShakeFlask`            | `LowGasLiquidMassTransfer`                                                | El matraz tiene capacidad limitada de transferencia gas-líquido                    | ALC02-EV20                                     | Explícita                          | Candidato                         |
| `achievesOTR`                | `StirredTankBioreactor` | `OxygenTransferRate`                                                      | Un STR logra tasas OTR cuantificadas de 100–150 mmol/L/h                           | ALC02-EV19                                     | Explícita                          | Candidato                         |
| `hasWorkingVolume`           | `Bioreactor`            | `WorkingVolume`                                                           | El biorreactor opera dentro de un rango de volúmenes definido                      | ALC02-EV10, ALC02-EV12                         | Explícita                          | Candidato                         |
| `hasAgitationRange`          | `Bioreactor`            | `AgitationRange` (rpm)                                                    | El biorreactor tiene un rango operativo de velocidad de agitación                  | ALC02-EV15                                     | Explícita                          | Candidato                         |
| `hasTemperatureControlRange` | `Bioreactor`            | `TemperatureRange` (°C)                                                   | El biorreactor controla temperatura dentro de un rango definido                    | ALC02-EV14                                     | Explícita                          | Candidato                         |
| `enablesSterilization`       | `SterilizationSystem`   | `AsepticCondition`                                                        | El sistema de esterilización garantiza condiciones asépticas                       | ALC02-EV16, ALC02-EV23                         | Explícita / Inferida               | Candidato — parcialmente inferido |
| `hasGasSupply`               | `Bioreactor`            | `GasType` (aire, O₂, CO₂, N₂)                                             | El biorreactor recibe suministro de gases específicos                              | ALC02-EV18                                     | Explícita                          | Candidato                         |
| `supportsOperationMode`      | `Bioreactor`            | `OperationMode` (batch, fed-batch, bolus, continuo)                       | El biorreactor soporta distintos modos de operación                                | ALC02-EV11                                     | Explícita (solo para BioLector XT) | Candidato                         |
| `conformsTo`                 | `Bioreactor`            | `ASME_BPE_2022`                                                           | Equipos de bioprocesos en contexto biofarmacéutico se diseñan según ASME BPE       | ALC02-EV22                                     | Explícita                          | Candidato                         |
| `isSubclassOf`               | `Bioreactor`            | `CultureVessel`                                                           | El biorreactor es un tipo especializado de recipiente de cultivo                   | ALC02-EV01                                     | Explícita                          | Candidato                         |
| `isSubclassOf`               | `ShakeFlask`            | `CultureVessel`                                                           | El matraz de agitación es un recipiente de cultivo no instrumentado                | ALC02-EV06, ALC02-EV20                         | Inferida                           | Candidato                         |

---

## 6. Triadas RDF candidatas

Las triadas se presentan con formato `Sujeto → Predicado → Objeto`, indicando soporte, fuente y estado.

```
# GRUPO A — Definición y jerarquía de clases

T01: Bioreactor → rdf:type → owl:Class
     Soporte: SRC-001 (EV01, EV02)
     Estado: Soportada

T02: Bioreactor → rdfs:subClassOf → CultureVessel
     Soporte: SRC-001 (EV01) — "Bioreactors are culture vessels..."
     Estado: Soportada

T03: ShakeFlask → rdfs:subClassOf → CultureVessel
     Soporte: SRC-005 (EV06), SRC-007 (EV20) — diferenciación explícita
     Estado: Parcialmente soportada (inferida; el corpus no usa "subClassOf" pero establece la distinción)

T04: InstrumentedBioreactor → rdfs:subClassOf → Bioreactor
     Soporte: SRC-004 (EV04), SRC-005 (EV06)
     Estado: Parcialmente soportada — requiere validación experta

T05: StirredTankBioreactor → rdfs:subClassOf → Bioreactor
     Soporte: SRC-007 (EV19, EV21)
     Estado: Soportada

T06: MicroBioreactor → rdfs:subClassOf → Bioreactor
     Soporte: SRC-002 (EV07, EV10)
     Estado: Soportada

---

# GRUPO B — Capacidades y requisitos mínimos del biorreactor

T07: Bioreactor → requiresCapability → ActiveProcessControl
     Soporte: SRC-001 (EV03), SRC-004 (EV04, EV05)
     Estado: Soportada

T08: Bioreactor → hasCapability → RealTimeProcessMonitoring
     Soporte: SRC-005 (EV06), SRC-004 (EV04)
     Estado: Soportada

T09: Bioreactor → hasSterileBarrier → SterilizationSystem
     Soporte: SRC-001 (EV01), SRC-003 (EV23)
     Estado: Parcialmente soportada — inferida del diseño "cleanable and sterilizable"

T10: Bioreactor → hasAerationSystem → GasInflowOutflowSystem
     Soporte: SRC-001 (EV01) — "air inflow and outflow systems"
     Estado: Soportada

T11: Bioreactor → hasDesignRequirement → Cleanability
     Soporte: SRC-003 (EV23)
     Estado: Parcialmente soportada — fragmento de scan parcial ASME BPE-2022

T12: Bioreactor → hasDesignRequirement → Sterilizability
     Soporte: SRC-003 (EV23)
     Estado: Parcialmente soportada — fragmento de scan parcial ASME BPE-2022

---

# GRUPO C — Distinción biorreactor / matraz de agitación

T13: ShakeFlask → lacksCapability → RealTimeProcessMonitoring
     Soporte: SRC-005 (EV06) — explícito
     Estado: Soportada

T14: ShakeFlask → lacksCapability → ControllableGasLiquidMassTransfer
     Soporte: SRC-007 (EV21) — explícito
     Estado: Soportada

T15: ShakeFlask → hasLimitation → LowGasLiquidMassTransfer
     Soporte: SRC-007 (EV20) — "limited gas-liquid mass transfer capacities"
     Estado: Soportada

T16: StirredTankBioreactor → achievesOTR → "100-150 mmol/L/h"
     Soporte: SRC-007 (EV19) — explícito y cuantificado
     Estado: Soportada

---

# GRUPO D — BioLector XT (individuo)

T17: BioLectorXT → rdf:type → MicroBioreactor
     Soporte: SRC-002 (EV07) — "microbioreactor"
     Estado: Soportada

T18: BioLectorXT → hasWorkingVolume → "800-2400 µL"
     Soporte: SRC-002 (EV10)
     Estado: Soportada

T19: BioLectorXT → hasSensor → BiomassSensor
     Soporte: SRC-002 (EV07)
     Estado: Soportada

T20: BioLectorXT → hasSensor → pHSensor
     Soporte: SRC-002 (EV07)
     Estado: Soportada

T21: BioLectorXT → hasSensor → DissolvedOxygenSensor
     Soporte: SRC-002 (EV07)
     Estado: Soportada

T22: BioLectorXT → hasSensor → FluorescenceSensor
     Soporte: SRC-002 (EV07)
     Estado: Soportada

T23: BioLectorXT → hasActuator → pHController
     Soporte: SRC-002 (EV08)
     Estado: Soportada

T24: BioLectorXT → hasActuator → TemperatureController
     Soporte: SRC-002 (EV08)
     Estado: Soportada

T25: BioLectorXT → hasActuator → GasController
     Soporte: SRC-002 (EV08, EV09)
     Estado: Soportada

T26: BioLectorXT → hasGasControlRange → "O2: 0-100%"
     Soporte: SRC-002 (EV09)
     Estado: Soportada

T27: BioLectorXT → hasGasControlRange → "CO2: 0-12%"
     Soporte: SRC-002 (EV09)
     Estado: Soportada

T28: BioLectorXT → supportsOperationMode → FedBatchMode
     Soporte: SRC-002 (EV11)
     Estado: Soportada

T29: BioLectorXT → supportsOrganismType → AerobicOrganism
     Soporte: SRC-002 (EV24)
     Estado: Soportada

T30: BioLectorXT → supportsOrganismType → AnaerobicOrganism
     Soporte: SRC-002 (EV24)
     Estado: Soportada

---

# GRUPO E — BIOSTAT B Sartorius (individuos 5 L y 10 L)

T31: SartoriusBIOSTATB_5L → rdf:type → StirredTankBioreactor
     Soporte: SRC-006 (EV25) — "fermenter | bioreactor"
     Estado: Soportada

T32: SartoriusBIOSTATB_5L → hasWorkingVolume → "0.6-5 L"
     Soporte: SRC-006 (EV12)
     Estado: Soportada — verificar con manual oficial Sartorius

T33: SartoriusBIOSTATB_10L → hasWorkingVolume → "1.5-10 L"
     Soporte: SRC-006 (EV12)
     Estado: Soportada — verificar con manual oficial Sartorius

T34: SartoriusBIOSTATB_5L → hasAgitationRange → "20-1500 rpm"
     Soporte: SRC-006 (EV15)
     Estado: Soportada — verificar con manual oficial Sartorius

T35: SartoriusBIOSTATB_10L → hasAgitationRange → "20-800 rpm"
     Soporte: SRC-006 (EV15)
     Estado: Soportada — verificar con manual oficial Sartorius

T36: SartoriusBIOSTATB → hasTemperatureControlRange → "0-80 °C"
     Soporte: SRC-006 (EV14)
     Estado: Soportada — verificar con manual oficial Sartorius

T37: SartoriusBIOSTATB → hasSensor → pHSensor
     Soporte: SRC-006 (EV13)
     Estado: Soportada — verificar con manual oficial Sartorius

T38: SartoriusBIOSTATB → hasSensor → pO2Sensor
     Soporte: SRC-006 (EV13)
     Estado: Soportada — verificar con manual oficial Sartorius

T39: SartoriusBIOSTATB → hasSensor → TemperatureSensor
     Soporte: SRC-006 (EV13)
     Estado: Soportada — verificar con manual oficial Sartorius

T40: SartoriusBIOSTATB → hasSensor → FoamSensor
     Soporte: SRC-006 (EV13)
     Estado: Soportada — verificar con manual oficial Sartorius

T41: SartoriusBIOSTATB → hasSensor → LevelSensor
     Soporte: SRC-006 (EV13)
     Estado: Soportada — verificar con manual oficial Sartorius

T42: SartoriusBIOSTATB → hasSensor → SubstrateSensor
     Soporte: SRC-006 (EV13)
     Estado: Soportada — verificar con manual oficial Sartorius

T43: SartoriusBIOSTATB → hasComponent → PorousSparger
     Soporte: SRC-006 (EV17)
     Estado: Soportada — verificar con manual oficial Sartorius

T44: SartoriusBIOSTATB → hasComponent → LTypeSparger
     Soporte: SRC-006 (EV17)
     Estado: Soportada — verificar con manual oficial Sartorius

T45: SartoriusBIOSTATB → hasGasSupply → N2
     Soporte: SRC-006 (EV18) — relevante para control anaeróbico
     Estado: Soportada — verificar con manual oficial Sartorius

T46: SartoriusBIOSTATB → hasMaxGasFlowRate → "20 lpm"
     Soporte: SRC-006 (EV18)
     Estado: Soportada — verificar con manual oficial Sartorius

T47: SartoriusBIOSTATB → enablesSterilization → SteamInPlaceProcess
     Soporte: SRC-006 (EV16) — inferido de "−1 to +2.5 barg @ 150 °C"
     Estado: Parcialmente soportada — inferida; requiere validación experta

T48: SartoriusBIOSTATB → conformsTo → ASME_BPE_2022
     Soporte: SRC-003 (EV22) — inferida; el corpus no vincula explícitamente BIOSTAT B con ASME BPE
     Estado: Requiere validación experta — no establecido directamente en el corpus
```

---

## 7. Sinónimos documentados

| Término principal (ontología) | Sinónimos o variantes extraídas del corpus                                | Idioma | Fuente                                                                                          |
| ----------------------------- | ------------------------------------------------------------------------- | ------ | ----------------------------------------------------------------------------------------------- |
| `Bioreactor`                  | Fermenter; Bioreaction vessel; Culture vessel (en contexto instrumentado) | EN     | SRC-001, SRC-006                                                                                |
| `Biorreactor`                 | Fermentador; Recipiente de bioproceso                                     | ES     | No establecido en el corpus suministrado (documentos están en inglés)                           |
| `DissolvedOxygen` (DO)        | Dissolved oxygen concentration; pO2; dissolved O2; oxygen saturation      | EN     | SRC-002, SRC-004, SRC-006                                                                       |
| `ShakeFlask`                  | Shaker flask; Erlenmeyer flask                                            | EN     | SRC-005, SRC-007                                                                                |
| `StirredTankBioreactor`       | STR; Stirred tank reactor; Stirred-tank bioreactor                        | EN     | SRC-007                                                                                         |
| `OxygenTransferRate`          | OTR; Gas-liquid mass transfer (en contexto de O₂)                         | EN     | SRC-007                                                                                         |
| `SterilizationInPlace`        | SIP                                                                       | EN     | No establecido en el corpus suministrado (inferido del rango de temperatura/presión de SRC-006) |
| `FedBatchMode`                | Fed-batch; fed-batch cultivation                                          | EN     | SRC-002                                                                                         |
| `AerationSystem`              | Air inflow and outflow system; gas sparger system                         | EN     | SRC-001, SRC-006                                                                                |
| `RealTimeProcessMonitoring`   | Online measurement; time-resolved monitoring; non-invasive monitoring     | EN     | SRC-002, SRC-005                                                                                |

---

## 8. Vacíos del corpus

Los siguientes elementos no pueden ser respondidos o formalizados con el corpus suministrado:

| ID Vacío | Descripción                                                                                                                                                                                                                                                      | Impacto ontológico                                                                                                                       | Acción recomendada                                                                             |
| -------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------- |
| VAC-01   | El corpus no contiene el texto completo de ASME BPE-2022 (sección GR-1, definiciones formales). SRC-003 solo incluye fragmentos de la descripción pública del estándar                                                                                           | No es posible extraer la definición normativa formal de "bioprocessing vessel" ni los criterios técnicos específicos del estándar        | Adquirir ASME BPE-2022 y suministrar la sección GR-1 al corpus                                 |
| VAC-02   | No existe en el corpus ninguna definición formal de biorreactor emitida por FDA, EMA o ISO                                                                                                                                                                       | La base ontológica carece de anclaje regulatorio explícito para el concepto `Bioreactor`                                                 | Incorporar FDA 21 CFR Part 600 y EMA CHMP/BWP guidelines al corpus                             |
| VAC-03   | El corpus no establece un **umbral mínimo cuantitativo** (número de sensores, variables controladas, etc.) que defina normativamente cuándo un sistema pasa a ser clasificado como biorreactor                                                                   | No es posible formalizar una restricción OWL `owl:minCardinality` basada en evidencia del corpus                                         | Solicitar definición experta o norma adicional                                                 |
| VAC-04   | SRC-006 proviene de una fuente secundaria (A\*SEF, repositorio institucional de Singapur) y no del manual oficial de Sartorius. Las especificaciones del BIOSTAT B (sensores, rangos, volúmenes) no han sido verificadas contra el documento primario            | Los valores numéricos de las triadas T32–T46 tienen confianza reducida                                                                   | Adquirir o descargar la documentación oficial de Sartorius (broch-biostat-b o equivalente)     |
| VAC-05   | La "Technical Data Sheet" del BioLector XT es referenciada en SRC-002 pero no fue incluida en el corpus                                                                                                                                                          | Podrían existir especificaciones adicionales o correcciones en la hoja de datos oficial                                                  | Solicitar la Technical Data Sheet de m2p-labs/Beckman Coulter e incorporarla al corpus         |
| VAC-06   | El corpus no establece si la esterilización in situ (SIP) del BIOSTAT B es una característica estándar o una opción; el rango de operación a 150 °C se inferió como compatible con SIP pero no se afirma explícitamente                                          | La triada T47 permanece como inferencia no confirmada                                                                                    | Verificar en manual oficial de Sartorius                                                       |
| VAC-07   | El corpus no documenta las características del Sartorius 5 L y 10 L cuando son referidos como modelos independientes del proyecto (vs. el BIOSTAT B genérico). No queda claro si "Sartorius 5 L" y "Sartorius 10 L" son el BIOSTAT A, el BIOSTAT B u otro modelo | Los individuos `SartoriusBIOSTATB_5L` y `SartoriusBIOSTATB_10L` podrían no corresponder a los equipos exactos del proyecto               | Confirmar con el equipo de investigación cuáles son los modelos Sartorius exactos del proyecto |
| VAC-08   | El corpus no especifica qué tipo de control de bucle (PID, on/off, modelo predictivo) usa cada equipo                                                                                                                                                            | No es posible instanciar `ControlLoop` con atributos de tipo de control                                                                  | Incorporar manuales de operación que describan los algoritmos de control                       |
| VAC-09   | El término "redox value" aparece en SRC-001 (EV03) como parámetro monitoreable, pero ningún otro documento del corpus menciona sensores redox en BioLector XT o BIOSTAT B                                                                                        | No es posible confirmar si `RedoxSensor` es un componente de los equipos del proyecto                                                    | Verificar en fichas técnicas oficiales de cada equipo                                          |
| VAC-10   | El corpus no provee evidencia sobre las fases del proceso (batch, fed-batch, cosecha), los eventos de alarma ni los modos de falla de los equipos                                                                                                                | Secciones de la ontología relacionadas con `ProcessPhase`, `AlarmEvent` y `FaultCondition` no pueden construirse a partir de este corpus | Incorporar manuales de operación y SOPs al corpus en una consulta posterior                    |

---

## 9. Estado final

| Criterio                                                    | Estado                                                                                                                                                                                                      | Justificación basada en el corpus                                                                                                                                                                                                                                                                                                                                                                 |
| ----------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Estado de la respuesta**                                  | **Parcialmente soportada**                                                                                                                                                                                  | Las cuatro características mínimas identificadas (contención estéril, monitoreo en tiempo real, control activo de variables y gestión de transferencia de masa) están respaldadas por evidencia explícita y convergente de al menos dos fuentes del corpus cada una. Sin embargo, no existe en el corpus una norma accesible que establezca un umbral formal y cuantitativo para la clasificación |
| **Cobertura de BioLector XT**                               | **Soportada**                                                                                                                                                                                               | SRC-002 provee evidencia explícita de sensores, actuadores, volúmenes, modos de operación y parámetros controlados                                                                                                                                                                                                                                                                                |
| **Cobertura de Sartorius 5 L / 10 L**                       | **Parcialmente soportada**                                                                                                                                                                                  | SRC-006 provee valores técnicos relevantes, pero la fuente es secundaria y no se puede confirmar la correspondencia exacta con los modelos del proyecto                                                                                                                                                                                                                                           |
| **Cobertura del concepto `Bioreactor` (criterios mínimos)** | **Parcialmente soportada**                                                                                                                                                                                  | El corpus establece criterios cualitativos robustos pero no un umbral normativo formal                                                                                                                                                                                                                                                                                                            |
| **Confianza general en las triadas**                        | **Media-Alta**                                                                                                                                                                                              | Las triadas del Grupo D (BioLector XT) tienen alta confianza; las del Grupo E (Sartorius) tienen confianza media hasta verificación con manual oficial; las del Grupo A-C tienen alta confianza conceptual pero requieren validación experta para formalización en OWL                                                                                                                            |
| **Próxima acción obligatoria**                              | Suministrar al corpus: (1) manual oficial Sartorius BIOSTAT B; (2) Technical Data Sheet BioLector XT; (3) texto de sección GR-1 de ASME BPE-2022; (4) confirmación del modelo Sartorius exacto del proyecto | —                                                                                                                                                                                                                                                                                                                                                                                                 |
