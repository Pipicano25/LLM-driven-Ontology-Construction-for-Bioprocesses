1. ID y pregunta

**ALC-04:** ¿Qué componentes comunes permiten describir estos tres biorreactores en una misma ontología?

2. Respuesta basada en evidencia

Con los fragmentos suministrados, se pueden identificar componentes presentes en BioLector XT y en Biostat B-DCU (5 L y 10 L):

- **Control de temperatura:** BioLector XT "10 – 50 °C" [SRC-001]; Biostat "Temperature Pt100|0–150°C (temperature control 0–80°C)" [SRC-002].
- **Agitación regulable:** BioLector "100 – 1500 rpm" [SRC-001]; Biostat "5L Glass: 20 – 1,500 rpm" y "10L Glass: 20 – 800 rpm" [SRC-002].
- **Medición de pH:** BioLector "pH 4 – 7.5" [SRC-001]; Biostat "pH, reusable Combined measuring electrode|2–12 pH" [SRC-002].
- **Medición de oxígeno disuelto:** ambos "0 – 100 %" [SRC-001][SRC-002].
- **Suministro de gas:** BioLector "1 – 100 % O 2 (optional)" y "0 – 12 % CO 2 (optional)" [SRC-001]; Biostat "Intelligent mass flow controllers with a flow range of 1:200" y "Max. total flow Up to 20 lpm" [SRC-002].
- **Alimentación:** BioLector "FEEDING OPTIONS", "Two feed lines", "Up to 665 pump strokes per hour" [SRC-001]; Biostat "Choose up to four variable speed and up to four fixed speed pumps" [SRC-002].
- **Recipiente de cultivo:** BioLector "48 cultivation wells", "Filling volume: 800 – 1900 μL", "Filling volume: 1000 – 2400 μL" [SRC-001]; Biostat "Connect Univessel® Glass", "1 L, 2 L, 5 L and 10 L" [SRC-002].
- **Uso en misma cadena de escala:** "1 to 2 mL scale in a BioLector XT® ... up to a 5 L bioreactor" y "5 L bioreactor (Biostat B5, Sartorius AG)" [SRC-003].

No establecido en el corpus suministrado: equivalencia de controladores en lazo cerrado, alarmas, sensores de espuma/nivel, o software específico común.

3. Tabla de afirmaciones y evidencia

| Afirmación                                                     | Fragmento de evidencia                                                                                           | Fuente y ubicación                   | Concepto/relación/triada candidata                                    | Tipo evidencia            | Confianza                                                    | Validación experta |
| -------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------- | ------------------------------------ | --------------------------------------------------------------------- | ------------------------- | ------------------------------------------------------------ | ------------------ |
| BioLector XT controla temperatura 10–50°C                      | "10 – 50 °C (min. temp.: 8 °C below ambient temp.)"                                                              | SRC-001, especificaciones            | BioreactorSystem -> hasComponent -> TemperatureControlSystem          | explícita                 | alta                                                         | no                 |
| Biostat B-DCU mide y controla temperatura 0–150°C / 0–80°C     | "Temperature Pt100                                                                                               | 0–150°C (temperature control 0–80°C) 0.1°C" SRC-002, especificaciones | BioreactorSystem -> hasComponent -> TemperatureControlSystem | explícita          | alta | no  |
| Ambos incluyen control térmico                                 | comparación de fragmentos anteriores                                                                             | SRC-001 + SRC-002                    | BioreactorSystem -> hasTemperatureControl -> TemperatureControlSystem | inferida                  | media                                                        | sí                 |
| BioLector XT agita 100–1500 rpm                                | "100 – 1500 rpm (3 mm diameter)"                                                                                 | SRC-001                              | BioreactorSystem -> hasComponent -> AgitationSystem                   | explícita                 | alta                                                         | no                 |
| Biostat 5L agita 20–1500 rpm; 10L 20–800 rpm                   | "5L Glass: 20 – 1,500 rpm" / "10L Glass: 20 – 800 rpm"                                                           | SRC-002                              | BioreactorSystem -> hasComponent -> AgitationSystem                   | explícita                 | alta                                                         | no                 |
| Ambos poseen agitación regulable                               | comparación de rangos rpm                                                                                        | SRC-001 + SRC-002                    | BioreactorSystem -> hasAgitationSystem -> AgitationSystem             | inferida                  | media                                                        | sí                 |
| BioLector mide pH 4–7.5                                        | "pH 4 – 7.5 (depending on plate)"                                                                                | SRC-001                              | BioreactorSystem -> measuresWith -> pHSensor                          | explícita                 | alta                                                         | no                 |
| Biostat mide pH 2–12                                           | "pH, reusable Combined measuring electrode                                                                       | 2–12 pH 0.01 pH" SRC-002                   | BioreactorSystem -> measuresWith -> pHSensor                 | explícita          | alta | no  |
| Ambos miden pH                                                 | comparación de sensores pH                                                                                       | SRC-001 + SRC-002                    | BioreactorSystem -> hasComponent -> pHSensor                          | inferida                  | media                                                        | sí                 |
| BioLector mide DO 0–100%                                       | "0 – 100 % dissolved oxygen\*1"                                                                                  | SRC-001                              | BioreactorSystem -> measuresWith -> DissolvedOxygenSensor             | explícita                 | alta                                                         | no                 |
| Biostat mide DO 0–100%                                         | "Dissolved oxygen, reusable Polarographic or optical                                                             | 0–100% 0.1%" SRC-002                   | BioreactorSystem -> measuresWith -> DissolvedOxygenSensor    | explícita          | alta | no  |
| Ambos miden oxígeno disuelto                                   | comparación DO                                                                                                   | SRC-001 + SRC-002                    | BioreactorSystem -> hasComponent -> DissolvedOxygenSensor             | inferida                  | alta                                                         | sí                 |
| BioLector suministra O2 1–100% y CO2 0–12%                     | "1 – 100 % O 2 (optional)" / "0 – 12 % CO 2 (optional)"                                                          | SRC-001                              | BioreactorSystem -> hasComponent -> GasSupplySystem                   | explícita                 | alta                                                         | no                 |
| Biostat usa MFC 1:200 hasta 20 lpm                             | "Intelligent mass flow controllers with a flow range of 1:200" / "Max. total flow Up to 20 lpm per gassing line" | SRC-002                              | BioreactorSystem -> hasComponent -> GasSupplySystem                   | explícita                 | alta                                                         | no                 |
| Ambos disponen de suministro de gas controlado                 | comparación gas                                                                                                  | SRC-001 + SRC-002                    | BioreactorSystem -> hasGasSupply -> GasSupplySystem                   | inferida                  | media                                                        | sí                 |
| BioLector tiene opciones de alimentación y bombas              | "FEEDING OPTIONS" / "Two feed lines" / "Up to 665 pump strokes per hour"                                         | SRC-001                              | BioreactorSystem -> hasComponent -> FeedSystem                        | explícita                 | alta                                                         | no                 |
| Biostat tiene hasta 4 bombas variables y 4 fijas               | "Choose up to four variable speed and up to four fixed speed pumps"                                              | SRC-002                              | BioreactorSystem -> hasComponent -> FeedSystem                        | explícita                 | alta                                                         | no                 |
| Ambos permiten alimentación controlada                         | comparación feeding                                                                                              | SRC-001 + SRC-002                    | BioreactorSystem -> hasFeedSystem -> FeedSystem                       | inferida                  | media                                                        | sí                 |
| BioLector usa placas de 48 pocillos 800–1900 µL / 1000–2400 µL | "48 cultivation wells" / "Filling volume: 800 – 1900 μL" / "Filling volume: 1000 – 2400 μL"                      | SRC-001                              | Microbioreactor -> hasVessel -> MicrotiterPlate                       | explícita                 | alta                                                         | no                 |
| Biostat usa Univessel Glass 1–10 L                             | "Connect Univessel® Glass" / "1 L, 2 L, 5 L and 10 L"                                                            | SRC-002                              | StirredTankBioreactor -> hasVessel -> GlassVessel                     | explícita                 | alta                                                         | no                 |
| BioLector y Biostat se usan en misma cadena 1–2 mL a 5 L       | "1 to 2 mL scale in a BioLector XT® ... up to a 5 L bioreactor" / "5 L bioreactor (Biostat B5, Sartorius AG)"    | SRC-003                              | Microbioreactor -> isScaleDownOf -> StirredTankBioreactor             | explícita                 | alta                                                         | no                 |

4. Conceptos candidatos

- BioreactorSystem
- Microbioreactor (BioLector XT)
- StirredTankBioreactor (Biostat B 5L/10L)
- TemperatureControlSystem
- AgitationSystem
- pHSensor
- DissolvedOxygenSensor
- GasSupplySystem
- FeedSystem
- CultureVessel
- MicrotiterPlate
- GlassVessel

5. Relaciones candidatas con dominio y rango sugeridos

- hasComponent: BioreactorSystem -> Component
- hasTemperatureControl: BioreactorSystem -> TemperatureControlSystem
- hasAgitationSystem: BioreactorSystem -> AgitationSystem
- measuresWith: BioreactorSystem -> Sensor
- hasGasSupply: BioreactorSystem -> GasSupplySystem
- hasFeedSystem: BioreactorSystem -> FeedSystem
- hasVessel: BioreactorSystem -> CultureVessel
- isScaleDownOf: Microbioreactor -> StirredTankBioreactor

6. Triadas RDF candidatas

- BioLectorXT -> hasComponent -> TemperatureControlSystem (soportada por SRC-001)
- BiostatB5L -> hasComponent -> TemperatureControlSystem (soportada por SRC-002)
- BioLectorXT -> hasAgitationSystem -> AgitationSystem_100-1500rpm (SRC-001)
- BiostatB5L -> hasAgitationSystem -> AgitationSystem_20-1500rpm (SRC-002)
- BioLectorXT -> measuresWith -> pHSensor_4-7.5 (SRC-001)
- BiostatB5L -> measuresWith -> pHSensor_2-12 (SRC-002)
- BioLectorXT -> measuresWith -> DissolvedOxygenSensor_0-100 (SRC-001)
- BiostatB5L -> measuresWith -> DissolvedOxygenSensor_0-100 (SRC-002)
- BioLectorXT -> hasGasSupply -> GasSupplySystem_O2-CO2 (SRC-001)
- BiostatB5L -> hasGasSupply -> GasSupplySystem_MFC-1:200 (SRC-002)
- BioLectorXT -> hasFeedSystem -> FeedSystem_665strokes/h (SRC-001)
- BiostatB5L -> hasFeedSystem -> FeedSystem_4variablePumps (SRC-002)
- BioLectorXT -> hasVessel -> MicrotiterPlate_48wells (SRC-001)
- BiostatB5L -> hasVessel -> GlassVessel_5L (SRC-002)
- BioLectorXT -> isScaleDownOf -> BiostatB5L (SRC-003)

7. Sinónimos documentados

- "BioLector XT®" / "microbioreactor" [SRC-003]
- "Biostat B5" / "5 L bioreactor (Biostat B5, Sartorius AG)" [SRC-003]
- "Univessel® Glass" [SRC-002]
- "pump strokes per hour" [SRC-001]
- "variable speed pumps" [SRC-002]

8. Vacíos del corpus

- No establecido en el corpus suministrado: controladores PID específicos en Biostat, equivalencia funcional de "TRIGGERED pH CONTROL (CLOSED LOOP CONTROLLER)" entre sistemas.
- No establecido: sensores de espuma, nivel, presión, biomasa capacitiva en BioLector.
- No establecido: software de control común, alarmas, eventos, o protocolos de esterilización comparables.
- No establecido: detalles de geometría de impulsores más allá de "two Rushton turbines" en Biostat 5L.

9. Estado final

- Soportado: parcialmente soportado
- Justificación: el corpus permite identificar siete componentes comunes (temperatura, agitación, pH, DO, gas, alimentación, recipiente) con evidencia explícita en cada sistema, pero no establece equivalencias funcionales completas ni componentes auxiliares.
