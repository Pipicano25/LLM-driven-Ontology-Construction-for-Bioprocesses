## 1) ID y pregunta

- **ID:** ALC-06
- **Pregunta:** ¿Qué propiedades generales deben describir cualquier biorreactor del proyecto, independientemente de su escala o volumen?

## 2) Respuesta basada en evidencia

El corpus documenta que todo biorreactor debe describirse por:

- **Volumen operativo**: BioLector XT 800–2400 µL; Sartorius 5 L 0,6–5 L y 10 L 1,5–10 L (totales 6,6 L y 13 L).
- **Control térmico**: BioLector 8 °C bajo ambiente a 50 °C; Sartorius 0–80 °C (sensor Pt100 0–150 °C).
- **Agitación**: BioLector 100–1500 rpm; Sartorius 5 L 20–1500 rpm, 10 L 20–800 rpm.
- **Medida**: pH y DO 0–100% en ambos; BioLector añade biomasa online; Sartorius especifica pH 2–12.
- **Control de pH**: por ácido/álcali (BioLector) y por ácido/base o CO₂ (Sartorius).
- **Aireación**: gases controlables (BioLector: CO₂, O₂; Sartorius: Air, O₂, N₂, CO₂).
- **Materiales**: Sartorius – vidrio borosilicato, acero AISI 316L, EPDM; BioLector – tecnología desechable.
- **Modos de proceso**: documentados para Sartorius como batch, fed-batch, continuous, perfusion.
- **Interfaz**: Ethernet (BioLector) y conectividad a BioPAT® MFCS/SCADA (Sartorius).

Propiedades no documentadas para ambos sistemas en el corpus: límites de presión, alarmas, fallas, validación de esterilidad.

## 3) Tabla de afirmaciones y evidencia

| Afirmación                          | Texto/fragmento evidencia                                                                       | Fuente (página/sección)             | Concepto/relación/triada candidata               | Tipo      | Confianza | Validación experta |
| ----------------------------------- | ----------------------------------------------------------------------------------------------- | ----------------------------------- | ------------------------------------------------ | --------- | --------- | ------------------ |
| Medición online de biomasa, pH y DO | "online monitoring of common cultivation parameters such as biomass, pH, dissolved oxygen (DO)" | DOC-01 – Introducción               | Sensor -> measuresParameter -> {Biomass, pH, DO} | explícita | alta      | no                 |
| Volumen trabajo BioLector           | "Working volume: 800 – 2400 µL"                                                                 | DOC-02 – System Performance         | CultureVessel -> hasWorkingVolumeRange           | explícita | alta      | no                 |
| Volumen trabajo/total Sartorius     | "Working volume 0.6–5 1.5–10 Total volume 6.6 13"                                               | DOC-03 – Especificaciones Univessel | hasWorkingVolumeRange / hasTotalVolume           | explícita | alta      | no                 |
| Rango temperatura BioLector         | "Temperature, minimum... 8 °C below ambient temperature Temperature, maximum 50 °C"             | DOC-02 – Technical Specifications   | hasTemperatureControlRange                       | explícita | alta      | no                 |
| Rango temperatura Sartorius         | "Temperature Pt100 0–150°C (temperature control 0–80°C)"                                        | DOC-04 – Process Control/Sensors    | hasTemperatureControlRange                       | explícita | alta      | no                 |
| Agitación BioLector                 | "Shaking frequencies 100 rpm – 1500 rpm"                                                        | DOC-02                              | AgitationSystem -> hasSpeedRange                 | explícita | alta      | no                 |
| Agitación Sartorius                 | "5L Glass: 20 – 1,500 rpm 10L Glass: 20 – 800 rpm"                                              | DOC-04 – Especificaciones           | hasSpeedRange                                    | explícita | alta      | no                 |
| Medida pH BioLector                 | "Measurement range pH ~5.0 – 7.5 or ~4 – 6 (low pH module)"                                     | DOC-02                              | pHSensor -> measures                             | explícita | alta      | no                 |
| Medida pH Sartorius                 | "pH, reusable... 2–12 pH 0.01 pH"                                                               | DOC-04                              | pHSensor -> measures                             | explícita | alta      | no                 |
| Medida DO ambos                     | "Measurement range DO 0 – 100% oxygen saturation" / "Dissolved oxygen... 0–100% 0.1%"           | DOC-02 / DOC-04                     | DOSensor -> measures                             | explícita | alta      | no                 |
| Control pH BioLector                | "pH control By acid or/and alkali"                                                              | DOC-02                              | Bioreactor -> controlsParameter -> pH            | explícita | alta      | no                 |
| Control pH Sartorius                | "Control the pH... by automatic acid and base addition or by CO₂ aeration"                      | DOC-03 – pH Control                 | controlsParameter -> pH                          | explícita | alta      | no                 |
| Gases Sartorius                     | "Air O2 N2 CO2" (tabla aeration)                                                                | DOC-03 – Aeration Strategies        | AerationSystem -> usesGasType                    | explícita | alta      | no                 |
| Atmósfera BioLector                 | "Controlled gas atmosphere (CO2, O2)"                                                           | DOC-02                              | usesGasType                                      | explícita | media     | sí                 |
| Materiales Sartorius                | "Materials... Borosilicate glass, stainless steel AISI 316L, EPDM"                              | DOC-03                              | CultureVessel -> hasMaterial                     | explícita | alta      | no                 |
| Tecnología desechable BioLector     | "Application mode Disposable technology"                                                        | DOC-02                              | hasConstructionMode                              | explícita | media     | sí                 |
| Modos proceso Sartorius             | "Process Modes - Batch - Fedbatch - Continuous - Perfusion"                                     | DOC-03                              | supportsProcessMode                              | explícita | alta      | no                 |
| Interfaz Ethernet                   | "Interface Ethernet"                                                                            | DOC-02                              | hasDataInterface                                 | explícita | alta      | no                 |
| Conectividad SCADA                  | "Easily connect... to BioPAT® MFCS or third party supervisory software"                         | DOC-04                              | hasDataInterface                                 | explícita | alta      | no                 |
| Bombas                              | "Choose up to four variable speed... pumps"                                                     | DOC-04                              | hasActuator -> Pump                              | explícita | alta      | no                 |

## 4) Conceptos candidatos

- Bioreactor
- CultureVessel
- WorkingVolumeRange
- TotalVolume
- TemperatureControlRange
- AgitationSystem
- SpeedRange
- Sensor (pHSensor, DOSensor, BiomassSensor, TemperatureSensor)
- AerationSystem
- GasType
- MaterialOfConstruction
- ConstructionMode (Reusable, Disposable)
- ProcessMode
- DataInterface
- Actuator (Pump)

## 5) Relaciones candidatas con dominio y rango sugeridos

| Relación                   | Dominio         | Rango                   | Basada en  |
| -------------------------- | --------------- | ----------------------- | ---------- |
| hasWorkingVolumeRange      | CultureVessel   | WorkingVolumeRange      | A2, A3     |
| hasTotalVolume             | CultureVessel   | TotalVolume             | A3         |
| hasTemperatureControlRange | Bioreactor      | TemperatureControlRange | A4, A5     |
| hasAgitationSystem         | Bioreactor      | AgitationSystem         | A6, A7     |
| hasSpeedRange              | AgitationSystem | SpeedRange              | A6, A7     |
| measuresParameter          | Sensor          | Parameter               | A1, A8-A10 |
| controlsParameter          | Bioreactor      | Parameter               | A11, A12   |
| hasAerationSystem          | Bioreactor      | AerationSystem          | A13, A14   |
| usesGasType                | AerationSystem  | GasType                 | A13, A14   |
| hasMaterial                | CultureVessel   | MaterialOfConstruction  | A15        |
| hasConstructionMode        | Bioreactor      | ConstructionMode        | A16        |
| supportsProcessMode        | Bioreactor      | ProcessMode             | A17        |
| hasDataInterface           | Bioreactor      | DataInterface           | A18, A19   |
| hasActuator                | Bioreactor      | Actuator                | A20        |

## 6) Triadas RDF candidatas

- Bioreactor -> hasWorkingVolumeRange -> "800-2400 µL" — DOC-02
- Bioreactor -> hasWorkingVolumeRange -> "0.6-5 L" — DOC-03
- Bioreactor -> hasTemperatureControlRange -> "0-80 °C" — DOC-04
- Bioreactor -> measuresParameter -> DissolvedOxygen — DOC-01, DOC-04
- Bioreactor -> controlsParameter -> pH — DOC-02, DOC-03
- CultureVessel -> hasMaterial -> "BorosilicateGlass" — DOC-03
- AerationSystem -> usesGasType -> CO2 — DOC-02, DOC-03
- Bioreactor -> supportsProcessMode -> FedBatch — DOC-03
- Bioreactor -> hasDataInterface -> Ethernet — DOC-02

## 7) Sinónimos documentados

| Término             | Variante                          | Fuente         |
| ------------------- | --------------------------------- | -------------- |
| Dissolved oxygen    | DO                                | DOC-01, DOC-04 |
| pH                  | potential of hydrogen (implícito) | DOC-02, DOC-04 |
| Working volume      | volumen de trabajo                | DOC-02, DOC-03 |
| Shaking frequencies | stirrer speed, rpm                | DOC-02, DOC-04 |
| Aeration            | gassing                           | DOC-01, DOC-03 |

## 8) Vacíos del corpus

- **Alarmas, eventos y fallas**: no establecido en el corpus suministrado
- **Límites de presión operativa**: no establecido en el corpus suministrado
- **Material exacto de placas desechables BioLector**: no establecido (solo "Disposable technology")
- **Equivalencias funcionales de kLa entre escalas**: no establecido
- **Validación de esterilidad/autoclavabilidad para 10 L**: no establecido

## 9) Estado final

- **Soportado**: propiedades de volumen, temperatura, agitación, medida/control de pH y DO, aireación, materiales (Sartorius), interfaz
- **Parcialmente soportado**: modos de proceso (solo Sartorius documentado explícitamente), construcción desechable
- **No soportado en corpus**: alarmas, fallas, decisiones, calidad de datos

**Estado general:** parcialmente soportado
