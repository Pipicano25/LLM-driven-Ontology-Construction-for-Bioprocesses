# Análisis de pregunta ALC-01

## Ontología OWL/RDF para sistemas BioLector XT, Sartorius 5 L y Sartorius 10 L

---

## 1. Identificación de la pregunta

| Campo                  | Contenido                                                                                                        |
| ---------------------- | ---------------------------------------------------------------------------------------------------------------- |
| **ID**                 | ALC-01                                                                                                           |
| **Nivel metodológico** | Fundacional / Alcance ontológico                                                                                 |
| **Tema**               | Definición de biorreactor en el contexto del proyecto multiescala                                                |
| **Pregunta**           | ¿Qué se entiende por biorreactor dentro del proyecto, considerando BioLector XT, Sartorius 5 L y Sartorius 10 L? |

---

## 2. Propósito de la pregunta

Esta pregunta tiene carácter fundacional: busca establecer el alcance conceptual del término _biorreactor_ dentro del proyecto, identificando qué sistemas físicos quedan incluidos, bajo qué criterios y en qué nivel de abstracción ontológica deben representarse. Su respuesta determina la clase raíz desde la cual se derivan las subclases del dominio (microbiorreactor, biorreactor de tanque agitado a escala de laboratorio), y permite definir las propiedades estructurales mínimas que todo individuo de la clase `Bioreactor` debe poseer: un volumen de trabajo, una escala de operación, un principio de mezcla, capacidad de monitoreo de parámetros de cultivo y un modo de operación. Para el corpus, esta pregunta justifica la incorporación de manuales de fabricante, artículos científicos comparativos multiescala y ontologías de bioprocesos ya existentes.

---

## 3. Plan de búsqueda documental

**Información técnica requerida:**

- Definición técnica y funcional de biorreactor en ingeniería de bioprocesos.
- Especificaciones del BioLector XT (fabricante, escala, principio de operación, sensores).
- Especificaciones del Biostat® B de Sartorius en configuraciones 5 L y 10 L (volumen de trabajo, sensores, principio de mezcla).
- Ontologías existentes de bioprocesos que modelen biorreactores (clases, propiedades, individuos).
- Artículos científicos que comparen escalas micro y de laboratorio usando estos equipos u otros equivalentes.

**Tipos de documentos necesarios:**

- Fichas técnicas y páginas de producto del fabricante (Beckman Coulter, Sartorius).
- Manuales o notas de aplicación oficiales.
- Artículos científicos revisados por pares (comparación de escalas, biodesarrollo).
- Preprints de ontologías de bioprocesos (MCBO, etc.).
- Recursos académicos consolidados de ingeniería de bioprocesos.

**Repositorios y sitios sugeridos:**

- `beckman.com` — producto BioLector XT
- `sartorius.com` — producto Biostat® B
- PubMed / PMC — artículos de bioprocesos
- bioRxiv — ontologías de bioprocesos recientes
- ScienceDirect Topics — revisiones temáticas
- Nature Scientific Reports

**Términos de búsqueda (español / inglés):**

- biorreactor definición / bioreactor definition bioprocess engineering
- BioLector XT especificaciones microbiorreactor / BioLector XT specifications Beckman Coulter
- Sartorius Biostat B 5L 10L biorreactor volumen de trabajo / working volume stirred tank
- ontología biorreactor OWL / bioreactor OWL ontology
- comparación microbiorreactor tanque agitado escala / microbioreactor stirred tank scale comparison

**Ecuaciones de búsqueda sugeridas:**

```
("BioLector XT") AND ("specifications" OR "technical data")
("Sartorius" OR "Biostat B") AND ("5L" OR "10L") AND ("working volume" OR "bioreactor")
("bioreactor" AND "OWL ontology" AND "bioprocess")
("microbioreactor" AND "stirred tank" AND "scale-up" AND "BioLector")
("MCBO" OR "bioprocessing ontology") AND ("bioreactor")
```

**Criterios de inclusión aplicables:** Documentos de fabricante oficial, artículos peer-reviewed (2010–2026) que mencionen alguno de los tres sistemas o sus equivalentes funcionales, ontologías de bioprocesos publicadas.

**Criterios de exclusión aplicables:** Blogs sin referencias, contenido de resellers de segunda mano sin especificaciones verificadas, documentos sin fecha ni autoría.

---

## 4. Documentos candidatos encontrados

| ID doc | Título                                                                                                              | Entidad autora                                   |   Año | Tipo de fuente                                                   | URL/DOI verificable                                                                                         | Relación con la pregunta                                                                                       | Decisión preliminar |
| ------ | ------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------ | ----: | ---------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------- | ------------------- |
| DOC-01 | BioLector XT Microbioreactor — Product Page                                                                         | Beckman Coulter Life Sciences                    | 2021+ | Página oficial de fabricante                                     | `https://www.beckman.com/microbioreactor/biolector-xt`                                                      | Directa: describe el BioLector XT como sistema, sensores, formato MTP                                          | Include             |
| DOC-02 | Next-Generation BioLector XT Microbioreactor — Press Release                                                        | Beckman Coulter Life Sciences / m2p-labs         |  2021 | Comunicado oficial de fabricante                                 | `https://www.beckman.com/news/next-generation-biolector-xt-microbioreactor`                                 | Directa: lanzamiento del producto, descripción funcional                                                       | Include             |
| DOC-03 | BioLector XT Technical Data Sheet                                                                                   | Beckman Coulter Life Sciences                    | 2021+ | Ficha técnica oficial                                            | `https://www.beckman.com/resources/reading-material/product-instructions/biolector-xt-technical-data-sheet` | Directa: especificaciones técnicas formales (página accesible, contenido descargable)                          | Uncertain           |
| DOC-04 | Biostat® B — Benchtop Bioreactor Controller                                                                         | Sartorius AG                                     | 2022+ | Página oficial de fabricante                                     | `https://www.sartorius.com/en/products/fermentation-bioreactors/benchtop-bioreactors/biostat-b`             | Directa: describe el sistema Biostat B incluyendo versiones 5 L y 10 L                                         | Include             |
| DOC-05 | Bioreactor Sartorius 10 (w/MFCS) — BIOSTAT B (A\*SEF)                                                               | A\*STAR / Sartorius Stedim                       |   s/f | Base de datos de equipos institucional verificable               | `https://asef.a-star.edu.sg/equipment/bioreactor-sartorius-10-w-mfcs-biostat-b-sifbi`                       | Directa: especificaciones técnicas verificables para 5 L y 10 L                                                | Include             |
| DOC-06 | Benchtop Bioreactors — Overview Page                                                                                | Sartorius AG                                     | 2023+ | Página oficial de fabricante                                     | `https://www.sartorius.com/en/products/fermentation-bioreactors/benchtop-bioreactors`                       | Directa: define el tanque agitado de sobremesa, rango 1–10 L                                                   | Include             |
| DOC-07 | MCBO: Mammalian Cell Bioprocessing Ontology — bioRxiv preprint                                                      | Robasky, Morrissey et al. — UCSD/JHU             |  2026 | Preprint científico (bioRxiv); DOI: `10.64898/2026.01.05.697007` | `https://www.biorxiv.org/content/10.64898/2026.01.05.697007v1`                                              | Indirecta-alta: ontología OWL de bioprocesos que modela biorreactor y condiciones de cultivo                   | Include             |
| DOC-08 | High-throughput microbioreactor provides a capable tool for early stage bioprocess development — Scientific Reports | Jäger et al.                                     |  2021 | Artículo científico peer-reviewed; DOI via Nature                | `https://www.nature.com/articles/s41598-021-81633-6`                                                        | Directa: usa BioLector y lo compara con STR, define escalas                                                    | Include             |
| DOC-09 | Scale-up from microtiter plate to laboratory fermenter — PMC                                                        | Kensy et al.                                     |  2009 | Artículo científico peer-reviewed (PMC)                          | `https://www.ncbi.nlm.nih.gov/pmc/articles/PMC2806293/`                                                     | Indirecta-alta: evalúa escalabilidad MTP (BioLector) vs STF; define escala micro                               | Uncertain           |
| DOC-10 | Bioprocess Engineering (ScienceDirect Topics)                                                                       | ScienceDirect / Elsevier (compilación académica) | 2023+ | Recurso académico consolidado                                    | `https://www.sciencedirect.com/topics/engineering/bioprocess-engineering`                                   | Indirecta: define biorreactor en contexto farmacéutico como dispositivo técnico de cultivo aséptico controlado | Include             |
| DOC-11 | Biostat® B Brochure — The Multi-Talented Bioreactor                                                                 | Sartorius AG                                     | 2020+ | Brochure oficial descargable                                     | `https://www.sartorius.com/download/700722/biostat-b-brochure-en-b-sbi1513-sartorius-pdf-data.pdf`          | Directa: características del Biostat B como biorreactor de I+D                                                 | Uncertain           |

---

## 5. Evaluación de documentos candidatos

| ID doc | Relevancia | Autoridad  | Trazabilidad | Cobertura de la pregunta | Evidencia localizable | Justificación                                                                                                                                                                                     |
| ------ | ---------- | ---------- | ------------ | ------------------------ | --------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| DOC-01 | Alta       | Alta       | Alta         | Alta                     | Alta                  | Página oficial del fabricante; describe características principales del BioLector XT como microbiorreactor de alto rendimiento; incluye sensores, formato MTP, aplicaciones                       |
| DOC-02 | Alta       | Alta       | Alta         | Alta                     | Alta                  | Comunicado de prensa oficial de Beckman Coulter (2021); define BioLector XT como sucesor de Pro, describe principio de operación y capacidades analíticas                                         |
| DOC-03 | Alta       | Alta       | Alta         | Alta                     | Baja                  | La URL es verificable y la página existe, pero el contenido descargable (PDF de datos técnicos) no pudo ser extraído en esta sesión; requiere descarga directa por el investigador                |
| DOC-04 | Alta       | Alta       | Alta         | Alta                     | Alta                  | Página oficial Sartorius; describe Biostat B como controlador universal de sobremesa para recipientes de 1–10 L; incluye modos de operación                                                       |
| DOC-05 | Alta       | Media-Alta | Alta         | Alta                     | Alta                  | Base de datos institucional A\*STAR (Singapur); referencia Biostat B con especificaciones exactas de 5 L y 10 L (velocidad de agitación, volumen de trabajo, sensores, gases)                     |
| DOC-06 | Alta       | Alta       | Alta         | Alta                     | Alta                  | Página de categoría Sartorius; incluye definición técnica del STR de sobremesa y rango de volúmenes 1–10 L                                                                                        |
| DOC-07 | Alta       | Alta       | Alta         | Media-Alta               | Alta                  | Preprint con DOI verificable; modela biorreactor (CellCultureSystem) en OWL/BFO; no específico para BioLector XT o Biostat B, pero directamente aplicable a la estructura ontológica del proyecto |
| DOC-08 | Alta       | Alta       | Alta         | Alta                     | Alta                  | Nature Scientific Reports, peer-reviewed; evalúa BioLector como plataforma HTP y lo contrasta con STR; proporciona contexto de comparación de escalas                                             |
| DOC-09 | Media-Alta | Alta       | Alta         | Media                    | Alta                  | PMC, peer-reviewed; evalúa la escala MTP original de BioLector vs STF; útil para contexto histórico y equivalencias de escala, aunque usa versión anterior del BioLector                          |
| DOC-10 | Media      | Media      | Media        | Media                    | Alta                  | Compilación de Elsevier de capítulos académicos; define biorreactor como dispositivo técnico de cultivo aséptico controlado en bioprocesos farmacéuticos                                          |
| DOC-11 | Alta       | Alta       | Alta         | Alta                     | Baja                  | Brochure oficial Sartorius en PDF; URL es verificable pero el contenido no pudo ser extraído directamente; requiere descarga por el investigador                                                  |

---

## 6. Corpus documental seleccionado

| ID doc | Documento seleccionado                                              | Pregunta asociada | Fragmentos o páginas relevantes                                                                                  | Estado                          |
| ------ | ------------------------------------------------------------------- | ----------------- | ---------------------------------------------------------------------------------------------------------------- | ------------------------------- |
| DOC-01 | BioLector XT Microbioreactor — Beckman Coulter (página de producto) | ALC-01            | Sección "Features", descripción del sistema, parámetros medidos en línea                                         | Incluido — accesible            |
| DOC-02 | Press Release BioLector XT — Beckman Coulter, mayo 2021             | ALC-01            | Párrafos descriptivos del principio de operación, FlowerPlate, sucesión del BioLector Pro                        | Incluido — accesible            |
| DOC-04 | Biostat® B — Sartorius (página de producto oficial)                 | ALC-01            | Sección de descripción, modos de proceso, tipos de recipiente, control DCU                                       | Incluido — accesible            |
| DOC-05 | BIOSTAT B — A\*STAR Equipment Finder                                | ALC-01            | Tabla de especificaciones técnicas: volumen de trabajo 5 L y 10 L, velocidades de agitación, gases, sensores     | Incluido — accesible            |
| DOC-06 | Benchtop Bioreactors Overview — Sartorius                           | ALC-01            | Definición de tanque agitado de sobremesa, rango de volúmenes, descripción física del STR                        | Incluido — accesible            |
| DOC-07 | MCBO — Robasky et al., bioRxiv 2026                                 | ALC-01            | Sección de modelado OWL de CellCultureSystem y biorreactor; patrón BFO                                           | Incluido — accesible (preprint) |
| DOC-08 | Jäger et al. 2021, Scientific Reports                               | ALC-01            | Sección de comparación BioLector vs STR; descripción del BioLector como µ-biorreactor de alto rendimiento        | Incluido — accesible            |
| DOC-10 | ScienceDirect Topics — Bioprocess Engineering                       | ALC-01            | Definición de biorreactor como dispositivo técnico para cultivo aséptico controlado en bioprocesos farmacéuticos | Incluido — accesible (parcial)  |

> **Nota:** DOC-03 (Technical Data Sheet) y DOC-11 (brochure PDF) se identifican como muy relevantes pero no fue posible extraer su contenido en esta sesión. **Se recomienda que el investigador los descargue directamente** desde las URLs indicadas y los incorpore al corpus en la siguiente iteración.

---

## 7. Respuesta basada en evidencia

### Definición de biorreactor en el contexto del proyecto

Dentro del proyecto, el término **biorreactor** engloba sistemas físicos de distinta escala y principio de operación que comparten la función esencial de proporcionar condiciones controladas para el cultivo de microorganismos, células u otros organismos, con monitoreo en línea de parámetros críticos del proceso.

#### 7.1 BioLector XT — Microbiorreactor de alto rendimiento (escala micro)

**Evidencia explícita:** El BioLector XT es un microbiorreactor de alto rendimiento basado en el formato estándar ANSI/SLAS (SBS) de placa de microtitulación (MTP), que opera con sensores ópticos en línea precalibrados. Las MTPs desechables de 48 pocillos permiten la medición en línea de parámetros de cultivo, mientras que la tecnología microfluídica patentada permite el control simultáneo del pH y la alimentación.

El BioLector XT fue lanzado por m2p-labs (Baesweiler, Alemania), parte de la Unidad de Negocio de Biotecnología de Beckman Coulter Life Sciences desde noviembre de 2020. Está equipado con la tecnología patentada de placa FlowerPlate de microtitulación y permite cribados de alto rendimiento de cepas, monitoreo de parámetros de cultivo y optimización de estrategias de alimentación.

El BioLector XT permite la evaluación en tiempo real de biomasa, fluorescencia, pH, oxígeno disuelto en fase líquida (OD) y otros parámetros clave de cultivo para microorganismos aerobios, anaerobios y fototróficos. Permite el gaseo con O₂ en un rango del 1% al 100% y con CO₂ entre 1% y 12%.

**Inferencia razonable:** El BioLector XT opera a escala de microsistema (pocillos individuales de la FlowerPlate), lo que lo distingue cualitativamente de un biorreactor de tanque agitado convencional. No obstante, cumple la función de un biorreactor al proveer condiciones de cultivo controladas y monitoreo continuo en línea. La escala exacta de volumen de trabajo por pocillo no pudo ser confirmada desde la ficha técnica oficial (DOC-03, no descargable en esta sesión) y **requiere validación con el investigador o descarga del TDS oficial**.

#### 7.2 Sartorius Biostat® B 5 L y 10 L — Biorreactor de tanque agitado de sobremesa (escala de laboratorio)

**Evidencia explícita:** El tanque agitado de sobremesa consiste en un recipiente con una relación de dimensiones de altura definida. La mezcla se logra mediante un elemento agitador central dentro del recipiente de cultivo. Hay múltiples puertos en la placa de cabeza con diferentes funcionalidades como inserción de sondas, adición de sustratos, inserción de gas y extracción de muestras. Son biorreactores de pequeña escala con volúmenes de 1 a 10 L, utilizados frecuentemente en laboratorios de investigación, disponibles con recipientes de vidrio de uso múltiple autoclavables o recipientes de un solo uso.

El Biostat B de Sartorius Stedim es un fermentador/biorreactor específicamente diseñado para los requisitos de optimización y caracterización de procesos. Sus especificaciones técnicas incluyen: volumen de trabajo de 5 L (0,6–5 L) y de 10 L (1,5–10 L); velocidad de agitación permitida de 5 L (20–1500 rpm) y 10 L (20–800 rpm); flujo de gas: aire, O₂, CO₂, N₂ (caudal total máximo 20 lpm); sensores de pH, pO₂, temperatura, espuma, nivel, sustrato.

El Biostat® B es el controlador universal de sobremesa para sistemas de agitación y movimiento de balanceo. La torre de control multipropósito permite configuración simple o doble, con una gama de cámaras de cultivo: recipientes clásicos de vidrio en tanque agitado, recipientes de un solo uso en tanque agitado, bolsas Flexsafe RM con mezcla por balanceo.

#### 7.3 Síntesis: concepto de biorreactor en el proyecto

En el proyecto, el concepto de **biorreactor** se define como un **sistema técnico diseñado para el cultivo controlado de organismos biológicos**, que:

- Contiene un volumen de trabajo definido (desde escala micro hasta escala de laboratorio).
- Provee control activo de variables operativas críticas (temperatura, pH, oxígeno disuelto, agitación, gasificación).
- Dispone de sensores e instrumentos para el monitoreo en línea de parámetros de cultivo.
- Puede operar en diferentes modos de proceso (batch, fed-batch, continuo).
- Es susceptible de comparación entre escalas para actividades de scale-up o scale-down.

En los bioprocesos farmacéuticos, los biorreactores son dispositivos técnicos para el cultivo aséptico controlado de células y la fabricación del producto. Son un elemento central que asigna los parámetros de cultivo y permite un control de proceso riguroso y, por ende, procesos y productos altamente reproducibles.

La diferencia fundamental entre los tres sistemas del proyecto es **de escala y principio de operación**: el BioLector XT es un microbiorreactor de formato de placa de microtitulación con mezcla por agitación orbital, mientras que los Biostat® B 5 L y 10 L son tanques agitados con impulsor central y control clásico de proceso. Los tres comparten la función de ser plataformas de cultivo controlado con monitoreo en línea.

#### 7.4 Información no establecida en el corpus actual

- El volumen de trabajo exacto por pocillo del BioLector XT (en µL o mL) no pudo ser confirmado desde una fuente primaria en esta sesión.
- La configuración específica de sensores instalada en los equipos del laboratorio del proyecto (que puede diferir de las especificaciones nominales del fabricante) requiere validación con experto.
- No se encontró documentación que defina formalmente "biorreactor" en el sentido normativo (ISO/ANSI) aplicado a estos sistemas específicos.

---

## 8. Tabla de afirmaciones y evidencia

| ID evidencia | Afirmación                                                                                                                                                                                         | Tipo de evidencia | Documento              | Página/sección                                   | Fragmento o resumen fiel                                                                                                                                                            | Confianza | Validación experta                                    |
| ------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------- | ---------------------- | ------------------------------------------------ | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------- | ----------------------------------------------------- |
| EV-01        | El BioLector XT es un microbiorreactor de alto rendimiento basado en formato MTP de 48 pocillos con sensores ópticos en línea precalibrados                                                        | Explícita         | DOC-01, DOC-02         | Descripción principal del producto               | BioLector XT basado en ANSI/SLAS MTP, sensores ópticos en línea, 48 pocillos desechables                                                                                            | Alta      | No requerida                                          |
| EV-02        | El BioLector XT permite medición en línea de biomasa, fluorescencia, pH y OD para organismos aerobios, anaerobios y fototróficos                                                                   | Explícita         | DOC-01, DOC-04         | Sección Features / descripción de producto       | Evaluación en tiempo real de biomasa, fluorescencia, pH, OD para aerobes, anaerobes y organismos fototróficos                                                                       | Alta      | No requerida                                          |
| EV-03        | El BioLector XT fue desarrollado por m2p-labs (Baesweiler, Alemania), integrado a Beckman Coulter Life Sciences en noviembre de 2020                                                               | Explícita         | DOC-02                 | Párrafo de lanzamiento del producto              | m2p-labs parte de Beckman Coulter Life Sciences' Biotechnology Business Unit desde noviembre de 2020                                                                                | Alta      | No requerida                                          |
| EV-04        | El BioLector XT sucede al BioLector Pro y utiliza tecnología patentada FlowerPlate                                                                                                                 | Explícita         | DOC-02                 | Comunicado de prensa, 25 mayo 2021               | El BioLector XT sucede al BioLector Pro; equipado con tecnología de placa FlowerPlate de microtitulación patentada                                                                  | Alta      | No requerida                                          |
| EV-05        | El Biostat® B de Sartorius opera con recipientes de vidrio de 5 L (volumen de trabajo 0,6–5 L) y 10 L (volumen de trabajo 1,5–10 L)                                                                | Explícita         | DOC-05                 | Tabla de especificaciones técnicas               | Working volume: 5 L (0,6–5 L); 10 L (1,5–10 L)                                                                                                                                      | Alta      | Recomendada (confirmar con manual del equipo)         |
| EV-06        | El Biostat® B 5 L opera a 20–1500 rpm y el 10 L a 20–800 rpm                                                                                                                                       | Explícita         | DOC-05                 | Tabla de especificaciones técnicas               | Permitted stirring speed: 5L (20–1500rpm); 10L (20–800rpm)                                                                                                                          | Alta      | Recomendada                                           |
| EV-07        | El Biostat® B dispone de sensores de pH, pO₂, temperatura, espuma, nivel, sustrato, gas, agitación, presión de recipiente, redox y turbidez                                                        | Explícita         | DOC-05                 | Tabla de sensores                                | Sensors: pH, pO2, Temperature, Foam, Level, Substrate addition, Gas mixing, Agitation, Gravimetric Feed & Harvest Control, Vessel pressure, Redox & Turbidity                       | Alta      | Recomendada (confirmar configuración del laboratorio) |
| EV-08        | El Biostat® B soporta procesos en batch, fed-batch, continuo y perfusión                                                                                                                           | Explícita         | DOC-04                 | Sección de estrategias de proceso                | Permite configurar Biostat® B con control de alimentación gravimétrica, control de nivel gravimétrico o perfiles de adición de sustrato para batch, fed-batch, continuo o perfusión | Alta      | No requerida                                          |
| EV-09        | Los tanques agitados de sobremesa de Sartorius son biorreactores de pequeña escala con volúmenes de 1 a 10 L, usados en laboratorios de investigación                                              | Explícita         | DOC-06                 | Descripción de la categoría benchtop bioreactors | Son biorreactores de pequeña escala con volúmenes de 1 a 10 L, disponibles con recipientes de vidrio autoclavables o de un solo uso                                                 | Alta      | No requerida                                          |
| EV-10        | En bioprocesos farmacéuticos, los biorreactores son dispositivos técnicos para el cultivo aséptico controlado de células y la manufactura del producto                                             | Explícita         | DOC-10                 | ScienceDirect Topics / Bioprocess Engineering    | Bioreactors are technical devices for the controlled aseptic culture of cells and manufacturing of the product                                                                      | Alta      | No requerida                                          |
| EV-11        | El BioLector opera con platos de 48 pocillos; en comparación con STR, es adecuado como plataforma de cribado en desarrollo temprano de procesos                                                    | Explícita         | DOC-08                 | Abstract y sección de materiales                 | El BioLector µ-biorreactor fue seleccionado como plataforma de cultivo de alto rendimiento para cribado de clones productores de proteínas recombinantes                            | Alta      | No requerida                                          |
| EV-12        | El BioLector XT constituye funcionalmente un biorreactor aunque opera a escala micro; comparte con el STR la función de control y monitoreo en línea de parámetros de cultivo                      | Inferida          | DOC-01, DOC-08, DOC-06 | Múltiples secciones                              | Inferido de la comparación funcional entre ambas plataformas de cultivo controlado con monitoreo en línea                                                                           | Media     | Requerida                                             |
| EV-13        | En la ontología MCBO, las condiciones ambientales de cultivo se modelan como cualidades del sistema material CellCultureSystem (en el que participa el biorreactor), conforme a los principios BFO | Explícita         | DOC-07                 | Figura 1 y texto principal del preprint          | Culture environmental conditions are modeled as qualities of the material cell culture system, consistent with BFO principles                                                       | Alta      | Recomendada (es preprint, no peer-reviewed)           |
| EV-14        | El volumen de trabajo exacto por pocillo del BioLector XT no fue recuperable desde fuente primaria en esta sesión                                                                                  | No establecida    | DOC-03                 | Technical Data Sheet (no descargable)            | El TDS existe en la URL oficial pero su contenido no pudo ser extraído                                                                                                              | Baja      | Requerida — descarga directa del TDS                  |

---

## 9. Conceptos ontológicos candidatos

| Concepto candidato      | Tipo sugerido                         | Definición basada en evidencia                                                                                                                                                    | Fuente asociada        | Estado                                                                           |
| ----------------------- | ------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------- | -------------------------------------------------------------------------------- |
| `Bioreactor`            | Clase                                 | Sistema técnico diseñado para el cultivo controlado y monitoreado de organismos biológicos bajo condiciones definidas de temperatura, pH, OD y agitación, a cualquier escala      | DOC-06, DOC-10, DOC-04 | Candidato — requiere validación                                                  |
| `Microbioreactor`       | Subclase de `Bioreactor`              | Biorreactor de alta densidad de cultivo paralelo basado en formato de placa de microtitulación, que opera a escala micro con sensores ópticos en línea y tecnología microfluídica | DOC-01, DOC-02, DOC-08 | Candidato — requiere validación                                                  |
| `StirredTankBioreactor` | Subclase de `Bioreactor`              | Biorreactor con mezcla lograda por un elemento agitador central dentro del recipiente de cultivo, disponible en recipientes de vidrio reutilizable o de un solo uso               | DOC-06, DOC-04, DOC-05 | Candidato — requiere validación                                                  |
| `BenchtopBioreactor`    | Subclase de `StirredTankBioreactor`   | Tanque agitado de pequeña escala (1–10 L) diseñado para uso en laboratorio de investigación y desarrollo, con control de proceso comparable a equipos de mayor escala             | DOC-06                 | Candidato — requiere validación                                                  |
| `BioLectorXT`           | Individuo de `Microbioreactor`        | Sistema específico fabricado por m2p-labs/Beckman Coulter; basado en MTP de 48 pocillos ANSI/SLAS; con sensores ópticos de biomasa, pH, OD, fluorescencia; tecnología FlowerPlate | DOC-01, DOC-02         | Candidato — requiere validación                                                  |
| `SartoriusBiostatB5L`   | Individuo de `BenchtopBioreactor`     | Configuración del Biostat® B de Sartorius con recipiente Univessel® Glass de 5 L; volumen de trabajo 0,6–5 L; agitación 20–1500 rpm                                               | DOC-04, DOC-05         | Candidato — requiere validación                                                  |
| `SartoriusBiostatB10L`  | Individuo de `BenchtopBioreactor`     | Configuración del Biostat® B de Sartorius con recipiente Univessel® Glass de 10 L; volumen de trabajo 1,5–10 L; agitación 20–800 rpm                                              | DOC-04, DOC-05         | Candidato — requiere validación                                                  |
| `OperatingVolume`       | Propiedad de dato                     | Volumen de trabajo efectivo del biorreactor en condiciones operativas; expresado en µL, mL o L según la escala                                                                    | DOC-05, DOC-06         | Candidato — requiere validación                                                  |
| `OperationScale`        | Propiedad de dato o Concepto auxiliar | Clasificación del biorreactor según el orden de magnitud del volumen de trabajo: micro (<10 mL), laboratorio (1–10 L), piloto (>10 L)                                             | DOC-06, DOC-08         | Candidato — requiere validación                                                  |
| `MixingPrinciple`       | Propiedad de dato                     | Mecanismo de mezcla del biorreactor: agitación orbital (MTP), agitador central con impulsor, mecánico magnético, etc.                                                             | DOC-06, DOC-01         | Candidato — requiere validación                                                  |
| `CellCultureSystem`     | Clase (referenciada de MCBO)          | Sistema material que incluye el biorreactor, el medio de cultivo y las células; sus cualidades representan las condiciones ambientales del cultivo                                | DOC-07                 | Candidato — referenciado de ontología externa; requiere validación de alineación |

---

## 10. Relaciones ontológicas candidatas

| Relación candidata           | Dominio sugerido                              | Rango sugerido                       | Significado                                                                                                                                | Evidencia asociada  | Estado                                                |
| ---------------------------- | --------------------------------------------- | ------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------ | ------------------- | ----------------------------------------------------- |
| `isA` / `rdfs:subClassOf`    | `Microbioreactor`                             | `Bioreactor`                         | El microbiorreactor es un tipo de biorreactor                                                                                              | EV-01, EV-12        | Candidato                                             |
| `isA` / `rdfs:subClassOf`    | `StirredTankBioreactor`                       | `Bioreactor`                         | El tanque agitado es un tipo de biorreactor                                                                                                | EV-09               | Candidato                                             |
| `isA` / `rdfs:subClassOf`    | `BenchtopBioreactor`                          | `StirredTankBioreactor`              | El biorreactor de sobremesa es un tanque agitado a escala laboratorio                                                                      | EV-09               | Candidato                                             |
| `hasWorkingVolume`           | `Bioreactor`                                  | `OperatingVolume`                    | El biorreactor tiene un volumen de trabajo definido                                                                                        | EV-05               | Candidato                                             |
| `operatesAtScale`            | `Bioreactor`                                  | `OperationScale`                     | El biorreactor opera a una escala definida                                                                                                 | EV-05, EV-09, EV-12 | Candidato                                             |
| `hasMixingPrinciple`         | `Bioreactor`                                  | `MixingPrinciple`                    | El biorreactor utiliza un principio de mezcla particular                                                                                   | EV-09, EV-01        | Candidato                                             |
| `hasOnlineSensor`            | `Bioreactor`                                  | `Sensor`                             | El biorreactor dispone de sensores de monitoreo en línea                                                                                   | EV-02, EV-07        | Candidato                                             |
| `participatesIn`             | `Bioreactor`                                  | `CellCultureProcess`                 | El biorreactor participa en un proceso de cultivo celular o microbiano                                                                     | DOC-07 (MCBO)       | Candidato                                             |
| `manufacturedBy`             | `BioLectorXT`                                 | `BeckmanCoulterLifeSciences`         | El BioLector XT es fabricado por Beckman Coulter                                                                                           | EV-03               | Candidato                                             |
| `manufacturedBy`             | `SartoriusBiostatB5L`, `SartoriusBiostatB10L` | `Sartorius`                          | Los Biostat B son fabricados por Sartorius                                                                                                 | DOC-04, DOC-05      | Candidato                                             |
| `isFunctionallyEquivalentTo` | `BioLectorXT`                                 | `StirredTankBioreactor` (en función) | El BioLector XT cumple funciones equivalentes a un STR para screening y monitoreo en línea, aunque difiere en principio de mezcla y escala | EV-12               | Candidato — requiere validación experta especialmente |

---

## 11. Triadas RDF candidatas

```
# Jerarquía de clases
Microbioreactor -> rdfs:subClassOf -> Bioreactor
[Soportada | DOC-01, DOC-08 | Sección principal de descripción]

StirredTankBioreactor -> rdfs:subClassOf -> Bioreactor
[Soportada | DOC-06 | Definición de tanque agitado de sobremesa]

BenchtopBioreactor -> rdfs:subClassOf -> StirredTankBioreactor
[Soportada | DOC-06 | Descripción de biorreactores de sobremesa 1–10 L]

# Individuos
BioLectorXT -> rdf:type -> Microbioreactor
[Soportada | DOC-01, DOC-02 | Descripción del sistema]

SartoriusBiostatB5L -> rdf:type -> BenchtopBioreactor
[Soportada | DOC-04, DOC-05 | Especificaciones técnicas]

SartoriusBiostatB10L -> rdf:type -> BenchtopBioreactor
[Soportada | DOC-04, DOC-05 | Especificaciones técnicas]

# Volúmenes de trabajo (Sartorius)
SartoriusBiostatB5L -> hasWorkingVolume -> "0.6–5 L"^^xsd:string
[Soportada | DOC-05 | Tabla de especificaciones técnicas]

SartoriusBiostatB10L -> hasWorkingVolume -> "1.5–10 L"^^xsd:string
[Soportada | DOC-05 | Tabla de especificaciones técnicas]

# Volumen de trabajo BioLector XT
BioLectorXT -> hasWorkingVolume -> [VALOR NO ESTABLECIDO]
[Requiere validación experta | DOC-03 no descargable en esta sesión]

# Principio de mezcla
BioLectorXT -> hasMixingPrinciple -> "OrbitalShaking_MicrotiterPlate"
[Parcialmente soportada | DOC-01, DOC-02 | Inferido de formato MTP/FlowerPlate]

SartoriusBiostatB5L -> hasMixingPrinciple -> "CentralImpellerAgitation"
[Soportada | DOC-06 | Definición de tanque agitado]

SartoriusBiostatB10L -> hasMixingPrinciple -> "CentralImpellerAgitation"
[Soportada | DOC-06 | Definición de tanque agitado]

# Escala de operación
BioLectorXT -> operatesAtScale -> "MicroScale"
[Soportada | DOC-08 | Descripción como µ-bioreactor HTP]

SartoriusBiostatB5L -> operatesAtScale -> "LaboratoryScale"
[Soportada | DOC-06 | Descripción como biorreactor de sobremesa]

SartoriusBiostatB10L -> operatesAtScale -> "LaboratoryScale"
[Soportada | DOC-06 | Descripción como biorreactor de sobremesa]

# Fabricantes
BioLectorXT -> manufacturedBy -> BeckmanCoulterLifeSciences
[Soportada | DOC-02 | Comunicado oficial 2021]

SartoriusBiostatB5L -> manufacturedBy -> Sartorius
[Soportada | DOC-04 | Página oficial Sartorius]

SartoriusBiostatB10L -> manufacturedBy -> Sartorius
[Soportada | DOC-04 | Página oficial Sartorius]

# Sensores (Sartorius, confirmados)
SartoriusBiostatB5L -> hasOnlineSensor -> pHSensor
[Soportada | DOC-05 | Tabla de sensores]

SartoriusBiostatB5L -> hasOnlineSensor -> DissolvedOxygenSensor
[Soportada | DOC-05 | Tabla de sensores]

SartoriusBiostatB5L -> hasOnlineSensor -> TemperatureSensor
[Soportada | DOC-05 | Tabla de sensores]

# Sensores (BioLector XT, confirmados)
BioLectorXT -> hasOnlineSensor -> BiomassSensor_Optical
[Soportada | DOC-01 | Descripción del sistema]

BioLectorXT -> hasOnlineSensor -> pHSensor_Optical
[Soportada | DOC-01 | Descripción del sistema]

BioLectorXT -> hasOnlineSensor -> DissolvedOxygenSensor_Optical
[Soportada | DOC-01 | Descripción del sistema]

BioLectorXT -> hasOnlineSensor -> FluorescenceSensor
[Soportada | DOC-01, DOC-02 | Descripción del sistema]

# Equivalencia funcional (clase de escala)
BioLectorXT -> isFunctionallyEquivalentTo -> StirredTankBioreactor
[Parcialmente soportada | DOC-08, DOC-12 | Comparten función de monitoreo en línea; difieren en escala y mezcla — requiere validación experta]

# Modos de proceso Sartorius
SartoriusBiostatB5L -> supportsOperationMode -> BatchProcess
[Soportada | DOC-04 | Sección de estrategias de proceso]

SartoriusBiostatB5L -> supportsOperationMode -> FedBatchProcess
[Soportada | DOC-04 | Sección de estrategias de proceso]

SartoriusBiostatB5L -> supportsOperationMode -> ContinuousProcess
[Soportada | DOC-04 | Sección de estrategias de proceso]

# Modelado MCBO (referencia externa)
Bioreactor -> participatesIn -> CellCultureProcess
[Soportada | DOC-07 | Patrón BFO/IOF del MCBO — preprint, requiere cita adecuada]
```

---

## 12. Sinónimos y variantes terminológicas

| Término principal         | Sinónimos o variantes documentadas                                                          | Idioma       | Documento de soporte   |
| ------------------------- | ------------------------------------------------------------------------------------------- | ------------ | ---------------------- |
| `Bioreactor`              | fermenter, fermentador, cultivation vessel, culture vessel, bioreaktor                      | EN / ES / DE | DOC-04, DOC-05, DOC-06 |
| `Microbioreactor`         | µ-bioreactor, micro-bioreactor, microbioreactor system, high-throughput bioreactor          | EN           | DOC-01, DOC-08         |
| `StirredTankBioreactor`   | STR, stirred tank fermenter (STF), tanque agitado, reactor de tanque agitado                | EN / ES      | DOC-06, DOC-08, DOC-17 |
| `BenchtopBioreactor`      | laboratory bioreactor, lab-scale bioreactor, benchtop fermenter, biorreactor de laboratorio | EN / ES      | DOC-06                 |
| `BioLector XT`            | BioLector XT Microbioreactor, M2P-G-BLXT, BioLector Pro (predecesor)                        | EN           | DOC-01, DOC-02         |
| `Sartorius Biostat B 5L`  | BIOSTAT B 5L, Biostat B + Univessel Glass 5L, Sartorius 5L                                  | EN / ES      | DOC-04, DOC-05         |
| `Sartorius Biostat B 10L` | BIOSTAT B 10L, Biostat B + Univessel Glass 10L, Sartorius 10L                               | EN / ES      | DOC-04, DOC-05         |
| `OperatingVolume`         | working volume, volumen de trabajo, volumen útil, culture volume                            | EN / ES      | DOC-05, DOC-06         |
| `DissolvedOxygen`         | DO, OD (oxígeno disuelto), pO₂                                                              | EN / ES      | DOC-01, DOC-05         |
| `MicrotiterPlate`         | MTP, microtiter plate, placa de microtitulación, FlowerPlate, SBS plate, ANSI/SLAS plate    | EN / ES      | DOC-01, DOC-02         |

---

## 13. Vacíos, riesgos y decisiones pendientes

**Información faltante:**

1. **Volumen de trabajo por pocillo del BioLector XT.** El Technical Data Sheet oficial (DOC-03) existe en la URL de Beckman Coulter pero su contenido detallado no pudo ser extraído en esta sesión. Este dato es crítico para completar la triada `BioLectorXT → hasWorkingVolume → [valor]`. _Acción requerida: el investigador debe descargar el TDS directamente._
2. **Configuración específica de sensores en los equipos del laboratorio.** La configuración estándar descrita en DOC-05 puede diferir de la instalación concreta en el laboratorio del proyecto (módulos opcionales, sensores adicionales como redox, turbidez, CO₂ en línea).
3. **Manual técnico completo del Biostat® B.** El brochure PDF de Sartorius (DOC-11) no pudo ser leído en esta sesión. Puede contener tablas de especificaciones más completas, incluyendo dimensiones de recipientes, geometría del impulsor y coeficientes de transferencia de masa.

**Ambigüedades terminológicas:**

- El término "fermenter/fermentador" se usa como sinónimo de "biorreactor" en documentación de Sartorius (DOC-05 lo llama "fermenter | bioreactor"), pero en bioprocesos modernos existe una distinción entre fermentación microbiana y cultivo de células de mamífero. Para la ontología, se debe decidir si `Fermenter` es sinónimo o subclase específica de `Bioreactor`.
- El término "microbiorreactor" en el contexto del BioLector XT hace referencia a un instrumento de escala micro basado en placa, no a un biorreactor miniaturizado convencional. Esta diferencia de principio de operación debe representarse en la ontología.

**Configuraciones dependientes del equipo:**

- El Biostat® B puede operar con una variedad de recipientes (Univessel® Glass 1/2/5/10 L; Univessel® SU 2 y 10 L; bolsas Flexsafe RM). La pregunta ALC-01 refiere a las versiones 5 L y 10 L pero no especifica si son de vidrio reutilizable o de un solo uso — esto afecta las propiedades de la clase o individuo ontológico.

**Datos que requieren validación con expertos:**

- La relación `isFunctionallyEquivalentTo` entre BioLectorXT y StirredTankBioreactor: aunque ambos comparten función de monitoreo en línea, difieren en principio de mezcla, escala, arquitectura de control y capacidad de transferencia de oxígeno (kLa). Declarar equivalencia funcional requiere acuerdo del dominio.
- Los modos de proceso soportados por el BioLector XT (batch/fed-batch con microfluidics) deben ser confirmados con el investigador en cuanto a cuáles se emplean efectivamente en el proyecto.

**Documentos adicionales necesarios:**

- Manual de operación del BioLector XT (descargable desde el área de clientes de Beckman Coulter — requiere registro).
- Manual del Biostat® B de Sartorius (disponible en sartorius.com con registro).
- Protocolos internos del laboratorio (SOPs) que definan operativamente cada sistema.
- Artículo de Kensy et al. (DOC-09, PMC2806293) debería ser revisado más detenidamente para extraer parámetros de escala del BioLector original que puedan orientar las especificaciones del XT.

---

## 14. Registro metodológico para el documento de investigación

La pregunta ALC-01 buscó establecer el concepto fundacional de biorreactor aplicable al proyecto de construcción de una ontología OWL/RDF para los sistemas BioLector XT (Beckman Coulter/m2p-labs), Sartorius Biostat® B 5 L y Sartorius Biostat® B 10 L. La estrategia de búsqueda combinó consultas a fuentes primarias de fabricante en los sitios oficiales de Beckman Coulter (`beckman.com`) y Sartorius (`sartorius.com`), rastreo de bases de datos de equipamiento institucional verificable (A*STAR), búsqueda de artículos científicos revisados por pares en PubMed/PMC y Nature, y recuperación de ontologías de bioprocesos recientes en bioRxiv. Los criterios de inclusión priorizaron documentos con autoría institucional verificable, fecha y evidencia técnica extraíble; los de exclusión eliminaron contenido de revendedores sin especificaciones trazables. El corpus seleccionado comprende ocho documentos: la página de producto oficial y el comunicado de lanzamiento del BioLector XT (Beckman Coulter, 2021), la página de producto y la categoría de biorreactores de sobremesa de Sartorius, la base de datos A*STAR con especificaciones del Biostat® B, el preprint MCBO (Robasky et al., bioRxiv 2026, DOI 10.64898/2026.01.05.697007), un artículo de Scientific Reports (Jäger et al., 2021) sobre BioLector como plataforma HTP, y una revisión consolidada de ScienceDirect sobre ingeniería de bioprocesos. La evidencia extraída permitió definir el biorreactor como dispositivo técnico de cultivo controlado aséptico con monitoreo en línea, identificar el BioLector XT como microbiorreactor de escala micro basado en formato de 48 pocillos con sensores ópticos, y caracterizar los Biostat® B 5 L y 10 L como tanques agitados de sobremesa con volúmenes de trabajo de 0,6–5 L y 1,5–10 L respectivamente. Se propusieron conceptos ontológicos candidatos (`Bioreactor`, `Microbioreactor`, `StirredTankBioreactor`, `BenchtopBioreactor`) con sus subclases e individuos, relaciones candidatas (`hasWorkingVolume`, `hasMixingPrinciple`, `hasOnlineSensor`, `operatesAtScale`) y triadas RDF soportadas. Las principales limitaciones identificadas son: la imposibilidad de extraer el Technical Data Sheet oficial del BioLector XT en esta sesión (volumen exacto por pocillo no establecido), la falta de confirmación de la configuración específica de sensores en el laboratorio del proyecto, y el carácter de preprint del MCBO. Todos los conceptos, relaciones y triadas presentados tienen estado de candidato hasta validación experta.

---

## 15. Estado final

| Dimensión                      | Estado                                                                                                                                                                                                                                                                                                                                                                                                                                                                 | Observación                                                                                                                                                                       |
| ------------------------------ | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Nivel de confianza general** | **Medio-Alto**                                                                                                                                                                                                                                                                                                                                                                                                                                                         | La evidencia es sólida para los Sartorius 5L y 10L y para la descripción funcional del BioLector XT; el volumen por pocillo del BioLector XT requiere confirmación                |
| **Estado de la respuesta**     | **Parcialmente soportada**                                                                                                                                                                                                                                                                                                                                                                                                                                             | La definición conceptual del biorreactor y las especificaciones de los Sartorius están bien soportadas; el BioLector XT carece de confirmación de volumen de trabajo específico   |
| **Estado del corpus**          | **Parcial**                                                                                                                                                                                                                                                                                                                                                                                                                                                            | Suficiente para la caracterización general y la propuesta ontológica inicial; requiere incorporación del TDS del BioLector XT y el manual del Biostat® B para completar el corpus |
| **Próxima acción recomendada** | Descargar el Technical Data Sheet del BioLector XT desde `beckman.com/resources/reading-material/product-instructions/biolector-xt-technical-data-sheet` y el manual PDF del Biostat® B desde `sartorius.com/download/700722/...`; incorporar SOPs del laboratorio del proyecto; someter los conceptos y relaciones candidatos a revisión con experto en bioprocesos para validación de la equivalencia funcional entre escalas y la configuración real de los equipos |
