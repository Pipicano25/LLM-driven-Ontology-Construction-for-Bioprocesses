# ALC-06: ¿Qué propiedades generales deben describir cualquier biorreactor del proyecto, independientemente de su escala o volumen?

---

## 1. Identificación de la pregunta

- **ID:** ALC-06
- **Nivel metodológico:** Ontológico-estructural (definición de propiedades abstractas transversales)
- **Tema:** Propiedades generales invariantes de biorreactor
- **Pregunta:** ¿Qué propiedades generales deben describir cualquier biorreactor del proyecto, independientemente de su escala o volumen?

---

## 2. Propósito de la pregunta

Esta pregunta busca identificar el conjunto mínimo de atributos descriptivos que son comunes a **todos** los sistemas biorreactor del proyecto (BioLector XT, Sartorius 5 L y Sartorius 10 L), con independencia de sus diferencias de escala, formato o tecnología. Su respuesta es esencial para definir la **clase abstracta `Bioreactor`** en la ontología OWL/RDF, de la cual todos los sistemas individuales serán individuos o subclases. Este núcleo de propiedades compartidas determina las **data properties** y **object properties** que toda instancia de biorreactor deberá heredar, asegurando comparabilidad semántica entre escalas y consistencia representacional en la ontología multiescala del proyecto.

---

## 3. Plan de búsqueda documental

**Información técnica requerida:**

- Definición estándar de biorreactor (estructura, funciones obligatorias)
- Propiedades físicas, químicas y operativas comunes a todo biorreactor
- Propiedades de identificación (nombre, modelo, fabricante, escala)
- Clasificaciones de modo de operación (batch, fed-batch, continuo)
- Enfoques ontológicos para representar propiedades de equipos de bioprocesos

**Tipos de documentos:**

- Fichas técnicas y hojas de especificaciones oficiales de fabricante
- Artículos científicos revisados por pares sobre ontologías de bioprocesos
- Revisiones técnicas sobre diseño de biorreactores
- Documentos de organismos estándar (NIST, IOF, ISA-88)

**Repositorios y sitios sugeridos:**

- `sartorius.com`, `m2p-labs.com`, `beckman.com`
- PubMed, ScienceDirect, bioRxiv
- NIST Publications (`nist.gov/publications`)
- IOF GitHub (`github.com/iofoundry`)
- OBO Foundry (`obofoundry.org`)

**Términos de búsqueda:**

| Español                                       | Inglés                                                   |
| --------------------------------------------- | -------------------------------------------------------- |
| Propiedades generales biorreactor             | Bioreactor general properties                            |
| Biorreactor clasificación y características   | Bioreactor classification instrumentation sensors        |
| Ontología equipos bioproceso                  | Bioprocess equipment ontology OWL                        |
| Volumen de trabajo, agitación, aireación      | Working volume, agitation, aeration, pH, DO, temperature |
| Propiedades comunes biorreactores multiescala | Common bioreactor properties multiscale                  |

**Ecuaciones de búsqueda sugeridas:**

- `bioreactor general properties working volume agitation aeration pH temperature DO sensors standard classification`
- `BioLector XT technical specifications sensors working volume m2p-labs`
- `Sartorius BIOSTAT B 5L 10L bioreactor technical specifications sensors`
- `NIST biomanufacturing ontology bioreactor properties BFO OWL 2024`

---

## 4. Documentos candidatos encontrados

| ID doc | Título                                                                                                                                        | Entidad autora                       |     Año | Tipo de fuente                                    | URL/DOI verificable                                                                                    | Relación con la pregunta                                                                                       | Decisión preliminar |
| ------ | --------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------ | ------: | ------------------------------------------------- | ------------------------------------------------------------------------------------------------------ | -------------------------------------------------------------------------------------------------------------- | ------------------- |
| D01    | BioLector XT Technical Specifications (PDF)                                                                                                   | m2p-labs / Beckman Coulter           |    2021 | Ficha técnica oficial de fabricante               | https://star-lab.am/upload/iblock/090/...specifikaciya.pdf                                             | Directa: define propiedades del BioLector XT (temperatura, agitación, DO, pH, volumen, gaseado)                | Include             |
| D02    | BIOSTAT® Bplus Exclusive Flow Specifications (PDF)                                                                                            | Sartorius Stedim Biotech             |    2023 | Ficha técnica oficial de fabricante               | https://www.richmondscientific.com/...Specifications.pdf                                               | Directa: define propiedades del Sartorius 5 L y 10 L (volumen, sensores, agitación, temperatura, pH, DO, etc.) | Include             |
| D03    | Bioreactor – an overview (ScienceDirect Topics)                                                                                               | ScienceDirect / Elsevier             | Vigente | Revisión enciclopédica técnica                    | https://www.sciencedirect.com/topics/engineering/bioreactor                                            | Directa: define propiedades generales de biorreactores (flujos, aireación, temperatura, pH, agitación, espuma) | Include             |
| D04    | MCBO: Mammalian Cell Bioprocessing Ontology (bioRxiv)                                                                                         | Autores múltiples (preprint bioRxiv) |    2026 | Preprint científico (no peer-reviewed aún)        | https://www.biorxiv.org/content/10.64898/2026.01.05.697007v1                                           | Indirecta: propiedades ontológicas de biorreactores según BFO/IOF, modelado de condiciones de cultivo          | Uncertain           |
| D05    | A Basic Formal Ontology-Based Ontological Modeling for Plan and Occurrence, a Biomanufacturing Process Verification Use Case (NIST/ASME 2024) | NIST / Šormaz et al.                 |    2024 | Artículo científico en proceedings (ASME)         | https://doi.org/10.1115/DETC2024-143710                                                                | Indirecta: uso de BFO/IOF para representar operación de biorreactor en bioprocesos                             | Uncertain           |
| D06    | PREFER: An Ontology for the PREcision FERmentation Community (arXiv)                                                                          | Autores múltiples                    |    2025 | Preprint científico                               | https://arxiv.org/pdf/2602.16755                                                                       | Indirecta: conceptos ontológicos de calidad, rol y unidad aplicables a biorreactores                           | Uncertain           |
| D07    | Towards Ontologizing a Digital Twin Framework for Manufacturing (NIST)                                                                        | NIST                                 |    2023 | Artículo técnico NIST                             | https://tsapps.nist.gov/publication/get_pdf.cfm?pub_id=936637                                          | Indirecta: modelo digital twin de biorreactor con sensores, actuadores y control de parámetros                 | Uncertain           |
| D08    | A Complete Guide to What Bioreactors Are and How They Work (IFP)                                                                              | International Filter Products        |    2025 | Blog técnico con descripción técnica estructurada | https://internationalfilterproducts.com/blogs/ifp-blog/...                                             | Parcial: describe estructura y propiedades generales de biorreactores                                          | Exclude             |
| D09    | Deep Dive: Fermentation Upstream Bioprocess Design (GFI)                                                                                      | Good Food Institute                  |    2025 | Revisión técnica (institución de investigación)   | https://gfi.org/science/the-science-of-fermentation/deep-dive-fermentation-upstream-bioprocess-design/ | Parcial: clasifica propiedades de biorreactor en físicas, químicas y biológicas                                | Include             |

---

## 5. Evaluación de documentos candidatos

| ID doc | Relevancia | Autoridad | Trazabilidad | Cobertura pregunta | Evidencia localizable | Justificación                                                                                                                                                                         |
| ------ | ---------- | --------- | ------------ | ------------------ | --------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| D01    | Alta       | Alta      | Alta         | Alta               | Alta                  | Ficha técnica oficial de m2p-labs/Beckman Coulter (2021), accesible en PDF con especificaciones numéricas verificables de temperatura, agitación, DO, pH, volumen, módulos opcionales |
| D02    | Alta       | Alta      | Alta         | Alta               | Alta                  | Ficha técnica oficial de Sartorius (2023), accesible en PDF con rangos exactos para 5 L y 10 L: volumen de trabajo, sensores, agitación, temperatura, gaseado, controladores          |
| D03    | Alta       | Media     | Media        | Alta               | Media                 | Fuente enciclopédica de ScienceDirect, revisada técnicamente, enumera propiedades estándar de biorreactores; no es artículo peer-reviewed pero es síntesis de literatura técnica      |
| D04    | Media      | Media     | Media        | Media              | Media                 | Preprint bioRxiv 2026, no peer-reviewed; útil para patrones ontológicos BFO/IOF pero requiere validación; cubre condiciones de cultivo como cualidades de sistemas biológicos         |
| D05    | Media      | Alta      | Alta         | Media              | Media                 | Artículo ASME 2024 / NIST, peer-reviewed, con DOI verificable; cubre modelado ontológico de operación de biorreactor fed-batch pero no lista propiedades generales directamente       |
| D06    | Media      | Media     | Media        | Media              | Media                 | Preprint arXiv 2025; propone ontología de fermentación de precisión con conceptos de calidad, rol y unidad compatibles con el alcance; requiere validación                            |
| D07    | Media      | Alta      | Alta         | Media              | Media                 | Documento técnico NIST (2023); ilustra explícitamente un biorreactor con sensores/actuadores/control de parámetros en marco BFO/IOF Core                                              |
| D09    | Alta       | Media     | Alta         | Alta               | Alta                  | GFI (2025), institución de investigación con fuentes citadas; clasifica parámetros de biorreactor en físicos, químicos y biológicos/bioquímicos con definiciones claras               |

---

## 6. Corpus documental seleccionado

| ID doc | Documento seleccionado                                                         | Pregunta asociada | Fragmentos o páginas relevantes                                                                                     | Estado   |
| ------ | ------------------------------------------------------------------------------ | ----------------- | ------------------------------------------------------------------------------------------------------------------- | -------- |
| D01    | BioLector XT Technical Specifications — m2p-labs/Beckman Coulter (2021)        | ALC-06            | Secciones: Cultivation Conditions, Oxygen Optodes, pH Optodes, Microfluidic Features, Microtiter Plates (volúmenes) | Incluido |
| D02    | BIOSTAT® Bplus Exclusive Flow Specifications — Sartorius Stedim Biotech (2023) | ALC-06            | Secciones: Measurement Ranges, Culture Vessel, Temperature System, Agitation System, Gassing System, Pumps          | Incluido |
| D03    | Bioreactor – an overview — ScienceDirect Topics (vigente)                      | ALC-06            | Párrafos sobre parámetros mantenidos: flujos de gas, temperatura, pH, DO, agitación; clasificación de biorreactores | Incluido |
| D09    | Deep Dive: Fermentation Upstream Bioprocess Design — GFI (2025)                | ALC-06            | Clasificación de parámetros en físicos, químicos y biológicos/bioquímicos                                           | Incluido |

Los documentos D04, D05, D06 y D07 se retienen como **referencias ontológicas auxiliares** (Uncertain) para la sección de triadas y relaciones, pero no se usan como fuente primaria de las propiedades generales.

---

## 7. Respuesta basada en evidencia

Sobre la base del corpus documental seleccionado, las propiedades generales que deben describir cualquier biorreactor del proyecto —con independencia de su escala o volumen— se organizan en las siguientes categorías:

### 7.1 Propiedades de identificación y clasificación

**Evidencia explícita** (D01, D02): Todo biorreactor posee un **nombre/modelo** (ej. BioLector XT, BIOSTAT® Bplus), una **entidad fabricante** (m2p-labs/Beckman Coulter, Sartorius Stedim), una **escala de operación** (micro, laboratorio) y un **formato de cultivo** (plato microtiter 48 pozos, vaso de vidrio borosilicato de pared simple).

**Evidencia explícita** (D03): Los biorreactores se clasifican según **modo de operación** (batch, fed-batch, continuo/quimiostato) y según **tipo de agitación** (agitado, perfusión, estático).

### 7.2 Propiedades de volumen

**Evidencia explícita** (D01): El BioLector XT opera con un **volumen de llenado (filling volume)** de 800–1.900 µL (FlowerPlate) o 1.000–2.400 µL (Round Well Plate), dependiente de la velocidad de agitación.

**Evidencia explícita** (D02): El BIOSTAT® Bplus define para cada tamaño de vaso un **volumen de trabajo (working volume)** y un **volumen total (total volume)**. Para el vaso de 5 L: working volume 0,6–5 L, total volume 6,6 L. Para el de 10 L: working volume 1,5–10 L, total volume 13 L.

**Inferencia razonable**: El **volumen de trabajo** y el **volumen total** son propiedades que todo biorreactor del proyecto debe exponer, con unidades homologadas (µL o L según escala).

### 7.3 Variables operativas monitoreadas y controladas

**Evidencia explícita** (D01, D02, D03, D09): Las propiedades operativas comunes son:

| Propiedad                 | BioLector XT (D01)                          | Sartorius Bplus (D02)                                                        | Clasificación (D09) |
| ------------------------- | ------------------------------------------- | ---------------------------------------------------------------------------- | ------------------- |
| Temperatura               | 10–50 °C                                    | 0–150 °C (rango medición); 8 °C sobre agua de enfriamiento a 60 °C (control) | Física              |
| pH                        | 4,0–7,5 (optodo óptico)                     | 2–12 (electrodo de gel)                                                      | Química             |
| Oxígeno disuelto (DO/pO₂) | 0–100 % sat. O₂ (optodo)                    | 0–100 % (electrodo polarográfico)                                            | Química             |
| Velocidad de agitación    | 100–1.500 rpm (3 mm diámetro)               | 20–2.000 rpm (1 L/2 L); 20–1.500 rpm (5 L); 20–800 rpm (10 L)                | Física              |
| Flujo de gas / aireación  | O₂ 1–100 %, CO₂ 0–12 % (módulos opcionales) | Aire, O₂, N₂, CO₂ (sparger y overlay)                                        | Física/Química      |

**Evidencia explícita** (D02): Propiedades adicionales presentes en el Sartorius: **nivel de espuma (foam)**, **nivel de líquido (level)**, **Redox** (opcional), **turbidez** (opcional).

**Evidencia explícita** (D03): Las propiedades monitoreadas incluyen "flow rates of gas (air, oxygen, nitrogen, carbon dioxide), temperature, pH and dissolved oxygen levels, and agitation speed/circulation rate."

**Inferencia razonable**: Aunque el BioLector XT no tiene sensores de espuma ni de nivel (por su formato de plato microtiter), el conjunto mínimo común a todo biorreactor del proyecto es: temperatura, pH, DO y velocidad de agitación/mezcla.

### 7.4 Propiedades del sistema de sensores

**Evidencia explícita** (D01): El BioLector XT utiliza **sensores ópticos pre-calibrados** (optodos) para DO y pH, medición sin contacto de biomasa por dispersión de luz.

**Evidencia explícita** (D02): El BIOSTAT® Bplus utiliza sensores **electroquímicos**: electrodo polarográfico para pO₂, electrodo de gel para pH, sonda Pt100 para temperatura, sensores de espuma y nivel; optcionalmente redox y turbidez.

**Inferencia razonable**: El tipo de sensor (óptico vs. electroquímico) es una propiedad diferenciadora que debe representarse en la ontología como atributo de cada instrumento de medición.

### 7.5 Propiedades del sistema de control

**Evidencia explícita** (D02): El controlador del BIOSTAT® Bplus gestiona lazos de control digital para temperatura, pH, DO (en cascada), agitación, mezcla de gases, flujo total de sparger/overlay y substrato.

**Evidencia explícita** (D01): El BioLector XT permite **control de pH en lazo cerrado** mediante microvalvas (módulo microfluidico opcional), con control PI configurable y estrategias de alimentación (constante, lineal, exponencial, pulso).

**Evidencia explícita** (D03): "Reactors can provide an output to specified process parameter control elements to rectify any deviation in the value of these parameters from the user-defined set point."

### 7.6 Modo de operación del cultivo

**Evidencia explícita** (D02, D09): Todo biorreactor del proyecto debe describir su **modo de operación**: batch, fed-batch, continuo o perfusión.

**Evidencia explícita** (D02): Posibles modos en BIOSTAT® Bplus: "batch, fed batch and continuous or perfusion mode."

**Evidencia explícita** (D01): El BioLector XT admite "batch, fed-batch, bolus, continuous" como estrategias de alimentación.

### 7.7 Propiedades de esterilización y materiales

**Evidencia explícita** (D02): El BIOSTAT® Bplus usa materiales en partes en contacto con el producto: vidrio borosilicato, acero inoxidable AISI 316L, EPDM.

**Evidencia explícita** (D01): El BioLector XT usa placas microtiter desechables, gamma-esterilizadas, de uso único.

**Inferencia razonable**: El concepto de **esterilidad** y el **tipo de vaso/recipiente** (reutilizable vs. desechable, single-use vs. multi-use) son propiedades generales relevantes para todo biorreactor del proyecto.

### 7.8 Propiedades de conectividad e integración

**Evidencia explícita** (D01): El BioLector XT soporta integración con sistemas robóticos de manejo de líquidos (RoboLector), interface Ethernet para comunicación con PC.

**Evidencia explícita** (D02): El BIOSTAT® Bplus dispone de "Host communication: Ethernet | RS422 | RS232" y software BioPAT® MFCS/DA para adquisición de datos y supervisión SCADA.

### 7.9 Información no establecida en el corpus

- El corpus no proporciona un listado canónico y unificado de propiedades mínimas obligatorias para una definición ontológica de clase `Bioreactor` en el contexto específico del proyecto.
- No se encontró documentación específica sobre el modelo exacto "Sartorius 5 L" o "Sartorius 10 L" con ese nombre comercial exacto; los datos fueron obtenidos del BIOSTAT® Bplus que existe en configuraciones de 5 L y 10 L.
- No se ha verificado si existen SOPs institucionales propios del laboratorio del proyecto que adicionen propiedades contextuales.

---

## 8. Tabla de afirmaciones y evidencia

| ID ev | Afirmación                                                                                                                                      | Tipo      | Documento     | Página/sección                                                                                                        | Fragmento o resumen fiel                                                                                                                                                          | Confianza | Validación experta |
| ----- | ----------------------------------------------------------------------------------------------------------------------------------------------- | --------- | ------------- | --------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------- | ------------------ |
| EV-01 | Todo biorreactor posee un nombre de modelo, fabricante y año de manufactura como propiedades de identificación                                  | Explícita | D01, D02      | Encabezado de fichas técnicas                                                                                         | Fichas identifican "BioLector XT", "m2p-labs/Beckman Coulter", ©2021; y "BIOSTAT® Bplus", "Sartorius Stedim"                                                                      | Alta      | No requerida       |
| EV-02 | El volumen de trabajo es una propiedad numérica fundamental de todo biorreactor                                                                 | Explícita | D01, D02      | D01: sección Microtiter Plates; D02: sección Culture Vessel                                                           | D01: "Filling volume: 800–1900 μL (rpm dependent)"; D02: "Working volume: 0.6–5 / 1.5–10 [L]"                                                                                     | Alta      | No requerida       |
| EV-03 | La temperatura es una propiedad operativa medida y controlada en todo biorreactor                                                               | Explícita | D01, D02, D03 | D01: Cultivation Conditions; D02: Measurement Ranges; D03: descripción general                                        | D01: "10–50 °C"; D02: "Temperature: 0–150°C [medición]"; D03: parámetro de mantenimiento obligatorio                                                                              | Alta      | No requerida       |
| EV-04 | El pH es una variable medida y controlada en todo biorreactor del proyecto                                                                      | Explícita | D01, D02, D03 | D01: pH Optodes / Microfluidic Features; D02: Measurement Ranges; D03: parámetros                                     | D01: "pH 4–7.5 (depending on plate)"; D02: "pH 2–12"                                                                                                                              | Alta      | No requerida       |
| EV-05 | El oxígeno disuelto (DO/pO₂) es propiedad medida en todo biorreactor del proyecto                                                               | Explícita | D01, D02, D03 | D01: Oxygen Optodes; D02: Measurement Ranges                                                                          | D01: "0–100 % dissolved oxygen"; D02: "pO2: 0–100 %"                                                                                                                              | Alta      | No requerida       |
| EV-06 | La velocidad de agitación/mezcla es propiedad operativa de todo biorreactor del proyecto                                                        | Explícita | D01, D02, D03 | D01: Cultivation Conditions; D02: Agitation System / Measurement Ranges                                               | D01: "100–1500 rpm (3 mm diameter)"; D02: "20–800 rpm" a "20–2000 rpm" según vaso                                                                                                 | Alta      | No requerida       |
| EV-07 | La composición del gas de entrada (O₂, CO₂, N₂, aire) es propiedad operable de todo biorreactor                                                 | Explícita | D01, D02      | D01: Environmental Conditions y módulos opcionales; D02: Gassing System                                               | D01: "1–100 % O₂ (optional); 0–12 % CO₂ (optional)"; D02: "Gas mixing of Air, O₂, N₂, CO₂"                                                                                        | Alta      | No requerida       |
| EV-08 | El modo de operación del cultivo (batch, fed-batch, continuo, perfusión) es propiedad clasificatoria de todo biorreactor                        | Explícita | D01, D02, D09 | D02: Applicability; D01: Feeding options; D09: clasificación de sistemas                                              | D02: "Batch, fed batch and continuous or perfusion mode"; D01: "batch, fed-batch, bolus, continuous"                                                                              | Alta      | No requerida       |
| EV-09 | Los biorreactores se clasifican como de tecnología desechable (single-use) o reutilizable (multi-use)                                           | Explícita | D01, D02      | D01: Application mode; D02: Design                                                                                    | D01: "Application mode: Disposable technology"; D02: "Multi-Use Bioreactors... Design: Single wall glass vessel"                                                                  | Alta      | No requerida       |
| EV-10 | Los parámetros operativos se agrupan en físicos (temperatura, agitación, presión) y químicos (pH, DO, concentraciones de gas)                   | Explícita | D09           | Sección de clasificación de parámetros                                                                                | GFI agrupa en "physical, such as temperature, vessel pressure, agitation rate" y "chemical, such as pH, nutrient concentration, and gas concentration like dissolved oxygen (DO)" | Alta      | No requerida       |
| EV-11 | El tipo de sensor (óptico vs. electroquímico) es una propiedad diferenciadora de los sistemas de medición en biorreactores                      | Inferida  | D01, D02      | D01: "online, pre-calibrated optical sensors (optodes)"; D02: "Polarographic [pO₂], Gel-filled [pH], Pt100 [Temp]"    | Ambos documentos describen sensores de forma explícita pero la categorización como "propiedad diferenciadora" es inferida del análisis comparativo                                | Media     | Recomendada        |
| EV-12 | El sistema de control de lazo cerrado (set-point, cascada) es una propiedad de los subsistemas de control de biorreactores                      | Explícita | D02, D01      | D02: "Integrated digital control loops for Temperature, pH, DO"; D01: "Triggered pH control (closed loop controller)" | Ambos documentos describen sistemas de control con set-points y lazos automáticos                                                                                                 | Alta      | No requerida       |
| EV-13 | El protocolo de comunicación (Ethernet, RS232, RS422) es una propiedad de conectividad de los biorreactores del proyecto                        | Explícita | D01, D02      | D01: "Interface: Ethernet"; D02: "Host communication: Ethernet RS422"                                                                                                                                                                             |    | Alta               | No requerida |
| EV-14 | La presión del vaso de cultivo es una propiedad técnica de biorreactores con vasos cerrados                                                     | Explícita | D02           | Culture Vessel y Utilities                                                                                            | D02: "Gasses: Controlled @ 1.5 barg dry, particle and oil-free"; D02 referencia presión de diseño del vaso                                                                        | Alta      | No requerida       |
| EV-15 | El control de espuma y nivel de líquido son propiedades presentes en biorreactores de mayor escala pero ausentes en microbiorreactores de plato | Inferida  | D01, D02      | D02: "Foam & Level amplifiers"; D01: sin mención de sensores de espuma ni nivel                                       | Ausencia documentada en D01 vs. presencia explícita en D02                                                                                                                        | Media     | Recomendada        |

---

## 9. Conceptos ontológicos candidatos

| Concepto candidato        | Tipo sugerido                              | Definición basada en evidencia                                                                                                                        | Fuente asociada | Estado    |
| ------------------------- | ------------------------------------------ | ----------------------------------------------------------------------------------------------------------------------------------------------------- | --------------- | --------- |
| `Bioreactor`              | Clase                                      | Sistema controlado que contiene y gestiona un cultivo biológico, dotado de propiedades de volumen, temperatura, pH, DO, agitación y modo de operación | D01, D02, D03   | Candidato |
| `WorkingVolume`           | Propiedad de dato (xsd:float)              | Volumen efectivo de medio de cultivo dentro del vaso o pozo del biorreactor, expresado en µL o L                                                      | D01, D02        | Candidato |
| `TotalVolume`             | Propiedad de dato (xsd:float)              | Volumen total del vaso de cultivo incluyendo espacio de cabeza, expresado en L                                                                        | D02             | Candidato |
| `TemperatureSetPoint`     | Propiedad de dato (xsd:float)              | Valor de consigna de temperatura en grados Celsius establecido para el proceso                                                                        | D01, D02        | Candidato |
| `TemperatureRange`        | Clase o Propiedad estructurada             | Rango operativo de temperatura (mínimo y máximo) del biorreactor en condiciones normales                                                              | D01, D02        | Candidato |
| `pHSetPoint`              | Propiedad de dato (xsd:float)              | Valor de consigna de pH para el proceso de cultivo                                                                                                    | D01, D02        | Candidato |
| `DissolvedOxygenSetPoint` | Propiedad de dato (xsd:float)              | Porcentaje de saturación de oxígeno disuelto como valor de consigna del proceso                                                                       | D01, D02        | Candidato |
| `AgitationSpeed`          | Propiedad de dato (xsd:float, unidad: rpm) | Velocidad de agitación del sistema de mezcla del biorreactor                                                                                          | D01, D02        | Candidato |
| `OperationMode`           | Propiedad de objeto o Individuo            | Modo de operación del cultivo: batch, fed-batch, continuo, perfusión, bolus                                                                           | D01, D02, D09   | Candidato |
| `GasComposition`          | Clase                                      | Descripción de la composición del gas de entrada (porcentajes de O₂, CO₂, N₂, aire)                                                                   | D01, D02        | Candidato |
| `VesselType`              | Propiedad de dato (xsd:string)             | Tipo de recipiente de cultivo: plato microtiter, vaso de vidrio, bolsa single-use                                                                     | D01, D02        | Candidato |
| `DisposabilityClass`      | Propiedad de dato o Subclase               | Clasificación del vaso como desechable (single-use) o reutilizable (multi-use)                                                                        | D01, D02        | Candidato |
| `SensorSystem`            | Clase                                      | Sistema de instrumentación del biorreactor que incluye sensores de pH, DO, temperatura y otros parámetros                                             | D01, D02        | Candidato |
| `SensorType`              | Propiedad de dato (xsd:string)             | Tecnología de medición: óptica (optodo), electroquímica (polarográfica), resistiva (Pt100)                                                            | D01, D02        | Candidato |
| `ControlLoop`             | Clase                                      | Lazo de control automático asociado a un parámetro operativo (temperatura, pH, DO, agitación)                                                         | D01, D02        | Candidato |
| `ManufacturerName`        | Propiedad de dato (xsd:string)             | Nombre de la entidad fabricante del biorreactor                                                                                                       | D01, D02        | Candidato |
| `ModelName`               | Propiedad de dato (xsd:string)             | Denominación comercial del modelo del biorreactor                                                                                                     | D01, D02        | Candidato |
| `OperatingScale`          | Propiedad de dato o Individuo              | Nivel de escala del biorreactor: micro, laboratorio, piloto, producción                                                                               | D01, D02, D03   | Candidato |
| `CommunicationProtocol`   | Propiedad de dato (xsd:string)             | Protocolo de comunicación de datos del sistema: Ethernet, RS232, RS422                                                                                | D01, D02        | Candidato |
| `CultureType`             | Propiedad de dato o Individuo              | Tipo de organismo cultivado: microbiano, células de mamífero, células de insecto, levadura                                                            | D02, D09        | Candidato |

---

## 10. Relaciones ontológicas candidatas

| Relación candidata         | Dominio sugerido | Rango sugerido          | Significado                                                         | Evidencia asociada            | Estado    |
| -------------------------- | ---------------- | ----------------------- | ------------------------------------------------------------------- | ----------------------------- | --------- |
| `hasWorkingVolume`         | `Bioreactor`     | `WorkingVolume`         | Un biorreactor tiene un volumen de trabajo nominal o rango          | EV-02, D01, D02               | Candidata |
| `hasTotalVolume`           | `Bioreactor`     | `TotalVolume`           | Un biorreactor tiene un volumen total de su vaso                    | EV-02, D02                    | Candidata |
| `operatesAt`               | `Bioreactor`     | `TemperatureSetPoint`   | Un biorreactor opera a una temperatura de consigna                  | EV-03, D01, D02               | Candidata |
| `hasSensor`                | `Bioreactor`     | `SensorSystem`          | Un biorreactor está equipado con un sistema de sensores             | EV-04, EV-05, EV-11, D01, D02 | Candidata |
| `hasControlLoop`           | `Bioreactor`     | `ControlLoop`           | Un biorreactor posee lazos de control para variables operativas     | EV-12, D01, D02               | Candidata |
| `hasOperationMode`         | `Bioreactor`     | `OperationMode`         | Un biorreactor puede operar en modos batch, fed-batch, etc.         | EV-08, D01, D02               | Candidata |
| `manufacturedBy`           | `Bioreactor`     | `Manufacturer`          | Un biorreactor es fabricado por una entidad manufacturera           | EV-01, D01, D02               | Candidata |
| `hasVesselType`            | `Bioreactor`     | `VesselType`            | Un biorreactor usa un tipo específico de recipiente de cultivo      | EV-09, D01, D02               | Candidata |
| `hasDisposabilityClass`    | `Bioreactor`     | `DisposabilityClass`    | Un biorreactor se clasifica como single-use o multi-use             | EV-09, D01, D02               | Candidata |
| `hasGasComposition`        | `Bioreactor`     | `GasComposition`        | Un biorreactor recibe una mezcla de gases con composición definida  | EV-07, D01, D02               | Candidata |
| `hasOperatingScale`        | `Bioreactor`     | `OperatingScale`        | Un biorreactor se clasifica en una escala de operación              | EV-01, D01, D02, D03          | Candidata |
| `hasCommunicationProtocol` | `Bioreactor`     | `CommunicationProtocol` | Un biorreactor se conecta a sistemas externos mediante un protocolo | EV-13, D01, D02               | Candidata |
| `measuresParameter`        | `SensorSystem`   | `OperativeParameter`    | Un sistema de sensores mide un parámetro operativo                  | EV-04, EV-05, EV-06, D01, D02 | Candidata |
| `controlsParameter`        | `ControlLoop`    | `OperativeParameter`    | Un lazo de control regula un parámetro operativo con set-point      | EV-12, D01, D02               | Candidata |

---

## 11. Triadas RDF candidatas

```
# Propiedades de identificación
BioLectorXT -> rdf:type -> Bioreactor
BioLectorXT -> hasManufacturerName -> "m2p-labs / Beckman Coulter"
BioLectorXT -> hasModelName -> "BioLector XT"
SartoriusBplus5L -> rdf:type -> Bioreactor
SartoriusBplus5L -> hasManufacturerName -> "Sartorius Stedim Biotech"
SartoriusBplus10L -> rdf:type -> Bioreactor

# Propiedades de volumen
BioLectorXT -> hasWorkingVolume -> "800–1900 µL (FlowerPlate, rpm-dependent)"
SartoriusBplus5L -> hasWorkingVolume -> "0.6–5 L"
SartoriusBplus5L -> hasTotalVolume -> "6.6 L"
SartoriusBplus10L -> hasWorkingVolume -> "1.5–10 L"
SartoriusBplus10L -> hasTotalVolume -> "13 L"

# Temperatura
BioLectorXT -> hasTemperatureRange -> TemperatureRange_10_50C
SartoriusBplus5L -> hasTemperatureControlRange -> TemperatureRange_8CAboveColingWaterTo60C

# pH
BioLectorXT -> hasMeasurementRange_pH -> "4.0–7.5"
SartoriusBplus5L -> hasMeasurementRange_pH -> "2–12"

# Oxígeno disuelto
BioLectorXT -> hasMeasurementRange_DO -> "0–100% O2 saturation"
SartoriusBplus5L -> hasMeasurementRange_DO -> "0–100%"

# Agitación
BioLectorXT -> hasAgitationSpeedRange -> "100–1500 rpm"
SartoriusBplus5L -> hasAgitationSpeedRange -> "20–1500 rpm"
SartoriusBplus10L -> hasAgitationSpeedRange -> "20–800 rpm"

# Tipo de sensor
BioLectorXT -> hasSensorType -> OpticalSensor
SartoriusBplus5L -> hasSensorType_pO2 -> PolarographicElectrode
SartoriusBplus5L -> hasSensorType_pH -> GelFilledElectrode
SartoriusBplus5L -> hasSensorType_Temp -> Pt100Probe

# Modo de operación
BioLectorXT -> hasOperationMode -> BatchMode
BioLectorXT -> hasOperationMode -> FedBatchMode
BioLectorXT -> hasOperationMode -> ContinuousMode
SartoriusBplus5L -> hasOperationMode -> BatchMode
SartoriusBplus5L -> hasOperationMode -> FedBatchMode
SartoriusBplus5L -> hasOperationMode -> ContinuousMode
SartoriusBplus5L -> hasOperationMode -> PerfusionMode

# Tipo de vaso / desechabilidad
BioLectorXT -> hasVesselType -> MicrotiterPlate
BioLectorXT -> hasDisposabilityClass -> SingleUse
SartoriusBplus5L -> hasVesselType -> GlassVessel
SartoriusBplus5L -> hasDisposabilityClass -> MultiUse

# Composición de gas
BioLectorXT -> hasGasComposition -> GasComp_O2_1_100pct
BioLectorXT -> hasGasComposition -> GasComp_CO2_0_12pct
SartoriusBplus5L -> hasGasComposition -> GasMix_Air_O2_N2_CO2

# Escala operativa
BioLectorXT -> hasOperatingScale -> MicroScale
SartoriusBplus5L -> hasOperatingScale -> LabScale
SartoriusBplus10L -> hasOperatingScale -> LabScale

# Conectividad
BioLectorXT -> hasCommunicationProtocol -> "Ethernet"
SartoriusBplus5L -> hasCommunicationProtocol -> "Ethernet"
SartoriusBplus5L -> hasCommunicationProtocol -> "RS422"
SartoriusBplus5L -> hasCommunicationProtocol -> "RS232"

# Control en lazo cerrado
BioLectorXT -> hasControlLoop -> ClosedLoopController_pH
SartoriusBplus5L -> hasControlLoop -> ClosedLoopController_Temperature
SartoriusBplus5L -> hasControlLoop -> ClosedLoopController_pH
SartoriusBplus5L -> hasControlLoop -> ClosedLoopController_DO
```

**Estado de triadas:**

| Grupo                               | Estado                                             |
| ----------------------------------- | -------------------------------------------------- |
| Identificación (modelo, fabricante) | Soportada — D01, D02                               |
| Volúmenes (working, total)          | Soportada — D01, D02                               |
| Temperatura                         | Soportada — D01, D02                               |
| pH                                  | Soportada — D01, D02                               |
| DO/pO₂                              | Soportada — D01, D02                               |
| Agitación                           | Soportada — D01, D02                               |
| Tipo de sensor                      | Soportada — D01, D02                               |
| Modo de operación                   | Soportada — D01, D02                               |
| Tipo de vaso / desechabilidad       | Soportada — D01, D02                               |
| Composición de gas                  | Soportada — D01, D02                               |
| Escala operativa                    | Parcialmente soportada — inferida de D01, D02, D03 |
| Comunicación                        | Soportada — D01, D02                               |
| Lazos de control                    | Soportada — D01, D02                               |

---

## 12. Sinónimos y variantes terminológicas

| Término principal     | Sinónimos o variantes documentadas                                   | Idioma | Documento de soporte                               |
| --------------------- | -------------------------------------------------------------------- | ------ | -------------------------------------------------- |
| Working volume        | Filling volume, volumen de llenado, volumen útil, volumen nominal    | EN/ES  | D01 (filling volume), D02 (working volume)         |
| Dissolved oxygen (DO) | pO₂, Oxygen saturation, oxígeno disuelto                             | EN/ES  | D01 (DO), D02 (pO2)                                |
| Agitation speed       | Stirring speed, shaking speed, stirrer speed, velocidad de agitación | EN/ES  | D01 (shaking speed), D02 (agitation/stirrer speed) |
| Operation mode        | Culture mode, process mode, modo de cultivo                          | EN/ES  | D01, D02                                           |
| Single-use            | Disposable, desechable                                               | EN/ES  | D01 (disposable technology)                        |
| Multi-use             | Reusable, reutilizable                                               | EN/ES  | D02 (multi-use bioreactors)                        |
| Optical sensor        | Optode, fluorescence sensor, pre-calibrated optical sensor           | EN     | D01                                                |
| Gas composition       | Gas mixture, gassing profile, mezcla de gases                        | EN/ES  | D01, D02                                           |
| Set point             | Consigna, valor de referencia, setpoint                              | EN/ES  | D01, D02                                           |
| Control loop          | Control cascade, lazo de control, closed loop controller             | EN/ES  | D01, D02                                           |
| Manufacturer          | Fabricante, maker, vendor                                            | EN/ES  | D01, D02                                           |
| Sensor system         | Instrumentation, probes, sensores, measurement system                | EN/ES  | D01, D02                                           |

---

## 13. Vacíos, riesgos y decisiones pendientes

**Información faltante:**

- No se localizó documentación técnica específica con la denominación exacta "Sartorius 5 L" o "Sartorius 10 L" como nombres propios del proyecto; se usó el BIOSTAT® Bplus, que corresponde funcionalmente. Se requiere confirmación del investigador sobre el modelo exacto instalado.
- No se obtuvo información sobre SOPs o protocolos institucionales propios del laboratorio que puedan definir propiedades adicionales o restricciones específicas.
- La presión interna del vaso de cultivo aparece implícitamente en D02 pero no se presenta como variable monitorizada online; se requiere validación.
- Propiedades como biomasa en línea (medida por dispersión de luz en BioLector XT) no tienen equivalente directo en el Sartorius → podría ser una propiedad específica de escala, no general.

**Ambigüedades terminológicas:**

- "Filling volume" (D01) vs. "Working volume" (D02): aunque ambos se refieren al volumen operativo, los criterios de determinación son distintos (uno depende de rpm, el otro de diseño del vaso). Requiere decisión de modelado.
- "Scale" puede referirse a escala de volumen (µL, L, m³) o a escala de proceso (laboratorio, piloto, producción). Se recomienda separar en dos propiedades distintas.

**Configuraciones dependientes del equipo:**

- Los módulos opcionales del BioLector XT (O₂, CO₂, anaerobiosis, microfluidica) definen propiedades que existen solo si están instalados; esto debe modelarse como restricciones de cardinalidad opcionales (0..1) en OWL.
- Los sensores de espuma y nivel están presentes en Sartorius pero ausentes en BioLector XT: propiedad opcional o restringida a subclase `BenchTopBioreactor`.

**Datos que requieren validación con expertos:**

- Confirmación del modelo Sartorius exacto (BIOSTAT® Bplus, B-DCU u otro).
- Validación de que `OperatingScale` (micro, laboratorio) sea una propiedad de la clase abstracta o deba asignarse solo a individuos.
- Confirmación de si `CommunicationProtocol` debe modelarse como propiedad del `Bioreactor` o de su `ControlSystem`.
- Definición de si la biomasa en línea (BioLector XT) debe ser una propiedad medida general o específica de microbiorreactores de plato.

**Documentos adicionales necesarios:**

- Manual de usuario o manual de operación del BioLector XT (Beckman Coulter/m2p-labs) para verificar propiedades de medición adicionales.
- Ficha de datos o manual del modelo Sartorius exacto (BIOSTAT® B, B-DCU, Bplus) confirmado por el laboratorio.
- SOP institucional de operación de biorreactores del proyecto (si existe).
- Ontología OBO/MCBO o PREFER para alineación formal de conceptos como `quality`, `role`, `process` en BFO.

---

## 14. Registro metodológico para el documento de investigación

La pregunta ALC-06 indaga sobre el conjunto mínimo e invariante de propiedades generales que debe describir cualquier biorreactor del proyecto —BioLector XT, Sartorius 5 L y Sartorius 10 L— con independencia de su escala o formato tecnológico. La estrategia de búsqueda incluyó consultas en bases de datos técnicas y científicas (ScienceDirect, bioRxiv, NIST Publications, arXiv), así como en sitios oficiales de fabricantes (m2p-labs/Beckman Coulter, Sartorius Stedim Biotech), con términos en inglés y español centrados en especificaciones técnicas de biorreactores, parámetros operativos y ontologías de bioprocesos. Los criterios de selección priorizaron fichas técnicas oficiales verificables, revisiones técnicas con autoridad reconocida y publicaciones científicas con trazabilidad de autoría y fecha. El corpus quedó conformado por cuatro documentos: la hoja de especificaciones técnicas del BioLector XT (m2p-labs/Beckman Coulter, 2021), la hoja de especificaciones del BIOSTAT® Bplus (Sartorius Stedim, 2023), la revisión técnica de biorreactores de ScienceDirect Topics y el análisis de diseño de bioprocesos del Good Food Institute (2025). La evidencia extraída permitió identificar trece categorías de propiedades generales: identificación y clasificación del sistema, volumen de trabajo y volumen total, temperatura, pH, oxígeno disuelto, velocidad de agitación, composición del gas de entrada, modo de operación del cultivo, tipo y desechabilidad del vaso, sistema de sensores y tipo de tecnología sensorial, lazos de control y set-points, escala operativa y protocolo de comunicación. Los conceptos ontológicos candidatos comprenden veinte términos, entre clases, propiedades de dato y propiedades de objeto, articulados en una clase abstracta `Bioreactor` de la cual todos los sistemas del proyecto serían individuos o subclases. Las limitaciones principales incluyen la falta de confirmación del modelo Sartorius exacto instalado en el laboratorio, la ausencia de SOPs institucionales y la ambigüedad entre "filling volume" y "working volume" que requiere decisión de modelado. La validación experta es recomendada para propiedades como escala operativa, protocolo de comunicación y medición de biomasa en línea.

---

## 15. Estado final

| Dimensión                      | Estado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| ------------------------------ | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Nivel de confianza general** | Alto                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| **Estado de la respuesta**     | Soportada                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| **Estado del corpus**          | Suficiente para propiedades fundamentales; Parcial para contexto institucional específico                                                                                                                                                                                                                                                                                                                                                                                               |
| **Próxima acción recomendada** | (1) Confirmar con el investigador el modelo Sartorius exacto instalado. (2) Solicitar SOP institucional si existe. (3) Validar con experto de dominio la separación entre propiedades generales de la clase abstracta `Bioreactor` y propiedades específicas de cada individuo/subclase. (4) Alinear los conceptos candidatos con BFO/IOF Core y OBO Foundry antes de formalizar en OWL. (5) Continuar con preguntas ALC subsiguientes para definir propiedades específicas por escala. |
