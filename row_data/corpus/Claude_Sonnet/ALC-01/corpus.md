# Extracción condicionada por corpus — ALC-01

---

## 1. ID y pregunta

**ID:** ALC-01
**Pregunta:** ¿Qué se entiende por biorreactor dentro del proyecto, considerando BioLector XT, Sartorius 5 L y Sartorius 10 L?
**Corpus activo:** SRC-001 a SRC-008
**Restricción:** Solo se usan fragmentos explícitamente incluidos en el paquete. Todo vacío se declara como _no establecido en el corpus suministrado_.

---

## 2. Respuesta basada en evidencia

### 2.1 Definición general de biorreactor (extraída del corpus)

La definición más directa proviene de SRC-008:

> _"In pharmaceutical bioprocesses, bioreactors are technical devices for the controlled aseptic culture of cells and manufacturing of the product."_

Complementada por SRC-008:

> _"Bioreactors are a central element as they assign the culture parameters and allow for a tight process control and therefore highly reproducible processes and products."_

Y reforzada por SRC-005, que describe la estructura física del tipo más representado en el proyecto:

> _"A stirred tank bioreactor consists of a vessel with a defined height dimension ratio. Mixing is achieved through a central stirrer element inside the culture vessel."_

**Síntesis con base exclusiva en el corpus:** dentro del proyecto, el término _biorreactor_ refiere a un sistema técnico diseñado para el cultivo controlado y aséptico de organismos biológicos, que provee monitoreo y control de parámetros críticos del proceso, y que opera en al menos uno de los modos: batch, fed-batch, continuo o perfusión.

---

### 2.2 BioLector XT como biorreactor (evidencia explícita)

SRC-001 y SRC-002 lo caracterizan como _microbiorreactor de alto rendimiento_ basado en placa de microtitulación:

- Formato: ANSI/SLAS (SBS) MTP de 48 pocillos desechables (SRC-001, SRC-002).
- Tecnología de mezcla: FlowerPlate con agitación orbital implícita en el formato de placa (SRC-002). **Nota:** el principio de mezcla orbital no se enuncia explícitamente como tal en ninguno de los fragmentos; se infiere del formato MTP.
- Sensores: ópticos en línea precalibrados; biomasa, fluorescencia, pH, OD (SRC-001).
- Control de proceso: pH y alimentación vía módulo microfluídico patentado; microválvulas a escala de nanolitro (SRC-001).
- Modos de operación soportados explícitamente: batch, fed-batch, bolus, continuo (SRC-001).
- Gaseado: O₂ 1–100 %, CO₂ 1–12 % (SRC-001).
- Aplicaciones: microbiana, fúngica, algal; aerobios, anaerobios (SRC-002).
- Volumen de trabajo por pocillo: **no establecido en el corpus suministrado** (el TDS no fue descargable; ninguno de los ocho fragmentos reporta este valor numérico).

SRC-007 lo denomina _µ-biorreactor_ y señala una diferencia operativa respecto del STR:

> _"This solution results in higher osmotic pressure and differences in media composition compared to stirred tank bioreactor systems."_

---

### 2.3 Sartorius Biostat® B 5 L y 10 L como biorreactores (evidencia explícita)

SRC-004 aporta las especificaciones técnicas más completas y verificables:

- Volumen de trabajo 5 L: **0,6–5 L** (SRC-004).
- Volumen de trabajo 10 L: **1,5–10 L** (SRC-004).
- Velocidad de agitación 5 L: **20–1 500 rpm** (SRC-004).
- Velocidad de agitación 10 L: **20–800 rpm** (SRC-004).
- Gases: aire, O₂, CO₂, N₂; caudal total máximo **20 lpm** (SRC-004).
- Spargers: poroso y tipo L (SRC-004).
- Diseño de recipiente: –1 a +2,5 barg @ 150 °C (SRC-004).
- Control de temperatura: 0–80 °C (SRC-004).
- Sensores confirmados: pH, pO₂, temperatura, espuma, nivel, adición de sustrato, mezcla de gases, agitación, control gravimétrico de alimentación y cosecha, control de flujo gaseoso total constante, presión del recipiente, redox, turbidez (SRC-004).

SRC-003 confirma los recipientes disponibles: Univessel® Glass 1, 2, 5 y 10 L; Univessel® SU 2 y 10 L (SRC-003).

SRC-005 define el principio físico del STR de sobremesa:

> _"Mixing is achieved through a central stirrer element inside the culture vessel. The stirrer is driven by a motor packed on the head plate."_

---

### 2.4 Posición ontológica común de los tres sistemas

SRC-006 (MCBO) ofrece el patrón BFO más relevante para el proyecto:

> _"Culture conditions are not modeled as qualities of the process itself; instead, they inhere in a CellCultureSystem (e.g., the bioreactor, medium, and cells) that participates in the process."_

Esto establece que el biorreactor, en una ontología conforme a BFO, no es una clase de proceso sino una entidad material continua (_continuant_) que **participa en** un proceso de cultivo. Los tres sistemas del proyecto son instanciables como individuos de una clase `Bioreactor` bajo este patrón.

---

## 3. Tabla de afirmaciones y evidencia

| ID afirmación | Afirmación                                                                                                                                                                                                                                                           | Fuente                                       | Sección/ubicación                               | Fragmento de soporte (resumen fiel)                                                                                                                                                                    | Tipo de evidencia                            | Confianza | Validación experta                              |
| ------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------- | ----------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | -------------------------------------------- | --------- | ----------------------------------------------- |
| AFI-01        | En bioprocesos farmacéuticos, los biorreactores son dispositivos técnicos para el cultivo aséptico controlado de células y la manufactura del producto                                                                                                               | SRC-008                                      | Introducción / capítulo farmacéutico            | _"bioreactors are technical devices for the controlled aseptic culture of cells and manufacturing of the product"_                                                                                     | Explícita                                    | Alta      | No                                              |
| AFI-02        | Los biorreactores son el elemento central que asigna los parámetros de cultivo y permite control riguroso del proceso                                                                                                                                                | SRC-008                                      | Sección introductoria                           | _"Bioreactors are a central element as they assign the culture parameters and allow for a tight process control"_                                                                                      | Explícita                                    | Alta      | No                                              |
| AFI-03        | El BioLector XT es un microbiorreactor de alto rendimiento                                                                                                                                                                                                           | SRC-001, SRC-002                             | Descripción principal                           | _"The high-throughput microbioreactor enables real-time evaluation…"_                                                                                                                                  | Explícita                                    | Alta      | No                                              |
| AFI-04        | El BioLector XT se basa en el formato estándar ANSI/SLAS (SBS) de placa de microtitulación de 48 pocillos desechables                                                                                                                                                | SRC-001                                      | Descripción principal                           | _"based on a standard ANSI/SLAS (SBS) microtiter plate (MTP) format… Disposable 48 well MTPs"_                                                                                                         | Explícita                                    | Alta      | No                                              |
| AFI-05        | El BioLector XT opera con sensores ópticos en línea precalibrados                                                                                                                                                                                                    | SRC-001                                      | Descripción principal                           | _"operates with online, pre-calibrated optical sensors"_                                                                                                                                               | Explícita                                    | Alta      | No                                              |
| AFI-06        | El BioLector XT mide en línea biomasa, fluorescencia, pH y oxígeno disuelto                                                                                                                                                                                          | SRC-001, SRC-002                             | Descripción / comunicado                        | _"real-time evaluation of biomass, fluorescence, pH, dissolved oxygen in the liquid phase (DO)"_                                                                                                       | Explícita                                    | Alta      | No                                              |
| AFI-07        | El BioLector XT soporta cultivos de microorganismos aerobios, anaerobios y fototróficos                                                                                                                                                                              | SRC-001, SRC-002                             | Descripción / comunicado                        | _"aerobes and anaerobes"_; _"microbial, fungal, and algal cultivations"_                                                                                                                               | Explícita                                    | Alta      | No                                              |
| AFI-08        | El BioLector XT utiliza tecnología microfluídica patentada para control de pH y alimentación                                                                                                                                                                         | SRC-001, SRC-002                             | Features / comunicado                           | _"patented microfluidic technology supports simultaneous pH control and feeding"_                                                                                                                      | Explícita                                    | Alta      | No                                              |
| AFI-09        | El BioLector XT permite estrategias de alimentación batch, fed-batch, bolus y continuo                                                                                                                                                                               | SRC-001                                      | Sección Features                                | _"Customizable feeding strategies (batch, fed-batch, bolus, continuous)"_                                                                                                                              | Explícita                                    | Alta      | No                                              |
| AFI-10        | El BioLector XT puede gasear con O₂ entre 1 % y 100 % y CO₂ entre 1 % y 12 %                                                                                                                                                                                         | SRC-001                                      | Sección Features                                | _"Gassing with O2 within a range of 1%–100% and with CO2 within 1%–12%"_                                                                                                                               | Explícita                                    | Alta      | No                                              |
| AFI-11        | El módulo microfluídico del BioLector XT usa microválvulas que dosifican líquidos a escala de nanolitro                                                                                                                                                              | SRC-001                                      | Sección Features / módulo MF                    | _"Microvalves allot liquids at the nanolitre scale"_                                                                                                                                                   | Explícita                                    | Alta      | No                                              |
| AFI-12        | El módulo microfluídico del BioLector XT habilita 2 pocillos reservorio por cada 4 pocillos de cultivo                                                                                                                                                               | SRC-001                                      | Sección Features / módulo MF                    | _"Enables the use of 2 reservoir wells per 4 cultivation wells"_                                                                                                                                       | Explícita                                    | Alta      | No                                              |
| AFI-13        | El BioLector XT permite 48 o 32 cultivaciones paralelas en tiempo real                                                                                                                                                                                               | SRC-001                                      | Sección Features                                | _"Real-time kinetics out of 48/32 parallel cultivations"_                                                                                                                                              | Explícita                                    | Alta      | No                                              |
| AFI-14        | El BioLector XT fue desarrollado por m2p-labs (Baesweiler, Alemania), integrado a Beckman Coulter Life Sciences en noviembre de 2020                                                                                                                                 | SRC-002                                      | Párrafo de lanzamiento                          | _"from m2p-labs, part of the Beckman Coulter Life Sciences' Biotechnology Business Unit since November 2020"_                                                                                          | Explícita                                    | Alta      | No                                              |
| AFI-15        | El BioLector XT sucede al BioLector Pro                                                                                                                                                                                                                              | SRC-002                                      | Comunicado                                      | _"The BioLector XT Microbioreactor succeeds the BioLector Pro Microbioreactor."_                                                                                                                       | Explícita                                    | Alta      | No                                              |
| AFI-16        | El BioLector XT utiliza tecnología patentada FlowerPlate de microtitulación                                                                                                                                                                                          | SRC-002                                      | Comunicado                                      | _"Equipped with patented FlowerPlate microtiter plate technology"_                                                                                                                                     | Explícita                                    | Alta      | No                                              |
| AFI-17        | El BioLector, operado en modo fed-batch enzimático, presenta mayor presión osmótica y diferencias en composición del medio respecto al STR                                                                                                                           | SRC-007                                      | Sección de resultados / comparación de sistemas | _"higher osmotic pressure and differences in media composition compared to stirred tank bioreactor systems"_                                                                                           | Explícita                                    | Alta      | No                                              |
| AFI-18        | El BioLector fue usado como plataforma HTP para cribado de clones de E. coli productores de proteínas recombinantes                                                                                                                                                  | SRC-007                                      | Abstract / materiales                           | _"selected the BioLector micro-bioreactor (µ-bioreactor) system as an HTP cultivation platform to screen E. coli expression clones"_                                                                   | Explícita                                    | Alta      | No                                              |
| AFI-19        | El Biostat® B de Sartorius es un controlador universal de sobremesa para sistemas de agitación y de movimiento de balanceo                                                                                                                                           | SRC-003                                      | Descripción general                             | _"universal benchtop controller for stirred and rocking motion systems"_                                                                                                                               | Explícita                                    | Alta      | No                                              |
| AFI-20        | El Biostat® B soporta recipientes de vidrio Univessel® Glass de 1, 2, 5 y 10 L y recipientes de un solo uso Univessel® SU de 2 y 10 L                                                                                                                                | SRC-003                                      | Sección de recipientes disponibles              | _"glass (Univessel® Glass – 1, 2, 5 and 10 L) and single-use vessels (Univessel® SU 2 and 10 L)"_                                                                                                      | Explícita                                    | Alta      | No                                              |
| AFI-21        | El Biostat® B soporta modos de operación batch, fed-batch, continuo y perfusión                                                                                                                                                                                      | SRC-003                                      | Sección de estrategias de proceso               | _"run your Biostat® B in batch, fed-batch, continuous or perfusion mode"_                                                                                                                              | Explícita                                    | Alta      | No                                              |
| AFI-22        | El Biostat® B incorpora control avanzado de DO con ajuste paralelo de velocidad de agitación y tasas de flujo gaseoso                                                                                                                                                | SRC-003                                      | Sección de control de DO                        | _"advanced DO controller supports parallel adjustment of all DO affecting parameter settings like stirrer speed and gas flow rates of air and pure oxygen"_                                            | Explícita                                    | Alta      | No                                              |
| AFI-23        | La torre DCU del Biostat® B controla hasta dos unidades de cultivo de forma independiente; incluye sistema de gasificación con hasta 4 controladores de flujo másico                                                                                                 | SRC-003                                      | Sección DCU                                     | _"all controlled with one DCU tower… Gassing system comparable to our Biostat STR® with up to four mass flow controller"_                                                                              | Explícita                                    | Alta      | No                                              |
| AFI-24        | El Biostat® B puede usarse para cultivo de células animales, vegetales e insectos y para fermentación microbiana                                                                                                                                                     | SRC-003                                      | Sección de aplicaciones/GMP                     | _"animal, plant and insect cell cultivation as well as for microbial fermentation"_                                                                                                                    | Explícita                                    | Alta      | No                                              |
| AFI-25        | El Biostat® B 5 L tiene un volumen de trabajo de 0,6–5 L                                                                                                                                                                                                             | SRC-004                                      | Tabla de especificaciones técnicas              | _"5L (0.6-5L)"_                                                                                                                                                                                        | Explícita                                    | Alta      | Recomendada (confirmar con manual del equipo)   |
| AFI-26        | El Biostat® B 10 L tiene un volumen de trabajo de 1,5–10 L                                                                                                                                                                                                           | SRC-004                                      | Tabla de especificaciones técnicas              | _"10L (1.5-10L)"_                                                                                                                                                                                      | Explícita                                    | Alta      | Recomendada (confirmar con manual del equipo)   |
| AFI-27        | El Biostat® B 5 L opera entre 20 y 1 500 rpm de agitación                                                                                                                                                                                                            | SRC-004                                      | Tabla de especificaciones técnicas              | _"5L (20-1500rpm)"_                                                                                                                                                                                    | Explícita                                    | Alta      | Recomendada                                     |
| AFI-28        | El Biostat® B 10 L opera entre 20 y 800 rpm de agitación                                                                                                                                                                                                             | SRC-004                                      | Tabla de especificaciones técnicas              | _"10L (20-800rpm)"_                                                                                                                                                                                    | Explícita                                    | Alta      | Recomendada                                     |
| AFI-29        | El Biostat® B admite gases: aire, O₂, CO₂ y N₂, con caudal total máximo de 20 lpm                                                                                                                                                                                    | SRC-004                                      | Tabla de especificaciones técnicas              | _"Gas flow: air, O2, CO2_, N2 (max. total flow rate 20 lpm)"\*                                                                                                                                         | Explícita                                    | Alta      | No                                              |
| AFI-30        | El Biostat® B dispone de dos tipos de sparger: poroso y tipo L                                                                                                                                                                                                       | SRC-004                                      | Tabla de especificaciones técnicas              | _"Gas spargers: Porous sparger / L-type sparger"_                                                                                                                                                      | Explícita                                    | Alta      | No                                              |
| AFI-31        | El recipiente del Biostat® B opera en el rango –1 a +2,5 barg a 150 °C                                                                                                                                                                                               | SRC-004                                      | Tabla de especificaciones técnicas              | _"Culture vessel design: -1 to + 2.5 barg @ 150 °C"_                                                                                                                                                   | Explícita                                    | Alta      | No                                              |
| AFI-32        | El Biostat® B controla temperatura entre 0 y 80 °C                                                                                                                                                                                                                   | SRC-004                                      | Tabla de especificaciones técnicas              | _"Temperature control: 0 – 80 °C"_                                                                                                                                                                     | Explícita                                    | Alta      | No                                              |
| AFI-33        | El Biostat® B dispone de los siguientes sensores: pH, pO₂, temperatura, espuma, nivel, adición de sustrato, mezcla de gases, agitación, control gravimétrico de alimentación y cosecha, control de flujo gaseoso constante, presión del recipiente, redox y turbidez | SRC-004                                      | Tabla de sensores                               | _"Sensors: pH, pO2, Temperature, Foam, Level, Substrate addition, Gas mixing, Agitation, Gravimetric Feed & Harvest Control, Constant Total Gas Flow Control, Vessel pressure, Redox & Turbidity"_     | Explícita                                    | Alta      | Recomendada (confirmar configuración instalada) |
| AFI-34        | El Biostat® B es el modelo estándar de industria para optimización y caracterización de procesos; es el modelo de escala reducida ideal para procesos a gran escala                                                                                                  | SRC-004                                      | Instrument Overview                             | _"The Industry Standard Bioreactor for Advanced Process Optimization and Characterization… ideal scale-down model for your large-scale process"_                                                       | Explícita                                    | Alta      | No                                              |
| AFI-35        | El tanque agitado de sobremesa consiste en un recipiente con proporción de dimensiones de altura definida, mezcla por agitador central accionado por motor en la placa de cabeza, y múltiples puertos para sondas, adición de sustratos, gases y muestras            | SRC-005                                      | Definición técnica                              | _"A stirred tank bioreactor consists of a vessel with a defined height dimension ratio. Mixing is achieved through a central stirrer element… multiple ports in the head plate"_                       | Explícita                                    | Alta      | No                                              |
| AFI-36        | Los STR de sobremesa tienen volúmenes de 1 a 10 L y se usan en laboratorios de investigación                                                                                                                                                                         | SRC-005                                      | Descripción de categoría                        | _"small-scale bioreactors with volumes from 1 to 10 L. These bioreactors are often used in research labs"_                                                                                             | Explícita                                    | Alta      | No                                              |
| AFI-37        | Los STR de sobremesa pueden funcionar como modelos de escala reducida para procesos comerciales a gran escala                                                                                                                                                        | SRC-005                                      | Descripción de categoría                        | _"can function as scale-down models for large commercial processes"_                                                                                                                                   | Explícita                                    | Alta      | No                                              |
| AFI-38        | Los STR exhiben excelente escalabilidad gracias a las proporciones constantes de altura/diámetro y diámetro de impulsor/diámetro del recipiente                                                                                                                      | SRC-005                                      | Sección de escalabilidad                        | _"well known for excellent scalability, as constant height to diameter ratios and vessel diameter to impeller diameter ratios can be achieved"_                                                        | Explícita                                    | Alta      | No                                              |
| AFI-39        | Los recipientes autoclavables del Biostat® B están disponibles de 1 a 10 L; los de un solo uso en 250 mL y 2 L                                                                                                                                                       | SRC-005                                      | Sección de recipientes                          | _"Autoclavable culture vessels are available from 1 L to 10 L and single use vessels of 250 mL and 2 L"_                                                                                               | Explícita                                    | Alta      | No                                              |
| AFI-40        | En una ontología conforme a BFO (como MCBO), el biorreactor no es un proceso sino una entidad material continua (continuant) que participa en el proceso de cultivo                                                                                                  | SRC-006                                      | Sección de modelado OWL / Figura 1              | _"MCBO strictly separates occurrents (processes) from continuants (material entities)… they inhere in a CellCultureSystem (e.g., the bioreactor, medium, and cells) that participates in the process"_ | Explícita                                    | Alta      | Sí (alineación BFO/IOF para este proyecto)      |
| AFI-41        | Las condiciones ambientales de cultivo son cualidades (qualities) del sistema material CellCultureSystem, no del proceso en sí                                                                                                                                       | SRC-006                                      | Sección de modelado OWL                         | _"Culture conditions are not modeled as qualities of the process itself; instead, they inhere in a CellCultureSystem"_                                                                                 | Explícita                                    | Alta      | Sí                                              |
| AFI-42        | Los procesos de cultivo celular mamífero se representan como clases OWL definidas con restricciones de participante, no como subclases primitivas                                                                                                                    | SRC-006                                      | Sección de modelado OWL                         | _"Mammalian cell culture processes are represented as OWL defined classes using participant restrictions rather than subclassing"_                                                                     | Explícita                                    | Alta      | Sí                                              |
| AFI-43        | El mecanismo de mezcla del BioLector XT es orbital (placa de microtitulación en agitación), a diferencia del impulsor central del STR                                                                                                                                | No establecido explícitamente en el corpus — | —                                               | Ningún fragmento de SRC-001 a SRC-008 describe el principio de mezcla del BioLector XT como "agitación orbital"                                                                                        | Inferida (del formato MTP)                   | Media     | Sí                                              |
| AFI-44        | El BioLector XT y los Sartorius 5 L / 10 L comparten la función de monitoreo y control en línea de parámetros de cultivo                                                                                                                                             | SRC-001, SRC-004, SRC-008                    | Múltiples secciones                             | Todos presentan medición en línea de pH, DO y temperatura; el BioLector añade biomasa óptica y fluorescencia                                                                                           | Inferida (de la lectura conjunta del corpus) | Alta      | Sí                                              |

---

## 4. Conceptos candidatos

| ID concepto | Concepto candidato      | Tipo sugerido                             | Definición basada exclusivamente en el corpus                                                                                                                                                                                 | Fuente principal | Estado                                                                |
| ----------- | ----------------------- | ----------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------- | --------------------------------------------------------------------- |
| CC-01       | `Bioreactor`            | Clase raíz                                | Dispositivo técnico diseñado para el cultivo aséptico y controlado de organismos biológicos, que asigna parámetros de cultivo y permite control riguroso del proceso con alta reproducibilidad                                | SRC-008          | Candidato                                                             |
| CC-02       | `Microbioreactor`       | Subclase de `Bioreactor`                  | Biorreactor de alto rendimiento basado en formato de placa de microtitulación (MTP), con sensores ópticos en línea y tecnología microfluídica para control de pH y alimentación; opera con múltiples pocillos paralelos       | SRC-001, SRC-002 | Candidato                                                             |
| CC-03       | `StirredTankBioreactor` | Subclase de `Bioreactor`                  | Biorreactor con recipiente de proporción de altura definida, mezcla por agitador central accionado por motor en la placa de cabeza, con puertos para sondas, gases, sustratos y muestreo                                      | SRC-005          | Candidato                                                             |
| CC-04       | `BenchtopBioreactor`    | Subclase de `StirredTankBioreactor`       | Tanque agitado de pequeña escala (1–10 L) de uso en laboratorio de investigación; puede funcionar como modelo de escala reducida para procesos comerciales; con pequeña huella de instalación                                 | SRC-005          | Candidato                                                             |
| CC-05       | `BioLectorXT`           | Individuo de `Microbioreactor`            | Sistema BioLector XT fabricado por m2p-labs / Beckman Coulter; basado en FlowerPlate MTP de 48 pocillos ANSI/SLAS; sensores ópticos de biomasa, pH, OD, fluorescencia; módulo microfluídico para control de pH y alimentación | SRC-001, SRC-002 | Candidato                                                             |
| CC-06       | `SartoriusBiostatB5L`   | Individuo de `BenchtopBioreactor`         | Configuración Biostat® B de Sartorius con recipiente de 5 L; volumen de trabajo 0,6–5 L; agitación 20–1 500 rpm; fabricado por Sartorius Stedim                                                                               | SRC-003, SRC-004 | Candidato                                                             |
| CC-07       | `SartoriusBiostatB10L`  | Individuo de `BenchtopBioreactor`         | Configuración Biostat® B de Sartorius con recipiente de 10 L; volumen de trabajo 1,5–10 L; agitación 20–800 rpm; fabricado por Sartorius Stedim                                                                               | SRC-003, SRC-004 | Candidato                                                             |
| CC-08       | `MicrotiterPlate`       | Clase                                     | Plato desechable de múltiples pocillos en formato estándar ANSI/SLAS (SBS), utilizado como recipiente de cultivo en el BioLector XT                                                                                           | SRC-001          | Candidato                                                             |
| CC-09       | `FlowerPlate`           | Subclase de `MicrotiterPlate` o Individuo | Placa de microtitulación patentada de 48 pocillos utilizada en el sistema BioLector XT; tecnología específica de m2p-labs                                                                                                     | SRC-002          | Candidato                                                             |
| CC-10       | `OpticalSensor`         | Subclase de `OnlineSensor`                | Sensor precalibrado basado en principios ópticos para medición en línea de biomasa, pH, OD y fluorescencia; usado en el BioLector XT                                                                                          | SRC-001          | Candidato                                                             |
| CC-11       | `ElectrochemicalSensor` | Subclase de `OnlineSensor` (candidato)    | Sensor para medición de pH, pO₂, redox; usado en el Biostat® B                                                                                                                                                                | SRC-004          | Candidato — tipo de sensor no explicitado en el corpus para Sartorius |
| CC-12       | `CellCultureSystem`     | Clase (referenciada de MCBO/BFO)          | Sistema material compuesto por el biorreactor, el medio de cultivo y las células; sus cualidades representan las condiciones ambientales del cultivo; participante en el proceso de cultivo                                   | SRC-006          | Candidato — de ontología externa; requiere alineación                 |
| CC-13       | `OperationMode`         | Clase o Propiedad de dato                 | Modo de ejecución del proceso de cultivo en el biorreactor: batch, fed-batch, bolus, continuo, perfusión                                                                                                                      | SRC-001, SRC-003 | Candidato                                                             |
| CC-14       | `WorkingVolume`         | Propiedad de dato                         | Volumen efectivo de cultivo en el biorreactor bajo condiciones operativas; expresado en L o mL                                                                                                                                | SRC-004, SRC-005 | Candidato                                                             |
| CC-15       | `AgitationSpeed`        | Propiedad de dato                         | Velocidad de agitación del impulsor o del sistema de mezcla; expresada en rpm                                                                                                                                                 | SRC-004          | Candidato                                                             |
| CC-16       | `GassingSystem`         | Clase o Propiedad de objeto               | Sistema de suministro de gases al biorreactor; incluye tipo y caudal de gases; controlado por controladores de flujo másico en el Biostat® B                                                                                  | SRC-003, SRC-004 | Candidato                                                             |
| CC-17       | `Sparger`               | Clase                                     | Dispositivo de introducción de gas en el líquido de cultivo; tipos documentados: poroso y tipo L                                                                                                                              | SRC-004          | Candidato                                                             |
| CC-18       | `HeadPlate`             | Clase                                     | Placa de cabeza del recipiente del STR; contiene puertos para sondas, sustratos, gas y muestreo; aloja el motor del agitador                                                                                                  | SRC-005          | Candidato                                                             |
| CC-19       | `MicrofluidicModule`    | Clase                                     | Módulo opcional del BioLector XT que permite dosificación de líquidos a escala de nanolitro mediante microválvulas; habilita control de pH específico por pocillo y estrategias de alimentación                               | SRC-001          | Candidato                                                             |
| CC-20       | `CellCultureProcess`    | Clase (referenciada de MCBO)              | Occurrente (proceso) en el que el biorreactor participa como entidad material; incluye subclases BatchCultureProcess, FedBatchCultureProcess, ContinuousCultureProcess, PerfusionCultureProcess                               | SRC-006          | Candidato — de ontología externa                                      |
| CC-21       | `OperationScale`        | Concepto auxiliar                         | Clasificación del biorreactor según el orden de magnitud del volumen de trabajo; distingue escala micro (BioLector XT) de escala de laboratorio (Sartorius 5 L / 10 L)                                                        | SRC-005, SRC-007 | Candidato                                                             |
| CC-22       | `DCUControlTower`       | Clase o Individuo                         | Torre de control digital (DCU) del Biostat® B; controla hasta dos unidades de cultivo independientemente; incluye módulos de gasificación, bombeo y temperatura                                                               | SRC-003          | Candidato                                                             |

---

## 5. Relaciones candidatas con dominio y rango sugeridos

| ID relación | Relación candidata           | Dominio sugerido                                 | Rango sugerido                         | Significado                                                                                        | Fuente principal                              | Estado                                                               |
| ----------- | ---------------------------- | ------------------------------------------------ | -------------------------------------- | -------------------------------------------------------------------------------------------------- | --------------------------------------------- | -------------------------------------------------------------------- |
| REL-01      | `rdfs:subClassOf`            | `Microbioreactor`                                | `Bioreactor`                           | El microbiorreactor es un tipo de biorreactor                                                      | SRC-001, SRC-008                              | Candidato                                                            |
| REL-02      | `rdfs:subClassOf`            | `StirredTankBioreactor`                          | `Bioreactor`                           | El tanque agitado es un tipo de biorreactor                                                        | SRC-005, SRC-008                              | Candidato                                                            |
| REL-03      | `rdfs:subClassOf`            | `BenchtopBioreactor`                             | `StirredTankBioreactor`                | El biorreactor de sobremesa es un tanque agitado a escala de laboratorio                           | SRC-005                                       | Candidato                                                            |
| REL-04      | `rdf:type`                   | `BioLectorXT`                                    | `Microbioreactor`                      | El BioLector XT es un individuo de la clase Microbioreactor                                        | SRC-001, SRC-002                              | Candidato                                                            |
| REL-05      | `rdf:type`                   | `SartoriusBiostatB5L`                            | `BenchtopBioreactor`                   | El Biostat® B 5 L es un individuo de la clase BenchtopBioreactor                                   | SRC-003, SRC-004                              | Candidato                                                            |
| REL-06      | `rdf:type`                   | `SartoriusBiostatB10L`                           | `BenchtopBioreactor`                   | El Biostat® B 10 L es un individuo de la clase BenchtopBioreactor                                  | SRC-003, SRC-004                              | Candidato                                                            |
| REL-07      | `hasWorkingVolume`           | `Bioreactor`                                     | `xsd:string` o clase `QuantityValue`   | El biorreactor tiene un volumen de trabajo nominal definido                                        | SRC-004, SRC-005                              | Candidato                                                            |
| REL-08      | `hasAgitationSpeedRange`     | `StirredTankBioreactor`                          | `xsd:string` o clase `QuantityRange`   | El STR tiene un rango de velocidad de agitación                                                    | SRC-004                                       | Candidato                                                            |
| REL-09      | `hasOnlineSensor`            | `Bioreactor`                                     | `OnlineSensor`                         | El biorreactor dispone de sensores de monitoreo en línea                                           | SRC-001, SRC-004                              | Candidato                                                            |
| REL-10      | `hasMixingPrinciple`         | `Bioreactor`                                     | `xsd:string` o clase `MixingPrinciple` | El biorreactor emplea un principio de mezcla particular                                            | SRC-005, SRC-001 (inferida para BioLector XT) | Candidato — requiere validación experta para BioLector XT            |
| REL-11      | `supportsOperationMode`      | `Bioreactor`                                     | `OperationMode`                        | El biorreactor soporta uno o más modos de operación de proceso                                     | SRC-001, SRC-003                              | Candidato                                                            |
| REL-12      | `manufacturedBy`             | `Bioreactor`                                     | `Organization`                         | El biorreactor fue fabricado por una organización específica                                       | SRC-002, SRC-004                              | Candidato                                                            |
| REL-13      | `hasGassingSystem`           | `Bioreactor`                                     | `GassingSystem`                        | El biorreactor incorpora un sistema de suministro de gases                                         | SRC-003, SRC-004                              | Candidato                                                            |
| REL-14      | `hasSparger`                 | `StirredTankBioreactor`                          | `Sparger`                              | El STR dispone de uno o más tipos de sparger                                                       | SRC-004                                       | Candidato                                                            |
| REL-15      | `hasHeadPlate`               | `StirredTankBioreactor`                          | `HeadPlate`                            | El STR tiene una placa de cabeza con puertos específicos                                           | SRC-005                                       | Candidato                                                            |
| REL-16      | `hasCultivationFormat`       | `Microbioreactor`                                | `MicrotiterPlate`                      | El microbiorreactor utiliza una placa de microtitulación como recipiente de cultivo                | SRC-001                                       | Candidato                                                            |
| REL-17      | `hasMicrofluidicModule`      | `BioLectorXT`                                    | `MicrofluidicModule`                   | El BioLector XT puede equiparse con módulo microfluídico opcional                                  | SRC-001                                       | Candidato                                                            |
| REL-18      | `participatesIn`             | `Bioreactor` (como parte de `CellCultureSystem`) | `CellCultureProcess`                   | El biorreactor, como parte del sistema de cultivo, participa en el proceso de cultivo              | SRC-006                                       | Candidato — patrón BFO; requiere validación de alineación ontológica |
| REL-19      | `operatesAtScale`            | `Bioreactor`                                     | `OperationScale`                       | El biorreactor opera a una escala definida (micro / laboratorio)                                   | SRC-005, SRC-007                              | Candidato                                                            |
| REL-20      | `hasTemperatureControlRange` | `Bioreactor`                                     | `xsd:string` o `QuantityRange`         | El biorreactor controla temperatura en un rango definido                                           | SRC-004                                       | Candidato — solo confirmado para Biostat® B en el corpus             |
| REL-21      | `isScaleDownModelOf`         | `BenchtopBioreactor`                             | `Bioreactor` (escala mayor)            | El biorreactor de sobremesa puede actuar como modelo de escala reducida de sistemas a mayor escala | SRC-004, SRC-005                              | Candidato                                                            |
| REL-22      | `hasControlSystem`           | `SartoriusBiostatB5L`, `SartoriusBiostatB10L`    | `DCUControlTower`                      | El Biostat® B está controlado por una torre DCU                                                    | SRC-003                                       | Candidato                                                            |

---

## 6. Triadas RDF candidatas

```turtle
# ─── JERARQUÍA DE CLASES ─────────────────────────────────────
Microbioreactor
    rdfs:subClassOf Bioreactor .
# Soportada | SRC-001, SRC-008 | Descripción principal del BioLector XT + definición farmacéutica

StirredTankBioreactor
    rdfs:subClassOf Bioreactor .
# Soportada | SRC-005, SRC-008 | Definición técnica del STR + definición farmacéutica

BenchtopBioreactor
    rdfs:subClassOf StirredTankBioreactor .
# Soportada | SRC-005 | "small-scale bioreactors with volumes from 1 to 10 L… used in research labs"

# ─── INSTANCIACIÓN DE INDIVIDUOS ─────────────────────────────
BioLectorXT
    rdf:type Microbioreactor .
# Soportada | SRC-001, SRC-002 | "high-throughput microbioreactor"

SartoriusBiostatB5L
    rdf:type BenchtopBioreactor .
# Soportada | SRC-003, SRC-004 | Recipiente de 5 L, controlador DCU de sobremesa

SartoriusBiostatB10L
    rdf:type BenchtopBioreactor .
# Soportada | SRC-003, SRC-004 | Recipiente de 10 L, controlador DCU de sobremesa

# ─── FABRICANTES ─────────────────────────────────────────────
BioLectorXT
    :manufacturedBy :BeckmanCoulterLifeSciences .
# Soportada | SRC-002 | "from m2p-labs, part of the Beckman Coulter Life Sciences'
#   Biotechnology Business Unit since November 2020"

SartoriusBiostatB5L
    :manufacturedBy :Sartorius .
# Soportada | SRC-003, SRC-004 | "Manufacturer: Sartorius Stedim"

SartoriusBiostatB10L
    :manufacturedBy :Sartorius .
# Soportada | SRC-003, SRC-004 | Idem

# ─── FORMATO DE CULTIVO ───────────────────────────────────────
BioLectorXT
    :hasCultivationFormat :MicrotiterPlate_48well_ANSI_SLAS .
# Soportada | SRC-001 | "based on a standard ANSI/SLAS (SBS) microtiter plate (MTP) format,
#   Disposable 48 well MTPs"

BioLectorXT
    :hasCultivationFormat :FlowerPlate .
# Soportada | SRC-002 | "patented FlowerPlate microtiter plate technology"

# ─── SENSORES EN LÍNEA ────────────────────────────────────────
BioLectorXT
    :hasOnlineSensor :BiomassSensor_Optical ,
                     :pHSensor_Optical ,
                     :DissolvedOxygenSensor_Optical ,
                     :FluorescenceSensor_Optical .
# Soportada | SRC-001 | "real-time evaluation of biomass, fluorescence, pH,
#   dissolved oxygen… online, pre-calibrated optical sensors"

SartoriusBiostatB5L
    :hasOnlineSensor :pHSensor ,
                     :DissolvedOxygenSensor_pO2 ,
                     :TemperatureSensor ,
                     :FoamSensor ,
                     :LevelSensor ,
                     :SubstrateAdditionSensor ,
                     :GasMixingSensor ,
                     :AgitationSensor ,
                     :GravimetricFeedHarvestControl ,
                     :ConstantTotalGasFlowControl ,
                     :VesselPressureSensor ,
                     :RedoxSensor ,
                     :TurbiditySensor .
# Soportada | SRC-004 | Tabla completa de sensores del Biostat® B

SartoriusBiostatB10L
    :hasOnlineSensor :pHSensor ,
                     :DissolvedOxygenSensor_pO2 ,
                     :TemperatureSensor ,
                     :FoamSensor ,
                     :LevelSensor ,
                     :SubstrateAdditionSensor ,
                     :GasMixingSensor ,
                     :AgitationSensor ,
                     :GravimetricFeedHarvestControl ,
                     :ConstantTotalGasFlowControl ,
                     :VesselPressureSensor ,
                     :RedoxSensor ,
                     :TurbiditySensor .
# Soportada | SRC-004 | Idem — la tabla de SRC-004 no diferencia entre 5L y 10L;
#   aplica igualmente a ambas configuraciones

# ─── VOLÚMENES DE TRABAJO ────────────────────────────────────
SartoriusBiostatB5L
    :hasWorkingVolume "0.6–5 L"^^xsd:string .
# Soportada | SRC-004 | "5L (0.6-5L)"

SartoriusBiostatB10L
    :hasWorkingVolume "1.5–10 L"^^xsd:string .
# Soportada | SRC-004 | "10L (1.5-10L)"

BioLectorXT
    :hasWorkingVolume [VALOR NO ESTABLECIDO EN EL CORPUS] .
# No soportada — el corpus no contiene el volumen por pocillo del BioLector XT

# ─── VELOCIDAD DE AGITACIÓN ──────────────────────────────────
SartoriusBiostatB5L
    :hasAgitationSpeedRange "20–1500 rpm"^^xsd:string .
# Soportada | SRC-004 | "5L (20-1500rpm)"

SartoriusBiostatB10L
    :hasAgitationSpeedRange "20–800 rpm"^^xsd:string .
# Soportada | SRC-004 | "10L (20-800rpm)"

# ─── CONTROL DE TEMPERATURA ──────────────────────────────────
SartoriusBiostatB5L
    :hasTemperatureControlRange "0–80 °C"^^xsd:string .
# Soportada | SRC-004 | "Temperature control: 0 – 80 °C"

SartoriusBiostatB10L
    :hasTemperatureControlRange "0–80 °C"^^xsd:string .
# Soportada | SRC-004 | Idem

# ─── MODOS DE OPERACIÓN ──────────────────────────────────────
BioLectorXT
    :supportsOperationMode :BatchProcess ,
                           :FedBatchProcess ,
                           :BolusProcess ,
                           :ContinuousProcess .
# Soportada | SRC-001 | "Customizable feeding strategies (batch, fed-batch, bolus, continuous)"

SartoriusBiostatB5L
    :supportsOperationMode :BatchProcess ,
                           :FedBatchProcess ,
                           :ContinuousProcess ,
                           :PerfusionProcess .
# Soportada | SRC-003 | "batch, fed-batch, continuous or perfusion mode"

SartoriusBiostatB10L
    :supportsOperationMode :BatchProcess ,
                           :FedBatchProcess ,
                           :ContinuousProcess ,
                           :PerfusionProcess .
# Soportada | SRC-003 | Idem

# ─── SISTEMA DE GASIFICACIÓN ─────────────────────────────────
SartoriusBiostatB5L
    :hasGassingSystem :GasSystem_Air_O2_CO2_N2_20lpm .
# Soportada | SRC-004 | "Gas flow: air, O2, CO2*, N2 (max. total flow rate 20 lpm)"

SartoriusBiostatB10L
    :hasGassingSystem :GasSystem_Air_O2_CO2_N2_20lpm .
# Soportada | SRC-004 | Idem

BioLectorXT
    :hasGassingSystem :GasSystem_O2_1to100pct_CO2_1to12pct .
# Soportada | SRC-001 | "Gassing with O2 within a range of 1%–100% and with CO2 within 1%–12%"

# ─── SPARGERS ────────────────────────────────────────────────
SartoriusBiostatB5L
    :hasSparger :PorousSparger , :LTypeSparger .
# Soportada | SRC-004 | "Gas spargers: Porous sparger / L-type sparger"

SartoriusBiostatB10L
    :hasSparger :PorousSparger , :LTypeSparger .
# Soportada | SRC-004 | Idem

# ─── MÓDULO MICROFLUÍDICO ────────────────────────────────────
BioLectorXT
    :hasMicrofluidicModule :MicrofluidicModule_optional .
# Soportada (con condición) | SRC-001 | "The optional microfluidic module"

:MicrofluidicModule_optional
    :enablesLiquidDosageScale "nanolitre"^^xsd:string .
# Soportada | SRC-001 | "Microvalves allot liquids at the nanolitre scale"

:MicrofluidicModule_optional
    :reservoirWellRatio "2 reservoir wells per 4 cultivation wells"^^xsd:string .
# Soportada | SRC-001 | "Enables the use of 2 reservoir wells per 4 cultivation wells"

# ─── CONTROL DCU (SARTORIUS) ─────────────────────────────────
SartoriusBiostatB5L
    :hasControlSystem :DCUControlTower .
# Soportada | SRC-003 | "all controlled with one DCU tower"

SartoriusBiostatB10L
    :hasControlSystem :DCUControlTower .
# Soportada | SRC-003 | Idem

:DCUControlTower
    :hasMassFlowControllers "up to 4"^^xsd:string .
# Soportada | SRC-003 | "Gassing system… with up to four mass flow controller"

# ─── ESCALA DE OPERACIÓN ─────────────────────────────────────
BioLectorXT
    :operatesAtScale :MicroScale .
# Parcialmente soportada | SRC-007 | Denominado "µ-bioreactor";
#   escala numérica no establecida en el corpus

SartoriusBiostatB5L
    :operatesAtScale :LaboratoryScale .
# Soportada | SRC-005 | "small-scale bioreactors with volumes from 1 to 10 L…
#   used in research labs"

SartoriusBiostatB10L
    :operatesAtScale :LaboratoryScale .
# Soportada | SRC-005 | Idem

# ─── PRINCIPIO DE MEZCLA ─────────────────────────────────────
SartoriusBiostatB5L
    :hasMixingPrinciple :CentralImpellerAgitation .
# Soportada | SRC-005 | "Mixing is achieved through a central stirrer element
#   inside the culture vessel"

SartoriusBiostatB10L
    :hasMixingPrinciple :CentralImpellerAgitation .
# Soportada | SRC-005 | Idem

BioLectorXT
    :hasMixingPrinciple :OrbitalShaking_MTP .
# Parcialmente soportada — inferida | SRC-001, SRC-002 |
#   El corpus no enuncia "orbital shaking" explícitamente;
#   se infiere del formato MTP/FlowerPlate; REQUIERE VALIDACIÓN EXPERTA

# ─── PATRÓN BFO (MCBO) ───────────────────────────────────────
:CellCultureSystem
    rdf:type owl:Class ;
    rdfs:comment "Material entity (continuant) that includes the bioreactor,
                  culture medium, and cells; cultural conditions inhere in it" .
# Soportada | SRC-006 | "they inhere in a CellCultureSystem (e.g., the bioreactor,
#   medium, and cells)"

BioLectorXT
    :isPartOf :CellCultureSystem .
# Parcialmente soportada — inferida desde el patrón MCBO | SRC-006 |
#   El corpus menciona el biorreactor como ejemplo del CellCultureSystem
#   pero no instancia específicamente el BioLectorXT en esa clase;
#   REQUIERE VALIDACIÓN EXPERTA DE ALINEACIÓN

# ─── ESCALA REDUCIDA ─────────────────────────────────────────
SartoriusBiostatB5L
    :isScaleDownModelOf :LargeScaleBioreactor .
# Soportada | SRC-004 | "ideal scale-down model for your large-scale process"

SartoriusBiostatB10L
    :isScaleDownModelOf :LargeScaleBioreactor .
# Soportada | SRC-004 | Idem

# ─── SUCESIÓN DE PRODUCTO ────────────────────────────────────
BioLectorXT
    :succeedsProduct :BioLectorPro .
# Soportada | SRC-002 | "The BioLector XT Microbioreactor succeeds
#   the BioLector Pro Microbioreactor"
```

---

## 7. Sinónimos documentados

| Término principal       | Sinónimos/variantes en el corpus                                                              | Idioma en el corpus | Fuente                    |
| ----------------------- | --------------------------------------------------------------------------------------------- | ------------------- | ------------------------- |
| `Bioreactor`            | fermenter, fermentador, bioreactor, culture vessel, cultivation vessel                        | EN                  | SRC-004, SRC-005, SRC-008 |
| `Microbioreactor`       | micro-bioreactor, µ-bioreactor, high-throughput microbioreactor, HTP bioreactor               | EN                  | SRC-001, SRC-002, SRC-007 |
| `StirredTankBioreactor` | stirred tank bioreactor, STR, stirred tank fermenter (STF), tanque agitado                    | EN                  | SRC-005, SRC-007          |
| `BenchtopBioreactor`    | benchtop bioreactor, laboratory bioreactor, lab-scale bioreactor, benchtop fermenter          | EN                  | SRC-005                   |
| `BioLectorXT`           | BioLector XT Microbioreactor, BioLector XT, M2P-G-BLXT (número de parte en SRC-002 implícito) | EN                  | SRC-001, SRC-002          |
| `BioLectorPro`          | BioLector Pro Microbioreactor (predecesor del XT)                                             | EN                  | SRC-002                   |
| `SartoriusBiostatB`     | Biostat® B, BIOSTAT B, Biostat B, Biostat B-DCUII                                             | EN                  | SRC-003, SRC-004          |
| `MicrotiterPlate`       | MTP, microtiter plate, SBS plate, ANSI/SLAS plate, well plate                                 | EN                  | SRC-001, SRC-002          |
| `FlowerPlate`           | FlowerPlate microtiter plate, FlowerPlate MTP, patented FlowerPlate                           | EN                  | SRC-002                   |
| `DissolvedOxygen`       | DO, pO₂, dissolved oxygen, oxígeno disuelto                                                   | EN                  | SRC-001, SRC-004          |
| `FedBatchProcess`       | fed-batch, fed-batch mode, fed-batch cultivation, enzymatic substrate release fed-batch       | EN                  | SRC-001, SRC-003, SRC-007 |
| `ContinuousProcess`     | continuous, continuous mode, chemostat (en MCBO), ChemostatCultureProcess                     | EN                  | SRC-001, SRC-003, SRC-006 |
| `PerfusionProcess`      | perfusion, perfusion mode, PerfusionCultureProcess                                            | EN                  | SRC-003, SRC-006          |
| `CellCultureSystem`     | cell culture system, bioreactor + medium + cells                                              | EN                  | SRC-006                   |
| `DCUControlTower`       | DCU tower, DCU, Digital Control Unit (inferido del acrónimo)                                  | EN                  | SRC-003                   |

---

## 8. Vacíos del corpus

| ID vacío | Información faltante                                                                                                                                                                           | Impacto ontológico                                                                                                                                    | Acción recomendada                                                                                                                                |
| -------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------- |
| GAP-01   | **Volumen de trabajo por pocillo del BioLector XT** no figura en ninguno de los ocho fragmentos. El TDS oficial (DOC-03) no fue descargable.                                                   | Impide completar la triada `BioLectorXT → hasWorkingVolume → [valor]`; la comparación cuantitativa de escalas queda incompleta.                       | Descargar el TDS desde `beckman.com/resources/reading-material/product-instructions/biolector-xt-technical-data-sheet` e incorporar como SRC-009. |
| GAP-02   | **Principio de mezcla del BioLector XT** ("agitación orbital") no es enunciado explícitamente en ningún fragmento; solo se infiere del formato MTP.                                            | La triada `BioLectorXT → hasMixingPrinciple → OrbitalShaking_MTP` es inferida, no explícita; riesgo de error conceptual si el principio real difiere. | Validación experta o consulta del manual técnico.                                                                                                 |
| GAP-03   | **Tipo de sensores del BioLector XT** para gases (CO₂ en líquido, N₂, presión) no descritos en el corpus más allá de biomasa, pH, OD, fluorescencia.                                           | Los sensores de gas en fase líquida del BioLector XT quedan sin representar en la ontología.                                                          | Consultar TDS oficial (DOC-03) o manual de usuario.                                                                                               |
| GAP-04   | **Configuración específica de sensores instalados en el laboratorio del proyecto** para ambos Sartorius. La lista de SRC-004 es la configuración completa opcional, no la instalada.           | La triada `hasOnlineSensor` puede sobrerrepresentar sensores no presentes en los equipos reales.                                                      | Validación experta con el operador de laboratorio; revisión de inventario de instrumentos.                                                        |
| GAP-05   | **Modo de operación perfusión en BioLector XT**: SRC-001 lista "batch, fed-batch, bolus, continuous" pero no "perfusión". No se puede afirmar ni negar si soporta perfusión.                   | La comparación de modos de operación entre BioLector XT y Sartorius queda asimétrica.                                                                 | Verificar en TDS o manual.                                                                                                                        |
| GAP-06   | **Tipo de recipiente del Sartorius 5 L y 10 L en el proyecto** (vidrio reutilizable vs. de un solo uso): SRC-003 lista ambas opciones pero el corpus no especifica cuál se usa en el proyecto. | El individuo ontológico necesita la propiedad `hasVesselType`; sin ella, queda ambiguo.                                                               | Consulta con el investigador/operador del laboratorio.                                                                                            |
| GAP-07   | **Definición normativa de biorreactor** (ISO, ASTM, ANSI): ninguna fuente del corpus cita una norma formal. La definición de SRC-008 es académica, no normativa.                               | La clase `Bioreactor` no puede anclarse a una norma formal en esta iteración.                                                                         | Búsqueda específica de normas ISO/ANSI sobre biorreactores para incorporar como fuente adicional.                                                 |
| GAP-08   | **Parámetros de transferencia de masa (kLa)** del BioLector XT no figuran en el corpus; SRC-007 alude a diferencias con el STR pero no aporta valores.                                         | La equivalencia funcional cuantitativa entre escalas (criterio de scale-up) no puede ser representada ontológicamente con este corpus.                | Incorporar artículo de Kensy et al. (DOC-09, PMC2806293) marcado como Uncertain.                                                                  |
| GAP-09   | **Versión de software/firmware de control** del Biostat® B (Biobrain®, MFCS) no establecida en los fragmentos del corpus (mencionado en SRC-003 solo como nombre de producto sin detalles).    | Las propiedades de software del sistema de control no pueden representarse.                                                                           | Consultar documentación técnica del Biobrain® o MFCS.                                                                                             |
| GAP-10   | **Número paralelo de pocillos activos del BioLector XT en modo microfluídico**: SRC-001 menciona "48/32 parallel cultivations" sin especificar cuándo aplica cada número.                      | La propiedad `hasMaxParallelCultivations` necesita condiciones de aplicación para ser correctamente representada.                                     | Consultar TDS oficial.                                                                                                                            |

---

## 9. Estado final

| Dimensión                          | Estado                          | Observación                                                                                                                                                                                                                                                                                                                                 |
| ---------------------------------- | ------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Respuesta a la pregunta ALC-01** | **Parcialmente soportada**      | La definición general de biorreactor y las especificaciones de los Sartorius 5 L / 10 L están bien soportadas por evidencia explícita de alta confianza. La caracterización del BioLector XT como microbiorreactor está soportada, pero su volumen de trabajo por pocillo y su principio de mezcla no están explícitos en el corpus actual. |
| **Conceptos candidatos**           | **22 conceptos identificados**  | 7 con soporte explícito alto; 2 referenciados de ontología externa (MCBO/BFO) que requieren alineación; los demás, inferidos con confianza media o dependientes de TDS faltante.                                                                                                                                                            |
| **Relaciones candidatas**          | **22 relaciones identificadas** | 18 con soporte explícito; 4 inferidas o parcialmente soportadas que requieren validación experta (mezcla orbital del BioLector XT, equivalencia funcional entre escalas, alineación BFO).                                                                                                                                                   |
| **Triadas RDF candidatas**         | **~45 triadas formuladas**      | Aproximadamente 35 soportadas; ~8 parcialmente soportadas; 2 no soportadas (volumen BioLector XT; alineación BFO sin confirmación).                                                                                                                                                                                                         |
| **Corpus**                         | **Parcial**                     | Suficiente para la caracterización general y propuesta ontológica inicial; incompleto para especificaciones numéricas del BioLector XT (GAP-01) y configuración real de laboratorio (GAP-04, GAP-06).                                                                                                                                       |
| **Próxima acción crítica**         | —                               | Incorporar DOC-03 (TDS BioLector XT) y DOC-09 (Kensy et al.) al corpus; obtener confirmación del investigador sobre tipo de recipiente y configuración de sensores instalados; someter GAP-02 y GAP-08 a validación experta.                                                                                                                |
