# Extracción de conocimiento ontológico — ALC-03

---

## 1. ID y pregunta

**ID:** ALC-03
**Pregunta:** ¿Cómo se diferencian conceptualmente BioLector XT, Sartorius 5 L y Sartorius 10 L como sistemas de bioproceso?

---

## 2. Respuesta basada en evidencia

Los tres sistemas se diferencian en cinco dimensiones conceptuales identificables exclusivamente desde el corpus suministrado:

**Dimensión 1 — Escala operativa (volumen de trabajo)**
El BioLector XT opera en microscala. SRC-010 documenta cultivaciones a 800 µL en FlowerPlates de 48 pocillos. SRC-008 documenta operación a 1 mL con OTRMax de 80 mmol·L⁻¹·h⁻¹. SRC-006 documenta operación a 200 µL en validación de escalado. El Sartorius 5 L opera en el rango 0.6–5 L y el Sartorius 10 L en el rango 1.5–10 L, según SRC-004.

**Dimensión 2 — Principio de agitación**
El BioLector XT opera por agitación orbital de la placa de microtitulación a velocidades de hasta 1400 rpm (SRC-010) y 1200 rpm (SRC-008). Los biorreactores Sartorius emplean agitación mecánica por impeller con eje central desde arriba y relaciones geométricas constantes entre el recipiente y el impeller (SRC-009).

**Dimensión 3 — Paralelismo de cultivos**
El BioLector XT soporta hasta 48 cultivos simultáneos en una sola placa (SRC-001, SRC-002). El Sartorius Biostat B soporta uno o dos recipientes en configuración single o twin (SRC-003).

**Dimensión 4 — Tipo de sensores y monitoreo**
El BioLector XT utiliza sensores ópticos pre-calibrados y medición no invasiva (backscatter a 620 nm para biomasa; fluorescencia para pH y DO) (SRC-001, SRC-010, SRC-011). Los sistemas Sartorius 5 L y 10 L utilizan sensores electroquímicos y fisicoquímicos in situ: pH, pO₂, temperatura, espuma, nivel, redox, turbidez y control gravimétrico (SRC-004).

**Dimensión 5 — Función en el pipeline de desarrollo de bioprocesos**
El BioLector XT está posicionado en tamizaje de alto rendimiento en fase temprana: selección de cepas, optimización de medios y condiciones (SRC-001, SRC-002, SRC-011). Los Sartorius 5 L y 10 L están posicionados como sistemas de optimización y caracterización de procesos y como modelos de escala descendente (scale-down models) respecto a procesos a gran escala (SRC-004, SRC-005).

**Diferencia entre Sartorius 5 L y Sartorius 10 L**
La diferencia entre ambos Sartorius es principalmente cuantitativa: mayor volumen máximo (5 L vs. 10 L), menor velocidad de agitación máxima (1500 rpm vs. 800 rpm) y mayor volumen mínimo de operación (0.6 L vs. 1.5 L). Ambos comparten el mismo controlador, principio de operación, familia de sensores y modos de proceso (SRC-004, SRC-003).

---

## 3. Tabla de afirmaciones y evidencia

| ID evid. | Afirmación                                                                                                                                                                                                              | Fragmento de evidencia (textual)                                                                                                                                                                                                                          | Fuente / Sección                      | Tipo      | Confianza | Validación experta                          |
| -------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------- | --------- | --------- | ------------------------------------------- |
| E-01     | El BioLector XT utiliza placas de microtitulación de 48 pocillos en formato estándar ANSI/SLAS (SBS)                                                                                                                    | "the BioLector XT microbioreactor is based on a standard ANSI/SLAS (SBS) microtiter plate (MTP) format… Disposable 48 well MTPs enable online measurement"                                                                                                | SRC-001 / Descripción de producto     | Explícita | Alta      | No                                          |
| E-02     | El BioLector XT opera con sensores ópticos pre-calibrados (no electroquímicos in situ)                                                                                                                                  | "operates with online, pre-calibrated optical sensors"                                                                                                                                                                                                    | SRC-001 / Descripción de producto     | Explícita | Alta      | No                                          |
| E-03     | El BioLector XT monitorea biomasa, fluorescencia, pH y DO en tiempo real para aerobios y anaerobios                                                                                                                     | "enables real-time evaluation of biomass, fluorescence, pH, dissolved oxygen in the liquid phase (DO), and other key cultivation parameters for aerobes and anaerobes"                                                                                    | SRC-001 / Descripción de producto     | Explícita | Alta      | No                                          |
| E-04     | El BioLector XT soporta tecnología microfluidica patentada para control simultáneo de pH y alimentación                                                                                                                 | "patented microfluidic technology supports simultaneous pH control and feeding"                                                                                                                                                                           | SRC-001 / Descripción de producto     | Explícita | Alta      | No                                          |
| E-05     | El BioLector XT es un sistema de tamizaje de cepas de alto rendimiento                                                                                                                                                  | "enables high-throughput strain screenings, cultivation parameter monitoring, and feeding strategy optimization"                                                                                                                                          | SRC-002 / Cuerpo del comunicado       | Explícita | Alta      | No                                          |
| E-06     | El BioLector XT es adecuado para cultivos microbianos, fúngicos y de algas                                                                                                                                              | "ideally suited for microbial, fungal, and algal cultivations"                                                                                                                                                                                            | SRC-002 / Cuerpo del comunicado       | Explícita | Alta      | No                                          |
| E-07     | El BioLector XT permite gasificación con O₂ de 1%–100% y CO₂ de 1%–12%                                                                                                                                                  | "Gassing with O2 within a range of 1% – 100% and with CO2 within 1% – 12%"                                                                                                                                                                                | SRC-002 / Características adicionales | Explícita | Alta      | No                                          |
| E-08     | El BioLector XT permite experimentos fed-batch bajo condiciones anaeróbicas                                                                                                                                             | "Enables fed-batch experiments under anaerobic conditions"                                                                                                                                                                                                | SRC-002 / Características adicionales | Explícita | Alta      | No                                          |
| E-09     | El Sartorius Biostat B puede configurarse en modo single o twin (1 o 2 recipientes)                                                                                                                                     | "Single or twin set-up for control of one or two culture vessel"                                                                                                                                                                                          | SRC-003 / Características principales | Explícita | Alta      | No                                          |
| E-10     | El Sartorius Biostat B admite hasta cuatro controladores de flujo másico (MFCs)                                                                                                                                         | "Gassing system comparable to our Biostat STR® with up to four mass flow controller"                                                                                                                                                                      | SRC-003 / Características principales | Explícita | Alta      | No                                          |
| E-11     | El Sartorius Biostat B soporta modos batch, fed-batch, continuo y perfusión                                                                                                                                             | "This enables you to run your Biostat® B in batch, fed-batch, continuous or perfusion mode"                                                                                                                                                               | SRC-003 / Modos de proceso            | Explícita | Alta      | No                                          |
| E-12     | El Sartorius Biostat B tiene control avanzado de DO con ajuste paralelo de velocidad de agitación y caudal de gas                                                                                                       | "The advanced DO controller supports parallel adjustment of all DO affecting parameter settings like stirrer speed and gas flow rates of air and pure oxygen, automatically and simultaneously"                                                           | SRC-003 / Control de DO               | Explícita | Alta      | No                                          |
| E-13     | El Sartorius Biostat B 5 L tiene volumen de trabajo de 0.6–5 L                                                                                                                                                          | "Working volume: 5L (0.6–5L)"                                                                                                                                                                                                                             | SRC-004 / Especificaciones técnicas   | Explícita | Alta      | No                                          |
| E-14     | El Sartorius Biostat B 10 L tiene volumen de trabajo de 1.5–10 L                                                                                                                                                        | "Working volume: 10L (1.5–10L)"                                                                                                                                                                                                                           | SRC-004 / Especificaciones técnicas   | Explícita | Alta      | No                                          |
| E-15     | El Sartorius Biostat B 5 L tiene velocidad de agitación de 20–1500 rpm                                                                                                                                                  | "Permitted stirring speed: 5L (20–1500rpm)"                                                                                                                                                                                                               | SRC-004 / Especificaciones técnicas   | Explícita | Alta      | No                                          |
| E-16     | El Sartorius Biostat B 10 L tiene velocidad de agitación de 20–800 rpm                                                                                                                                                  | "Permitted stirring speed: 10L (20–800rpm)"                                                                                                                                                                                                               | SRC-004 / Especificaciones técnicas   | Explícita | Alta      | No                                          |
| E-17     | El Sartorius Biostat B admite flujos de gas de aire, O₂, CO₂ y N₂ con caudal total máximo de 20 lpm                                                                                                                     | "Gas flow: air, O2, CO2\*, N2 (max. total flow rate 20 lpm)"                                                                                                                                                                                              | SRC-004 / Especificaciones técnicas   | Explícita | Alta      | No                                          |
| E-18     | El Sartorius Biostat B admite dos tipos de sparger: poroso y tipo L                                                                                                                                                     | "Gas spargers: Porous sparger / L-type sparger"                                                                                                                                                                                                           | SRC-004 / Especificaciones técnicas   | Explícita | Alta      | No                                          |
| E-19     | El Sartorius Biostat B tiene control de temperatura de 0–80°C                                                                                                                                                           | "Temperature control: 0–80°C"                                                                                                                                                                                                                             | SRC-004 / Especificaciones técnicas   | Explícita | Alta      | No                                          |
| E-20     | El Sartorius Biostat B lleva sensores de pH, pO₂, temperatura, espuma, nivel, adición de sustrato, mezcla de gases, agitación, control gravimétrico de alimentación y cosecha, presión del recipiente, redox y turbidez | "Sensors: pH, pO2, Temperature, Foam, Level, Substrate addition, Gas mixing, Agitation, Gravimetric Feed & Harvest Control, Constant Total Gas Flow Control, Vessel pressure, Redox & Turbidity\*"                                                        | SRC-004 / Especificaciones técnicas   | Explícita | Alta      | Sí (asterisco indica opcional)              |
| E-21     | El Sartorius Biostat B está diseñado específicamente para optimización y caracterización de procesos en biotech y biofarmacéutica                                                                                       | "specifically designed to accommodate the requirements of process optimization and characterization in the food, biotech and biopharmaceutical industry"                                                                                                  | SRC-004 / Descripción del instrumento | Explícita | Alta      | No                                          |
| E-22     | El Sartorius Biostat B es el modelo ideal de escala descendente para procesos a gran escala                                                                                                                             | "making it the ideal scale-down model for your large-scale process"                                                                                                                                                                                       | SRC-004 / Descripción del instrumento | Explícita | Alta      | No                                          |
| E-23     | Los biorreactores Sartorius de banco tienen recipientes autoclavables de 1 a 10 L y recipientes de uso único de 250 mL y 2 L                                                                                            | "Autoclavable culture vessels are available from 1 L to 10 L and single use vessels of 250 mL and 2 L"                                                                                                                                                    | SRC-005 / Descripción general         | Explícita | Alta      | No                                          |
| E-24     | El Biostat B puede controlar hasta dos unidades de cultivo de forma completamente independiente                                                                                                                         | "Our Biostat® B tower controls up to two culture units completely independently"                                                                                                                                                                          | SRC-005 / Descripción general         | Explícita | Alta      | No                                          |
| E-25     | Los biorreactores Sartorius de banco pueden funcionar como modelos de escala descendente para procesos comerciales a gran escala                                                                                        | "they allow for similar process control as their large scale counterparts and can function as scale-down models for large commercial processes"                                                                                                           | SRC-005 / Descripción general         | Explícita | Alta      | No                                          |
| E-26     | La FlowerPlate provee OTR de hasta 0.2 mol/L/h, suficiente para la mayoría de fermentaciones microbianas                                                                                                                | "provide unlimited oxygen transfer conditions (OTR up to 0.2 mol/L/h) for most microbial fermentation applications"                                                                                                                                       | SRC-006 / Descripción del sistema     | Explícita | Alta      | No                                          |
| E-27     | La escalabilidad del BioLector a un fermentador de laboratorio fue validada en paralelo a 200 µL y 1.4 L para E. coli y Hansenula polymorpha                                                                            | "parallel fermentations of E. coli and the yeast Hansenula polymorpha were conducted in both scales, with 200 µL and 1.4 L respectively"                                                                                                                  | SRC-006 / Validación de escalado      | Explícita | Alta      | No                                          |
| E-28     | El escalado de MTP (200 µL) a fermentador de tanque agitado (1.4 L) fue evaluado y validado para E. coli y Hansenula polymorpha                                                                                         | "evaluate the scale-up from a microtiter plate scale (200 μL) to a stirred tank fermenter scale (1.4 L)… fermented in parallel at both scales"                                                                                                            | SRC-007 / Abstract                    | Explícita | Alta      | No                                          |
| E-29     | La escalabilidad de MTPs a STFs las hace adecuadas como microbiorreactor y unidad de reactor de escala descendente                                                                                                      | "This proven scalability of MTPs to STFs could make them ideally suited as a microbioreactor and a scale-down reactor unit"                                                                                                                               | SRC-007 / Discusión                   | Explícita | Alta      | No                                          |
| E-30     | El criterio de escalado empleado entre BioLector (FlowerPlate a 1 mL) y biorreactor fue DO > 20%                                                                                                                        | "The scale-up criterion was a DO > 20%... In flowerplates this criterion was fulfilled at shaking frequency n = 1200 min-1 and filling volume V = 1 mL"                                                                                                   | SRC-008 / Métodos                     | Explícita | Alta      | Sí (específico del experimento documentado) |
| E-31     | La OTRMax del BioLector en FlowerPlate a 1 mL y 1200 rpm es de 80 mmol·L⁻¹·h⁻¹                                                                                                                                          | "filling volume V = 1 mL leading to an OTRMax = 80 mmol·L-1·h-1"                                                                                                                                                                                          | SRC-008 / Métodos                     | Explícita | Alta      | No                                          |
| E-32     | La tasa de crecimiento máxima µMax fue equivalente a 1 mL (BioLector) y 1 L (biorreactor): 0.41 ± 0.02 h⁻¹                                                                                                              | "The maximum specific growth rate of μMax = 0.41 ± 0.02 h-1 was the same in 1 mL MBR as well as in 1 L Bioreactor"                                                                                                                                        | SRC-008 / Resultados                  | Explícita | Alta      | No                                          |
| E-33     | Los biorreactores Sartorius tienen diseño clásico de tanque agitado con eje central desde arriba y relaciones geométricas constantes                                                                                    | "Sartorius bioreactors have a classic stirred tank design with a top stirred center shaft, a constant vessel height to vessel diameter ratio, and constant impeller diameter to vessel diameter ratios"                                                   | SRC-009 / Principios de escalado      | Explícita | Alta      | No                                          |
| E-34     | La similitud geométrica es la base del escalado en biorreactores Sartorius                                                                                                                                              | "Bioreactor geometric similarity is the foundation to simplifying bioreactor scaling"                                                                                                                                                                     | SRC-009 / Principios de escalado      | Explícita | Alta      | No                                          |
| E-35     | El BioLector se operó a 1400 rpm de velocidad de agitación y 85% de humedad relativa para cultivaciones en µ-biorreactor                                                                                                | "All cultivations were performed at a shaking speed of 1400 rpm and the relative humidity kept at 85%"                                                                                                                                                    | SRC-010 / Materiales y métodos        | Explícita | Alta      | No                                          |
| E-36     | El BioLector monitorea biomasa en línea cada 15 min por medición de backscatter a 620 nm                                                                                                                                | "The biomass was monitored online at 15 min intervals by scattered light measurement at 620 nm"                                                                                                                                                           | SRC-010 / Materiales y métodos        | Explícita | Alta      | No                                          |
| E-37     | En FlowerPlate B (precultivo) se usaron 800 µL como volumen de trabajo                                                                                                                                                  | "Pre-culture was setup in 48-well Flowerplates B (m2p-labs GmbH) with 800 µL of LB broth"                                                                                                                                                                 | SRC-010 / Materiales y métodos        | Explícita | Alta      | No                                          |
| E-38     | El BioLector utiliza los pocillos de placas de microtitulación agitadas como fermentadores a pequeña escala                                                                                                             | "the fiber-optic online-monitoring system BioLector which utilizes the wells of shaken microtiter plates (MTPs) as small-scale fermenters"                                                                                                                | SRC-011 / Abstract                    | Explícita | Alta      | No                                          |
| E-39     | El BioLector microfluidico permite fermentaciones a microscala que simulan bioprocesos a gran escala y constituyen la base del desarrollo confiable de procesos                                                         | "this microfluidic BioLector allows user-friendly, cost-effective microscale fermentations that provide high information output and mimic large-scale bioprocesses. This is the mandatory basis for reliable process development and subsequent scale-up" | SRC-011 / Conclusiones                | Explícita | Alta      | No                                          |
| E-40     | La diferencia de velocidad de agitación máxima entre Sartorius 5 L (1500 rpm) y 10 L (800 rpm) es cuantitativa, no cualitativa, dentro del mismo principio de operación por impeller                                    | No hay fragmento explícito que declare esto; se infiere de comparar E-15 y E-16 dentro del mismo sistema Biostat B (SRC-004)                                                                                                                              | SRC-004 / Especificaciones técnicas   | Inferida  | Alta      | Sí                                          |
| E-41     | El BioLector XT succede al BioLector Pro                                                                                                                                                                                | "The BioLector XT Microbioreactor succeeds the BioLector Pro Microbioreactor"                                                                                                                                                                             | SRC-002 / Cuerpo del comunicado       | Explícita | Alta      | No                                          |

---

## 4. Conceptos candidatos

| ID concepto | Nombre candidato              | Tipo sugerido                             | Definición basada en corpus                                                                                                                                                                                           | Evidencias             | Estado    |
| ----------- | ----------------------------- | ----------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------- | --------- |
| C-01        | `BioprocessSystem`            | Clase raíz                                | Sistema instrumental utilizado para llevar a cabo bioprocesos de cultivo microbiano, fúngico, vegetal o de células animales                                                                                           | E-01, E-13, E-21       | Candidato |
| C-02        | `Microbioreactor`             | Subclase de `BioprocessSystem`            | Sistema de bioproceso que opera en microscala (µL a pocos mL) utilizando los pocillos de placas de microtitulación agitadas como unidades de cultivo, con medición en línea no invasiva                               | E-01, E-38, E-39       | Candidato |
| C-03        | `StirredTankBioreactor`       | Subclase de `BioprocessSystem`            | Sistema de bioproceso con recipiente cerrado, agitación mecánica por impeller con eje central y control de múltiples variables de proceso; escalable por similitud geométrica                                         | E-33, E-34, E-28       | Candidato |
| C-04        | `BioLectorXT`                 | Individuo de `Microbioreactor`            | Instancia específica del microbiorreactor de alto rendimiento fabricado por m2p-labs / Beckman Coulter, basado en formato MTP ANSI/SLAS de 48 pocillos con sensores ópticos pre-calibrados y tecnología microfluidica | E-01, E-02, E-05, E-41 | Candidato |
| C-05        | `SartoriusBiostatB5L`         | Individuo de `StirredTankBioreactor`      | Instancia del Biostat B de Sartorius con recipiente de 5 L, volumen de trabajo 0.6–5 L y velocidad de agitación 20–1500 rpm                                                                                           | E-13, E-15, E-09       | Candidato |
| C-06        | `SartoriusBiostatB10L`        | Individuo de `StirredTankBioreactor`      | Instancia del Biostat B de Sartorius con recipiente de 10 L, volumen de trabajo 1.5–10 L y velocidad de agitación 20–800 rpm                                                                                          | E-14, E-16, E-09       | Candidato |
| C-07        | `MicrotiterPlate`             | Clase                                     | Recipiente de cultivo desechable en formato de placa de pocillos (estándar ANSI/SLAS/SBS) usado en sistemas de microbiorreactor de agitación orbital                                                                  | E-01, E-38             | Candidato |
| C-08        | `FlowerPlate`                 | Subclase de `MicrotiterPlate`             | Placa de microtitulación con geometría de pocillo en forma de flor, desarrollada por m2p-labs, que maximiza la transferencia de oxígeno (OTR hasta 0.2 mol/L/h)                                                       | E-26, E-37, E-31       | Candidato |
| C-09        | `OpticalSensor`               | Clase                                     | Sensor que emplea principios fotónicos (backscatter, fluorescencia) para medición en línea no invasiva de parámetros de cultivo                                                                                       | E-02, E-36             | Candidato |
| C-10        | `ElectrochemicalSensor`       | Clase                                     | Sensor que emplea principios electroquímicos para medición in situ de pH, pO₂ u otros parámetros en biorreactores de tanque agitado                                                                                   | E-20                   | Candidato |
| C-11        | `GassingSystem`               | Clase                                     | Subsistema que controla el suministro, mezcla y caudal de gases (aire, O₂, CO₂, N₂) al recipiente de cultivo                                                                                                          | E-10, E-17, E-07       | Candidato |
| C-12        | `ProcessMode`                 | Clase                                     | Categoría del modo operativo de un bioproceso: batch, fed-batch, continuo, perfusión                                                                                                                                  | E-11                   | Candidato |
| C-13        | `ScaleDownModel`              | Concepto auxiliar                         | Función de un sistema de bioproceso orientada a replicar a pequeña escala las condiciones operativas de biorreactores a gran escala, para desarrollo y caracterización del proceso                                    | E-22, E-25, E-29       | Candidato |
| C-14        | `HighThroughputScreening`     | Concepto auxiliar                         | Función de un sistema de bioproceso orientada al tamizaje paralelo masivo de cepas, medios y condiciones, característica de la microscala                                                                             | E-05, E-39             | Candidato |
| C-15        | `OrbitalShaking`              | Clase o individuo de `AgitationPrinciple` | Principio de agitación por movimiento orbital de la plataforma portadora de la placa de microtitulación, sin impeller mecánico                                                                                        | E-35, E-30             | Candidato |
| C-16        | `MechanicalImpellerAgitation` | Clase o individuo de `AgitationPrinciple` | Principio de agitación por turbina mecánica (impeller) con eje central accionado por motor, propio de los biorreactores de tanque agitado                                                                             | E-33                   | Candidato |
| C-17        | `OxygenTransferRate`          | Propiedad de dato                         | Tasa volumétrica de transferencia de oxígeno (OTR), expresada en mol·L⁻¹·h⁻¹ o mmol·L⁻¹·h⁻¹; parámetro de escalado clave                                                                                              | E-26, E-31             | Candidato |
| C-18        | `ScaleUpCriterion`            | Clase                                     | Parámetro o condición operativa utilizado como base para la transferencia de un proceso entre escalas (ej.: DO > 20%, kLa, OTR)                                                                                       | E-30                   | Candidato |
| C-19        | `WorkingVolume`               | Propiedad de dato                         | Volumen de cultivo efectivo durante la operación de un sistema de bioproceso; expresado en µL, mL o L                                                                                                                 | E-13, E-14, E-37       | Candidato |
| C-20        | `GeometricSimilarity`         | Concepto auxiliar                         | Principio de diseño de biorreactores de tanque agitado que mantiene constantes las relaciones entre altura, diámetro del recipiente y diámetro del impeller entre escalas                                             | E-33, E-34             | Candidato |

---

## 5. Relaciones candidatas

| ID relación | Nombre candidato           | Dominio sugerido                    | Rango sugerido                 | Significado                                                                                     | Evidencias               | Estado                          |
| ----------- | -------------------------- | ----------------------------------- | ------------------------------ | ----------------------------------------------------------------------------------------------- | ------------------------ | ------------------------------- |
| R-01        | `hasWorkingVolume`         | `BioprocessSystem`                  | `xsd:decimal` (en L o mL)      | Volumen de cultivo efectivo en operación                                                        | E-13, E-14, E-37         | Candidato                       |
| R-02        | `hasMaxWorkingVolume`      | `BioprocessSystem`                  | `xsd:decimal`                  | Límite superior del volumen de trabajo permitido                                                | E-13, E-14               | Candidato                       |
| R-03        | `hasMinWorkingVolume`      | `BioprocessSystem`                  | `xsd:decimal`                  | Límite inferior del volumen de trabajo permitido                                                | E-13, E-14               | Candidato                       |
| R-04        | `usesAgitationPrinciple`   | `BioprocessSystem`                  | `AgitationPrinciple`           | Principio de agitación empleado en el sistema                                                   | E-33, E-35               | Candidato                       |
| R-05        | `usesCultureVessel`        | `BioprocessSystem`                  | `CultureVessel`                | Recipiente de cultivo empleado (MTP, Univessel Glass, Univessel SU)                             | E-01, E-23               | Candidato                       |
| R-06        | `hasSensorType`            | `BioprocessSystem`                  | `SensorType`                   | Tipo de sensor empleado para monitoreo en línea                                                 | E-02, E-20               | Candidato                       |
| R-07        | `supportsParallelCultures` | `BioprocessSystem`                  | `xsd:integer`                  | Número máximo de cultivos simultáneos soportados                                                | E-01, E-09               | Candidato                       |
| R-08        | `functionsAs`              | `BioprocessSystem`                  | `BioprocessFunction`           | Función principal del sistema en el pipeline de desarrollo (tamizaje, scale-down, optimización) | E-05, E-22, E-25         | Candidato                       |
| R-09        | `isScalableFrom`           | `BioprocessSystem`                  | `BioprocessSystem`             | Relación de escalado desde un sistema de menor escala hacia uno de mayor escala                 | E-27, E-28, E-39         | Candidato (requiere validación) |
| R-10        | `supportsProcessMode`      | `BioprocessSystem`                  | `ProcessMode`                  | Modos operativos del bioproceso soportados por el sistema                                       | E-11                     | Candidato                       |
| R-11        | `hasMaxAgitationSpeed`     | `BioprocessSystem`                  | `xsd:decimal` (en rpm)         | Velocidad máxima de agitación del sistema                                                       | E-15, E-16, E-35         | Candidato                       |
| R-12        | `hasMinAgitationSpeed`     | `StirredTankBioreactor`             | `xsd:decimal` (en rpm)         | Velocidad mínima de agitación del sistema                                                       | E-15, E-16               | Candidato                       |
| R-13        | `hasGassingSystem`         | `BioprocessSystem`                  | `GassingSystem`                | Subsistema de suministro de gases asociado al sistema                                           | E-10, E-17, E-07         | Candidato                       |
| R-14        | `hasOTR`                   | `CultureVessel` o `Microbioreactor` | `xsd:decimal` (en mol·L⁻¹·h⁻¹) | Tasa de transferencia de oxígeno del sistema o recipiente                                       | E-26, E-31               | Candidato                       |
| R-15        | `manufacturedBy`           | `BioprocessSystem`                  | `Organization`                 | Fabricante del sistema de bioproceso                                                            | E-01, E-03, E-13         | Candidato                       |
| R-16        | `hasScaleUpCriterion`      | `BioprocessSystem`                  | `ScaleUpCriterion`             | Parámetro utilizado como criterio de escalado entre sistemas                                    | E-30                     | Candidato                       |
| R-17        | `succeedsModel`            | `BioprocessSystem`                  | `BioprocessSystem`             | Relación de sucesión de modelo entre versiones de un mismo sistema                              | E-41                     | Candidato                       |
| R-18        | `hasTemperatureRange`      | `BioprocessSystem`                  | `xsd:string`                   | Rango de temperatura de operación del sistema                                                   | E-19                     | Candidato                       |
| R-19        | `hasVesselPressureDesign`  | `StirredTankBioreactor`             | `xsd:string`                   | Diseño de presión del recipiente de cultivo                                                     | E-20 (implícito en spec) | Candidato                       |
| R-20        | `hasGeometricSimilarity`   | `StirredTankBioreactor`             | `xsd:boolean`                  | Indica si el biorreactor mantiene relaciones geométricas constantes entre escalas               | E-33, E-34               | Candidato                       |

---

## 6. Triadas RDF candidatas

```
# T-01 — BioLector XT es de tipo Microbioreactor
BioLectorXT  rdf:type  Microbioreactor
Fuente: SRC-001, SRC-011 | Tipo: Explícita | Estado: Soportada

# T-02 — SartoriusBiostatB5L es de tipo StirredTankBioreactor
SartoriusBiostatB5L  rdf:type  StirredTankBioreactor
Fuente: SRC-004, SRC-009 | Tipo: Explícita | Estado: Soportada

# T-03 — SartoriusBiostatB10L es de tipo StirredTankBioreactor
SartoriusBiostatB10L  rdf:type  StirredTankBioreactor
Fuente: SRC-004, SRC-009 | Tipo: Explícita | Estado: Soportada

# T-04 — Microbioreactor es subclase de BioprocessSystem
Microbioreactor  rdfs:subClassOf  BioprocessSystem
Fuente: SRC-001, SRC-011 | Tipo: Inferida | Estado: Parcialmente soportada

# T-05 — StirredTankBioreactor es subclase de BioprocessSystem
StirredTankBioreactor  rdfs:subClassOf  BioprocessSystem
Fuente: SRC-003, SRC-009 | Tipo: Inferida | Estado: Parcialmente soportada

# T-06 — BioLector XT usa formato de placa ANSI/SLAS de 48 pocillos
BioLectorXT  usesCultureVessel  MicrotiterPlate_48well_ANSI_SLAS
Fuente: SRC-001 | Tipo: Explícita | Estado: Soportada

# T-07 — BioLector XT opera con sensores ópticos pre-calibrados
BioLectorXT  hasSensorType  OpticalSensor
Fuente: SRC-001 | Tipo: Explícita | Estado: Soportada

# T-08 — BioLector XT soporta 48 cultivos paralelos
BioLectorXT  supportsParallelCultures  "48"
Fuente: SRC-001 | Tipo: Explícita | Estado: Soportada

# T-09 — BioLector XT usa agitación orbital
BioLectorXT  usesAgitationPrinciple  OrbitalShaking
Fuente: SRC-010, SRC-008 | Tipo: Explícita | Estado: Soportada

# T-10 — BioLector XT funciona como sistema de tamizaje de alto rendimiento
BioLectorXT  functionsAs  HighThroughputScreening
Fuente: SRC-002, SRC-011 | Tipo: Explícita | Estado: Soportada

# T-11 — BioLector XT permite gasificación con O₂ en rango 1%–100%
BioLectorXT  hasO2GassingRange  "1-100%"
Fuente: SRC-002 | Tipo: Explícita | Estado: Soportada

# T-12 — BioLector XT permite gasificación con CO₂ en rango 1%–12%
BioLectorXT  hasCO2GassingRange  "1-12%"
Fuente: SRC-002 | Tipo: Explícita | Estado: Soportada

# T-13 — BioLector XT soporta modo fed-batch bajo condiciones anaeróbicas
BioLectorXT  supportsProcessMode  AnaerobicFedBatch
Fuente: SRC-002 | Tipo: Explícita | Estado: Soportada

# T-14 — BioLector XT usa FlowerPlate como recipiente de cultivo
BioLectorXT  usesCultureVessel  FlowerPlate
Fuente: SRC-002, SRC-010, SRC-008 | Tipo: Explícita | Estado: Soportada

# T-15 — FlowerPlate es subclase de MicrotiterPlate
FlowerPlate  rdfs:subClassOf  MicrotiterPlate
Fuente: SRC-006, SRC-010 | Tipo: Inferida | Estado: Parcialmente soportada

# T-16 — FlowerPlate tiene OTR máxima de 0.2 mol/L/h
FlowerPlate  hasOTR  "0.2"
Fuente: SRC-006 | Tipo: Explícita | Estado: Soportada

# T-17 — Volumen de trabajo del BioLector en FlowerPlate B es 800 µL
BioLectorXT  hasWorkingVolume  "0.0008"
Fuente: SRC-010 | Tipo: Explícita | Nota: valor específico para FlowerPlate B en precultivo | Estado: Soportada (condicionada al tipo de placa)

# T-18 — Volumen de trabajo del BioLector en FlowerPlate es 1 mL
BioLectorXT  hasWorkingVolume  "0.001"
Fuente: SRC-008 | Tipo: Explícita | Nota: condición de cultivo principal | Estado: Soportada (condicionada a condiciones del experimento)

# T-19 — BioLector XT fue operado a 1400 rpm de agitación
BioLectorXT  hasAgitationSpeed  "1400"
Fuente: SRC-010 | Tipo: Explícita | Nota: condición operativa documentada, no necesariamente la máxima | Estado: Soportada

# T-20 — BioLector XT fue operado a 1200 rpm en FlowerPlate a 1 mL
BioLectorXT  hasAgitationSpeed  "1200"
Fuente: SRC-008 | Tipo: Explícita | Estado: Soportada (condición específica del experimento)

# T-21 — BioLector XT tiene OTRMax de 80 mmol/L/h a 1 mL y 1200 rpm
BioLectorXT  hasOTRMax  "80"
Fuente: SRC-008 | Tipo: Explícita | Estado: Soportada (condición específica documentada)

# T-22 — BioLector XT monitorea biomasa por backscatter a 620 nm cada 15 min
BioLectorXT  usesMeasurementMethod  BackscatterAt620nm
BioLectorXT  hasMeasurementInterval  "15"
Fuente: SRC-010 | Tipo: Explícita | Estado: Soportada

# T-23 — SartoriusBiostatB5L tiene volumen de trabajo máximo de 5 L
SartoriusBiostatB5L  hasMaxWorkingVolume  "5"
Fuente: SRC-004 | Tipo: Explícita | Estado: Soportada

# T-24 — SartoriusBiostatB5L tiene volumen de trabajo mínimo de 0.6 L
SartoriusBiostatB5L  hasMinWorkingVolume  "0.6"
Fuente: SRC-004 | Tipo: Explícita | Estado: Soportada

# T-25 — SartoriusBiostatB10L tiene volumen de trabajo máximo de 10 L
SartoriusBiostatB10L  hasMaxWorkingVolume  "10"
Fuente: SRC-004 | Tipo: Explícita | Estado: Soportada

# T-26 — SartoriusBiostatB10L tiene volumen de trabajo mínimo de 1.5 L
SartoriusBiostatB10L  hasMinWorkingVolume  "1.5"
Fuente: SRC-004 | Tipo: Explícita | Estado: Soportada

# T-27 — SartoriusBiostatB5L tiene velocidad de agitación máxima de 1500 rpm
SartoriusBiostatB5L  hasMaxAgitationSpeed  "1500"
Fuente: SRC-004 | Tipo: Explícita | Estado: Soportada

# T-28 — SartoriusBiostatB10L tiene velocidad de agitación máxima de 800 rpm
SartoriusBiostatB10L  hasMaxAgitationSpeed  "800"
Fuente: SRC-004 | Tipo: Explícita | Estado: Soportada

# T-29 — SartoriusBiostatB5L tiene velocidad de agitación mínima de 20 rpm
SartoriusBiostatB5L  hasMinAgitationSpeed  "20"
Fuente: SRC-004 | Tipo: Explícita | Estado: Soportada

# T-30 — SartoriusBiostatB10L tiene velocidad de agitación mínima de 20 rpm
SartoriusBiostatB10L  hasMinAgitationSpeed  "20"
Fuente: SRC-004 | Tipo: Explícita | Estado: Soportada

# T-31 — SartoriusBiostatB10L usa agitación por impeller mecánico
SartoriusBiostatB10L  usesAgitationPrinciple  MechanicalImpellerAgitation
SartoriusBiostatB5L   usesAgitationPrinciple  MechanicalImpellerAgitation
Fuente: SRC-009 | Tipo: Explícita | Estado: Soportada

# T-32 — Sartorius Biostat B tiene diseño clásico de tanque agitado con similitud geométrica
SartoriusBiostatB5L   hasGeometricSimilarity  "true"
SartoriusBiostatB10L  hasGeometricSimilarity  "true"
Fuente: SRC-009 | Tipo: Explícita | Estado: Soportada

# T-33 — Sartorius Biostat B soporta modos batch, fed-batch, continuo y perfusión
SartoriusBiostatB5L   supportsProcessMode  BatchMode
SartoriusBiostatB5L   supportsProcessMode  FedBatchMode
SartoriusBiostatB5L   supportsProcessMode  ContinuousMode
SartoriusBiostatB5L   supportsProcessMode  PerfusionMode
Fuente: SRC-003 | Tipo: Explícita | Estado: Soportada
(se extiende por inferencia a SartoriusBiostatB10L dado que comparten controlador)

# T-34 — Sartorius Biostat B tiene sensores electroquímicos in situ (pH, pO₂)
SartoriusBiostatB10L  hasSensorType  ElectrochemicalSensor
Fuente: SRC-004 | Tipo: Explícita | Estado: Soportada

# T-35 — Sartorius Biostat B lleva sensores adicionales de espuma, nivel, redox, turbidez
SartoriusBiostatB10L  hasSensorType  FoamSensor
SartoriusBiostatB10L  hasSensorType  LevelSensor
SartoriusBiostatB10L  hasSensorType  RedoxSensor
SartoriusBiostatB10L  hasSensorType  TurbiditySensor
Fuente: SRC-004 | Tipo: Explícita | Nota: asterisco indica posibles sensores opcionales | Estado: Soportada (requiere validación de opcionalidad)

# T-36 — Sartorius Biostat B admite caudal total de gas de hasta 20 lpm (aire, O₂, CO₂, N₂)
SartoriusBiostatB5L   hasMaxTotalGasFlowRate  "20"
SartoriusBiostatB10L  hasMaxTotalGasFlowRate  "20"
Fuente: SRC-004 | Tipo: Explícita | Estado: Soportada

# T-37 — Sartorius Biostat B funciona como modelo de escala descendente
SartoriusBiostatB5L   functionsAs  ScaleDownModel
SartoriusBiostatB10L  functionsAs  ScaleDownModel
Fuente: SRC-004, SRC-005 | Tipo: Explícita | Estado: Soportada

# T-38 — BioLectorXT es escalable hacia StirredTankBioreactor (relación de escalado)
BioLectorXT  isScalableFrom  StirredTankBioreactor
Fuente: SRC-006, SRC-007, SRC-011 | Tipo: Inferida | Estado: Parcialmente soportada (requiere validación experta)

# T-39 — BioLector XT sucede al BioLector Pro
BioLectorXT  succeedsModel  BioLectorPro
Fuente: SRC-002 | Tipo: Explícita | Estado: Soportada

# T-40 — BioLector XT es fabricado por Beckman Coulter / m2p-labs
BioLectorXT  manufacturedBy  BeckmanCoulterLifeSciences
Fuente: SRC-001, SRC-002 | Tipo: Explícita | Estado: Soportada

# T-41 — Sartorius Biostat B es fabricado por Sartorius
SartoriusBiostatB5L   manufacturedBy  Sartorius
SartoriusBiostatB10L  manufacturedBy  Sartorius
Fuente: SRC-003, SRC-004 | Tipo: Explícita | Estado: Soportada

# T-42 — El criterio de escalado DO > 20% fue usado entre BioLector (FlowerPlate 1 mL) y biorreactor
BioLectorXT  hasScaleUpCriterion  DissolvedOxygenAbove20Percent
Fuente: SRC-008 | Tipo: Explícita | Nota: específico del experimento documentado | Estado: Soportada (condicionada al protocolo del estudio)

# T-43 — SartoriusBiostatB5L es escalable desde SartoriusBiostatB10L
SartoriusBiostatB5L  isScalableFrom  SartoriusBiostatB10L
Fuente: SRC-009 | Tipo: Inferida | Estado: Parcialmente soportada (inferida de similitud geométrica; requiere validación experta)
```

---

## 7. Sinónimos documentados en el corpus

| Término principal             | Sinónimos o variantes documentadas en el corpus                                             | Fuente                             |
| ----------------------------- | ------------------------------------------------------------------------------------------- | ---------------------------------- |
| `BioLector XT`                | BioLector XT Microbioreactor, BioLector (genérico), µ-bioreactor, microbioreactor           | SRC-001, SRC-002, SRC-010, SRC-011 |
| `BioLector Pro`               | BioLector Pro Microbioreactor (predecesor del XT)                                           | SRC-002                            |
| `Microbioreactor`             | MBR, µ-bioreactor, small-scale fermenter, microscale fermenter                              | SRC-008, SRC-010, SRC-011          |
| `MicrotiterPlate`             | MTP, microtiter plate, microwell plate, SBS plate, ANSI/SLAS plate, shaken microtiter plate | SRC-001, SRC-007, SRC-008, SRC-011 |
| `FlowerPlate`                 | Flower plate, FlowerPlate B, FlowerPlate BOH, flower-shaped well geometry                   | SRC-006, SRC-010, SRC-008          |
| `StirredTankBioreactor`       | STR, STF (stirred tank fermenter), stirred tank reactor, benchtop bioreactor, fermenter     | SRC-007, SRC-009, SRC-005          |
| `Sartorius Biostat B`         | BIOSTAT B, Biostat B, Sartorius 5 L, Sartorius 10 L, Sartorius 10 (w/MFCS)                  | SRC-003, SRC-004, SRC-005          |
| `DissolvedOxygen`             | DO, pO₂, dissolved oxygen in liquid phase                                                   | SRC-001, SRC-004, SRC-008          |
| `OxygenTransferRate`          | OTR, OTRMax, oxygen transfer rate                                                           | SRC-006, SRC-008                   |
| `HighThroughputScreening`     | HTS, high-throughput strain screenings, tamizaje de alto rendimiento                        | SRC-002, SRC-011                   |
| `ScaleDownModel`              | Scale-down model, scale-down reactor unit                                                   | SRC-004, SRC-005, SRC-007          |
| `FedBatch`                    | Fed-batch, fed-batch cultivation, feeding strategy                                          | SRC-002, SRC-003, SRC-010          |
| `OrbitalShaking`              | Shaking, shaking speed, shaking frequency                                                   | SRC-008, SRC-010                   |
| `MechanicalImpellerAgitation` | Stirrer, stirrer speed, agitation, impeller, top stirred center shaft                       | SRC-003, SRC-004, SRC-009          |

---

## 8. Vacíos del corpus

| ID vacío | Descripción                                                                                                                                                                                                                                                                                                                                                           | Impacto ontológico                                                                                                                 | Acción recomendada                                                                                       |
| -------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------- |
| V-01     | El corpus no contiene el Technical Data Sheet (TDS) oficial del BioLector XT; no se documenta el rango exacto de volumen de trabajo por pocillo para cada modelo de FlowerPlate (B, BOH, u otros). Los valores 800 µL (SRC-010) y 1 mL (SRC-008) provienen de artículos científicos con condiciones experimentales específicas, no de la ficha técnica del fabricante | Impide establecer `hasWorkingVolume` como rango definido y el individuo correcto de `FlowerPlate` con su volumen nominal           | Suministrar el TDS oficial del BioLector XT (disponible en `beckman.com` con registro)                   |
| V-02     | No se confirma en el corpus si los Sartorius 5 L y 10 L del proyecto son el modelo Biostat B estándar o el Biostat B-DCU. Los fragmentos de SRC-004 y SRC-003 describen ambas versiones sin distinguirlas siempre con claridad                                                                                                                                        | Impacta la lista de sensores disponibles (el B-DCU tiene mayor nivel de automatización) y la identificación correcta del individuo | Validación experta con el responsable de los equipos del laboratorio                                     |
| V-03     | El corpus no documenta si los sensores marcados con asterisco en SRC-004 (Redox & Turbidity\*) son estándar u opcionales en las configuraciones específicas del proyecto                                                                                                                                                                                              | Impide establecer con certeza las triadas T-35 (sensores adicionales)                                                              | Confirmar con documentación técnica del equipo específico o con el fabricante                            |
| V-04     | No se establece en el corpus un protocolo de escalado específico entre BioLector XT y los Sartorius 5 L o 10 L del proyecto. Los criterios documentados (DO > 20% en SRC-008; kLa en SRC-007) provienen de experimentos externos al proyecto                                                                                                                          | Las triadas T-38, T-42 y T-43 quedan como parcialmente soportadas                                                                  | Suministrar SOP interno de escalado del laboratorio o protocolo experimental propio                      |
| V-05     | El corpus no incluye los part numbers (números de referencia del fabricante) de los Sartorius 5 L y 10 L del proyecto                                                                                                                                                                                                                                                 | Impide crear individuos ontológicos con identificadores unívocos verificables                                                      | Solicitar al laboratorio los números de modelo y serie de los equipos                                    |
| V-06     | No se documenta en el corpus la velocidad de agitación máxima del BioLector XT como especificación del fabricante (los valores 1200 rpm y 1400 rpm provienen de condiciones experimentales en artículos; podrían no ser el límite máximo del sistema)                                                                                                                 | Impide establecer `hasMaxAgitationSpeed` para el BioLector XT con confianza alta                                                   | Suministrar TDS oficial del BioLector XT                                                                 |
| V-07     | No se documenta en el corpus el rango de temperatura de operación del BioLector XT                                                                                                                                                                                                                                                                                    | Impide crear `hasTemperatureRange` para el BioLector XT                                                                            | Suministrar TDS oficial del BioLector XT                                                                 |
| V-08     | El corpus no describe los tipos de impeller usados en los Sartorius 5 L y 10 L (tipo Rushton, segmento, etc.)                                                                                                                                                                                                                                                         | Impide caracterizar ontológicamente el subsistema de agitación con mayor detalle                                                   | Suministrar manual del operador del Biostat B                                                            |
| V-09     | Las triadas T-04 y T-05 (`Microbioreactor rdfs:subClassOf BioprocessSystem` y `StirredTankBioreactor rdfs:subClassOf BioprocessSystem`) son inferidas de la estructura conceptual del dominio, no de declaraciones explícitas en el corpus                                                                                                                            | Jerarquía de clases raíz no está explícitamente documentada en las fuentes suministradas                                           | Validar con ontologías de referencia del dominio (OBI, SBO, OSMO) o con experto en ingeniería ontológica |

---

## 9. Estado final

| Dimensión evaluada                                                                         | Estado                                                                                                                                                                                                                              |
| ------------------------------------------------------------------------------------------ | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Diferenciación conceptual cualitativa** entre BioLector XT y Sartorius 5 L / 10 L        | **Soportada** — evidencia explícita en SRC-001, SRC-002, SRC-004, SRC-009, SRC-011                                                                                                                                                  |
| **Diferenciación cuantitativa** entre Sartorius 5 L y 10 L (volumen, RPM)                  | **Soportada** — evidencia explícita en SRC-004                                                                                                                                                                                      |
| **Especificaciones técnicas numéricas** del Sartorius 5 L y 10 L                           | **Soportada** — evidencia explícita en SRC-004                                                                                                                                                                                      |
| **Especificaciones técnicas numéricas** del BioLector XT (volumen por pocillo, RPM máxima) | **Parcialmente soportada** — valores disponibles en artículos (SRC-008, SRC-010) pero no en TDS oficial del fabricante                                                                                                              |
| **Relaciones de escalado** entre los tres sistemas                                         | **Parcialmente soportada** — principio general validado en corpus; criterios específicos del proyecto no documentados                                                                                                               |
| **Identificación de individuos ontológicos** con precisión de modelo y versión             | **Parcialmente soportada** — requiere confirmación de versión exacta (Biostat B vs. B-DCU)                                                                                                                                          |
| **Respuesta global a la pregunta ALC-03**                                                  | **Parcialmente soportada** — las dimensiones conceptuales principales están completamente respaldadas; los detalles de especificación del BioLector XT y la confirmación de versión del Sartorius requieren documentación adicional |
