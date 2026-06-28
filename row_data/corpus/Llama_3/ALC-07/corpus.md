# Extracción condicionada por corpus – ALC-07

## 1) ID y pregunta

**ALC-07:** ¿Qué relaciones básicas debe tener cada biorreactor con sensores, actuadores, variables operativas, fases del proceso y eventos?

## 2) Respuesta basada en evidencia

Trabajando exclusivamente con los fragmentos suministrados:

- **Variables operativas monitoreadas:** el BioLector XT realiza "onlinemonitoring of common cultivation parameters such as biomass, pH, dissolved oxygen (DO) and fluorescence" y "enables realtime evaluation of biomass, fluorescence, pH, DO, and other key cultivation parameters". Las MTPs "enable online measurement of biomass, fluorescences, pH and DO".
- **Control:** la tecnología microfluídica "supports simultaneous pH control and feeding"; el control de pH es "By acid or/and alkali" y en Biostat B "by automatic acid and base addition or by CO₂ aeration".
- **Actuadores / módulos:** la torre de control "contains both the aeration, pump and temperature control modules"; "Up to four internal pumps can be selected per vessel"; agitación "100 rpm – 1500 rpm"; gaseo seleccionable "five different gassing modes" con "flowrates between 5 50 mL/min".
- **Sensores / instrumentos:** se documentan rangos de medida: "Temperature Pt100 | 0– 150 °C"; "Dissolved oxygen... | 0– 100%"; "pH... | 2– 12 pH"; filtros preinstalados "Biomass, Riboflavin, pH and DO".
- **Fases / modos de proceso:** "Process Modes | - Batch | - Fedbatch | - Continuous | - Perfusion"; condiciones de cultivo "aerobic, anaerobic and phototrophic".
- **Eventos:** el sistema dispone de "Potentialfree (common) alarm contact" y "Remote Alarming".

No se establecen en el corpus relaciones explícitas con la palabra "sensor" o "actuador", ni taxonomías completas de eventos.

## 3) Tabla de afirmaciones y evidencia

| ID  | Afirmación                                                                  | Fragmento                                                                       | Fuente (sección)          | Concepto/Relación/Triada candidata                                                 | Tipo                                         | Confianza    | Validación experta |
| --- | --------------------------------------------------------------------------- | ------------------------------------------------------------------------------- | ------------------------- | ---------------------------------------------------------------------------------- | -------------------------------------------- | ------------ | ------------------ |
| A01 | BioLector XT monitorea online biomasa, pH, DO y fluorescencia               | "onlinemonitoring... biomass, pH, dissolved oxygen (DO) and fluorescence"       | SRC-001 Introducción      | Bioreactor -> monitors -> OperationalVariable                                      | Explícita                                    | Alta         | No                 |
| A02 | MTPs permiten medición online de biomasa, pH, DO                            | "enable online measurement of biomass, fluorescences, pH and DO"                | SRC-004 Online Monitoring | MTP -> enablesMeasurement -> {biomass, pH, DO}                                     | Explícita                                    | Alta         | No                 |
| A03 | Tecnología microfluídica soporta control simultáneo de pH y alimentación    | "supports simultaneous pH control and feeding"                                  | SRC-004                   | MicrofluidicTechnology -> supports -> {pHControl, Feeding}                         | Explícita                                    | Alta         | No                 |
| A04 | Evaluación en tiempo real para cultivos aerobios, anaerobios y fototróficos | "realtime evaluation... for aerobic, anaerobic and phototrophic microorganisms" | SRC-005                   | Bioreactor -> operatesUnder -> CultivationCondition                                | Explícita                                    | Alta         | No                 |
| A05 | Control de pH por ácido y/o álcali                                          | "pH control By acid or/and alkali"                                              | SRC-006                   | pHControl -> uses -> {Acid, Alkali}                                                | Explícita                                    | Alta         | No                 |
| A06 | Frecuencias de agitación 100–1500 rpm                                       | "Shaking frequencies 100 rpm – 1500 rpm"                                        | SRC-007                   | Bioreactor -> hasActuatorSetting -> ShakingFrequency                               | Explícita                                    | Alta         | No                 |
| A07 | Filtros preinstalados: Biomasa, Riboflavina, pH, DO                         | "Preinstalled filters Biomass, Riboflavin, pH and DO"                           | SRC-008                   | MeasurementSystem -> includesFilter -> {Biomass, pH, DO}                           | Explícita                                    | Alta         | No                 |
| A08 | Vasos disponibles 1 L, 2 L, 5 L, 10 L                                       | "vessel is available in four different volumes: 1 L, 2 L, 5 L and 10 L"         | SRC-009                   | Bioreactor -> hasVolumeVariant -> {1L,2L,5L,10L}                                   | Explícita                                    | Alta         | No                 |
| A09 | Modos de proceso: Batch, Fedbatch, Continuous, Perfusion                    | "Process Modes - Batch - Fedbatch - Continuous - Perfusion" | SRC-010            | Bioreactor -> operatesIn -> ProcessMode | Explícita | Alta | No  |
| A10 | Torre contiene módulos de aeración, bomba y control temperatura             | "contains both the aeration, pump and temperature control modules"              | SRC-011                   | ControlTower -> contains -> {AerationModule, PumpModule, TemperatureControlModule} | Explícita                                    | Alta         | No                 |
| A11 | Medición temperatura Pt100 0–150°C                                          | "Temperature Pt100  0– 150 °C"                | SRC-012                                                                            | TemperatureSensor -> measures -> Temperature | Explícita    | Alta               | No                                      |
| A12 | Medición DO 0–100%                                                          | "Dissolved oxygen... 0– 100%"                  | SRC-013                                                                            | DOSensor -> measures -> DissolvedOxygen      | Explícita    | Alta               | No                                      |
| A13 | Medición pH 2–12                                                            | "pH... 2– 12 pH"                 | SRC-014                                                                            | PHSensor -> measures -> pH                   | Explícita    | Alta               | No                                      |
| A14 | Hasta cuatro bombas internas por vaso                                       | "Up to four internal pumps can be selected per vessel"                          | SRC-015                   | Vessel -> hasPump -> Pump (max 4)                                                  | Explícita                                    | Alta         | No                 |
| A15 | Control pH automático por ácido/base o CO2                                  | "Control the pH... by automatic acid and base addition or by CO₂ aeration"      | SRC-016                   | pHControl -> uses -> {Acid, Base, CO2Aeration}                                     | Explícita                                    | Alta         | No                 |
| A16 | Control DO por cascade clásico y avanzado                                   | "Besides classic DO cascade control... advanced DO controller"                  | SRC-017                   | DOControl -> implements -> CascadeControl                                          | Explícita                                    | Media        | Sí                 |
| A17 | Contacto de alarma libre de potencial                                       | "Potentialfree (common) alarm contact"                                          | SRC-018                   | System -> hasComponent -> AlarmContact                                             | Explícita                                    | Alta         | No                 |
| A18 | Alarmas remotas                                                             | "Remote Alarming"                                                               | SRC-019                   | System -> generates -> RemoteAlarm                                                 | Explícita                                    | Media        | Sí                 |
| A19 | Cinco modos de gaseo seleccionables por software                            | "you can choose between five different gassing modes"                           | SRC-002                   | Software -> selects -> GassingMode                                                 | Explícita                                    | Alta         | No                 |
| A20 | Flujos gas 5–50 mL/min seleccionables                                       | "flowrates between 5 50 mL/min can also be selected"                            | SRC-003                   | GassingSystem -> hasFlowRateRange -> 5-50mL/min                                    | Explícita                                    | Alta         | No                 |

## 4) Conceptos candidatos

- **Bioreactor** – mencionado como "BioLector XT microbioreactor", "Biostat B"
- **OperationalVariable** – biomasa, pH, DO/dissolved oxygen, fluorescence, temperature, shaking frequency, flowrate
- **MeasurementCapability** – "online measurement", "realtime evaluation"
- **ControlModule** – aeration module, pump module, temperature control module
- **Pump** – "internal pumps"
- **pHControl** – "pH control"
- **DOControl** – "DO cascade control"
- **ProcessMode** – Batch, Fedbatch, Continuous, Perfusion
- **CultivationCondition** – aerobic, anaerobic, phototrophic
- **Alarm** – "alarm contact", "Remote Alarming"
- **GassingMode** – "gassing modes"
- **MicrofluidicTechnology** – soporta control y feeding

## 5) Relaciones candidatas con dominio y rango

| Relación           | Dominio sugerido       | Rango sugerido       | Base     |
| ------------------ | ---------------------- | -------------------- | -------- |
| monitors           | Bioreactor             | OperationalVariable  | A01, A02 |
| enablesMeasurement | MTP                    | OperationalVariable  | A02      |
| supportsControl    | MicrofluidicTechnology | {pHControl, Feeding} | A03      |
| operatesUnder      | Bioreactor             | CultivationCondition | A04      |
| usesActuator       | Bioreactor             | ControlModule        | A10      |
| containsModule     | ControlTower           | ControlModule        | A10      |
| hasPump            | Vessel                 | Pump                 | A14      |
| measures           | MeasurementDevice      | OperationalVariable  | A11-A13  |
| controlsBy         | pHControl              | {Acid, Alkali, CO2}  | A05, A15 |
| implements         | DOControl              | CascadeControl       | A16      |
| operatesIn         | Bioreactor             | ProcessMode          | A09      |
| hasAlarm           | System                 | AlarmContact         | A17      |
| generates          | System                 | RemoteAlarm          | A18      |
| selectsMode        | Software               | GassingMode          | A19      |

## 6) Triadas RDF candidatas

- Bioreactor -> monitors -> pH — SRC-001 — soportada
- Bioreactor -> monitors -> DissolvedOxygen — SRC-001 — soportada
- Bioreactor -> monitors -> Biomass — SRC-004 — soportada
- MicrofluidicTechnology -> supports -> pHControl — SRC-004 — soportada
- MicrofluidicTechnology -> supports -> Feeding — SRC-004 — soportada
- ControlTower -> contains -> AerationModule — SRC-011 — soportada
- ControlTower -> contains -> PumpModule — SRC-011 — soportada
- ControlTower -> contains -> TemperatureControlModule — SRC-011 — soportada
- Vessel -> hasPump -> Pump — SRC-015 — soportada (máx 4 no expresado en triada)
- pHControl -> uses -> Acid — SRC-006 — soportada
- pHControl -> uses -> Alkali — SRC-006 — soportada
- Bioreactor -> operatesIn -> Fedbatch — SRC-010 — soportada
- System -> hasComponent -> AlarmContact — SRC-018 — soportada

## 7) Sinónimos documentados

| Término principal | Variante                   | Fuente                          |
| ----------------- | -------------------------- | ------------------------------- |
| dissolved oxygen  | DO                         | SRC-001 "dissolved oxygen (DO)" |
| Fedbatch          | Fed-batch (forma en tabla) | SRC-010                         |
| pH control        | pHControl                  | SRC-004, SRC-006                |
| Remote Alarming   | RemoteAlarm                | SRC-019                         |

## 8) Vacíos del corpus

- No se define explícitamente la clase "Sensor" ni "Actuador"; solo se listan dispositivos y rangos.
- No hay descripción de la relación directa "bioreactor hasSensor" – solo capacidades de medición.
- No se especifican eventos distintos de alarmas (fallas, advertencias, estados).
- No hay equivalencias funcionales entre escalas (microplaca vs 5 L vs 10 L).
- No se describen variables operativas como "feeding rate" con rangos.
- No se define taxonomía de "gassing modes" (nombres de los cinco modos).

## 9) Estado final

- **Soporte de la respuesta:** parcialmente soportado
- **Motivo:** el corpus suministra evidencia explícita para monitoreo de variables, módulos de control, modos de proceso y alarmas, pero no establece de forma explícita las relaciones ontológicas genéricas "hasSensor", "hasActuator" ni una taxonomía de eventos.
