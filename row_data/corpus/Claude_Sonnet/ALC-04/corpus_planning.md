# Registro Ontológico — Pregunta ALC-04

---

## 1. Identificación de la pregunta

- **ID:** ALC-04
- **Nivel metodológico:** Alcance ontológico transversal (arquitectura de clases compartidas)
- **Tema:** Componentes comunes a los tres biorreactores como base para una ontología unificada
- **Pregunta:** ¿Qué componentes comunes permiten describir estos tres biorreactores en una misma ontología?

---

## 2. Propósito de la pregunta

La pregunta busca identificar el conjunto mínimo de clases, propiedades y relaciones que son compartidas por el BioLector XT (microbiorreactor, µL), el Sartorius 5 L y el Sartorius 10 L (biorreactores de tanque agitado, L), independientemente de sus diferencias de escala o tecnología. Este conocimiento es fundacional para la ontología: define la **superclase común** `Bioreactor` y sus subcomponentes reutilizables (sensores, actuadores, recipiente, sistema de control, variables operativas), evitando redundancia y garantizando la interoperabilidad semántica entre escalas. La respuesta a esta pregunta produce el esqueleto jerárquico de la ontología OWL/RDF.

---

## 3. Plan de búsqueda documental

### Información técnica requerida

- Especificaciones de componentes físicos del BioLector XT (m2p-labs / Beckman Coulter)
- Especificaciones de componentes físicos del BIOSTAT® B 5 L y 10 L (Sartorius Stedim Biotech)
- Componentes funcionales genéricos de biorreactores según literatura científica y ontologías existentes
- Clases y propiedades de ontologías de bioprocesos (MCBO, OBI, IOF)

### Tipos de documentos necesarios

- Fichas técnicas y brochures oficiales de fabricante (Beckman Coulter, Sartorius)
- Manuales de usuario (si disponibles públicamente)
- Artículos científicos sobre taxonomía de componentes de biorreactores
- Ontologías de referencia en bioprocesos (BioPortal, GitHub)
- Notas de aplicación de los fabricantes

### Repositorios y sitios sugeridos

- `beckman.com/microbioreactor/biolector-xt`
- `sartorius.com/en/products/fermentation-bioreactors/benchtop-bioreactors/biostat-b`
- `bioportal.bioontology.org`
- `biorxiv.org` (preprints MCBO)
- `bioprocessintl.com`
- `pmc.ncbi.nlm.nih.gov`
- `cytivalifesciences.com` (recursos técnicos generales de biorreactores)

### Términos de búsqueda

| Español                                  | Inglés                                             |
| ---------------------------------------- | -------------------------------------------------- |
| componentes comunes biorreactor          | bioreactor common components                       |
| sensores biorreactor pH DO temperatura   | bioreactor sensors pH dissolved oxygen temperature |
| actuadores biorreactor agitación gaseado | bioreactor actuators agitation gassing             |
| recipiente de cultivo biorreactor        | culture vessel bioreactor                          |
| ontología bioproceso OWL RDF             | bioprocess ontology OWL RDF                        |
| especificaciones BioLector XT            | BioLector XT specifications                        |
| especificaciones Sartorius BIOSTAT B     | Sartorius BIOSTAT B specifications                 |
| escalado biorreactor componentes comunes | bioreactor scale-up common components              |

### Ecuaciones de búsqueda sugeridas

- `"BioLector XT" AND (sensor OR component OR specification)`
- `"BIOSTAT B" AND ("5L" OR "10L") AND (sensor OR component OR specification)`
- `bioreactor AND "common components" AND ontology`
- `bioprocess ontology AND (OWL OR RDF) AND bioreactor`
- `"dissolved oxygen" AND "pH" AND "temperature" AND bioreactor AND sensor`

---

## 4. Documentos candidatos encontrados

| ID doc | Título                                                                    | Entidad autora                                             | Año       | Tipo                                            | URL/DOI verificable                                                                                                             | Relación con la pregunta                                                                          | Decisión preliminar |
| ------ | ------------------------------------------------------------------------- | ---------------------------------------------------------- | --------- | ----------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------- | ------------------- |
| D01    | BioLector XT Microbioreactor – Product Page                               | Beckman Coulter Life Sciences (m2p-labs)                   | 2021–2024 | Página oficial de fabricante                    | https://www.beckman.com/microbioreactor/biolector-xt                                                                            | Describe componentes, parámetros y sensores del BioLector XT                                      | Include             |
| D02    | BioLector XT Modules – Product Page                                       | Beckman Coulter Life Sciences                              | 2021–2024 | Página oficial de fabricante                    | https://www.beckman.com/microbioreactor/biolector-xt/modules                                                                    | Lista módulos y componentes opcionales del BioLector XT                                           | Include             |
| D03    | BIOSTAT® B – Benchtop Bioreactor Controller                               | Sartorius Stedim Biotech                                   | 2021–2024 | Página oficial de fabricante                    | https://www.sartorius.com/en/products/fermentation-bioreactors/benchtop-bioreactors/biostat-b                                   | Describe componentes, sensores y actuadores del BIOSTAT B (incluye 5 L y 10 L)                    | Include             |
| D04    | Bioreactor Sartorius 10 (BIOSTAT B) – A\*SEF Equipment                    | A\*STAR / Sartorius Stedim                                 | 2022      | Ficha técnica institucional                     | https://asef.a-star.edu.sg/equipment/bioreactor-sartorius-10-w-mfcs-biostat-b-sifbi                                             | Especificaciones técnicas detalladas del BIOSTAT B para 5 L y 10 L                                | Include             |
| D05    | BIOLECTOR XT High-Throughput Bioprocess Development – Brochure            | Beckman Coulter / m2p-labs                                 | 2021      | Brochure oficial PDF                            | https://dafratec.com/storage/file/BioLector-XT-Microbioreactor-Brochure-2021.pdf                                                | Parámetros monitoreados, capacidades y componentes del BioLector XT                               | Include             |
| D06    | Anaerobic cultivation processes of probiotic bacteria in the BioLector XT | Beckman Coulter (m2p-labs)                                 | 2022–2023 | Nota de aplicación técnica                      | https://www.beckman.com/resources/reading-material/application-notes/anaerobic-cultivation-processes-biolector-xt               | Describe condiciones operativas y parámetros en uso real del BioLector XT                         | Include             |
| D07    | Parts of a stirred-tank bioreactor – Cytiva Life Sciences                 | Cytiva Life Sciences                                       | 2022–2024 | Recurso técnico/educativo de fabricante         | https://www.cytivalifesciences.com/en/us/news-center/parts-of-a-stirred-tank-bioreactor-and-their-function-10001                | Describe componentes genéricos de biorreactores de tanque agitado (aplica a Sartorius 5 L y 10 L) | Include             |
| D08    | Exploring Principles of Bioreactor Scale-Up – BioProcess International    | BioProcess International                                   | 2026-02   | Artículo técnico revisado por pares / industria | https://www.bioprocessintl.com/bioreactors/lessons-in-bioreactor-scale-up-part-1-mdash-exploring-introductory-principles        | Parámetros comunes a diferentes escalas de biorreactores                                          | Include             |
| D09    | MCBO: Mammalian Cell Bioprocessing Ontology – bioRxiv                     | Investigadores académicos (Georgia Tech / Allen Institute) | 2026-01   | Preprint revisado (bioRxiv)                     | https://www.biorxiv.org/content/10.64898/2026.01.05.697007v1.full                                                               | Ontología OWL para bioprocesos; clases y relaciones relevantes para biorreactores                 | Include             |
| D10    | Sartorius BIOSTAT B-DCU Brochure                                          | Sartorius Stedim Biotech                                   | 2021      | Brochure oficial PDF                            | https://www.sartorius.com/download/12080/broch-biostat-b-dcu-sbi1555-e-data.pdf                                                 | Sistema de gaseado y control DO en cascada del BIOSTAT B-DCU (5 L y 10 L)                         | Include             |
| D11    | Application Note: Precise Control of Gas Flows in BIOSTAT® B-DCU          | Sartorius Stedim Biotech                                   | 2021      | Nota de aplicación técnica oficial              | https://www.sartorius.com/download/12102/appl-biostat-b-dcu-sbt1025-e-data.pdf                                                  | Especificaciones del sistema de gaseado (MFC) del BIOSTAT B-DCU en recipientes de 5 L             | Include             |
| D12    | Stirred-Tank Bioreactor Scalability – BioProcess International            | BioProcess International                                   | 2024-02   | Artículo técnico/industrial revisado            | https://www.bioprocessintl.com/bioreactors/shear-proof-design-space-scaling-stirred-tank-bioreactors-for-cell-culture-processes | Parámetros independientes de escala (pH, DO, temperatura) comunes a biorreactores                 | Include             |

---

## 5. Evaluación de documentos candidatos

| ID doc | Relevancia | Autoridad                                                     | Trazabilidad                         | Cobertura de la pregunta                                                              | Evidencia localizable                      | Justificación                                                                                   |
| ------ | ---------- | ------------------------------------------------------------- | ------------------------------------ | ------------------------------------------------------------------------------------- | ------------------------------------------ | ----------------------------------------------------------------------------------------------- |
| D01    | Alta       | Alta (Beckman Coulter oficial)                                | Alta (URL directa del fabricante)    | Alta – enumera sensores, parámetros, módulos                                          | Alta – página pública con especificaciones | Fuente primaria para BioLector XT; cubre biomasa, pH, DO, fluorescencia, temperatura, agitación |
| D02    | Alta       | Alta (Beckman Coulter oficial)                                | Alta                                 | Alta – detalla módulos opcionales y componentes del sistema                           | Alta                                       | Complementa D01 con información de módulos físicos                                              |
| D03    | Alta       | Alta (Sartorius oficial)                                      | Alta (URL directa)                   | Alta – cubre BIOSTAT B en todas las escalas incluyendo 5 L y 10 L                     | Alta                                       | Fuente primaria para Sartorius; describe recipiente, gaseado, bombas, sensores                  |
| D04    | Alta       | Alta (A\*STAR, institución de investigación)                  | Alta (URL institucional verificable) | Alta – lista sensores, volúmenes de trabajo, velocidades de agitación para 5 L y 10 L | Alta                                       | Especificaciones detalladas y verificables del BIOSTAT B en 5 L y 10 L                          |
| D05    | Alta       | Alta (m2p-labs/Beckman Coulter)                               | Media (PDF alojado en distribuidor)  | Alta – resumen de componentes y parámetros del BioLector XT                           | Alta                                       | Brochure oficial con parámetros clave; requiere confirmación de fecha exacta                    |
| D06    | Alta       | Alta (Beckman Coulter, nota de aplicación oficial)            | Alta                                 | Media – cubre condiciones operativas (temperatura, rpm, DO, pH, biomasa) en uso real  | Alta                                       | Evidencia de uso real de parámetros medidos por el BioLector XT                                 |
| D07    | Alta       | Alta (Cytiva, fabricante especializado)                       | Alta                                 | Alta – enumera componentes genéricos de biorreactores de tanque agitado               | Alta                                       | Referencia técnica de fabricante para componentes comunes a STR (Sartorius 5 L y 10 L)          |
| D08    | Alta       | Alta (BioProcess International, publicación técnica revisada) | Alta                                 | Alta – parámetros comunes a diferentes escalas                                        | Alta                                       | Sustenta la posibilidad de representar múltiples escalas con variables comunes                  |
| D09    | Alta       | Alta (preprint académico, afiliaciones verificadas)           | Alta (bioRxiv DOI)                   | Alta – ontología OWL con clases para bioprocesos                                      | Alta                                       | Referente ontológico directo; define clases, subclases y propiedades relevantes                 |
| D10    | Media      | Alta (Sartorius oficial)                                      | Media (PDF en dominio Sartorius)     | Media – control DO y gaseado en cascada                                               | Alta                                       | Complementa D03 y D04 con detalles del sistema de control                                       |
| D11    | Alta       | Alta (Sartorius oficial)                                      | Media (PDF en dominio Sartorius)     | Alta – datos de MFC y gaseado en recipientes de 5 L                                   | Alta                                       | Evidencia técnica del subsistema de gaseado para 5 L                                            |
| D12    | Alta       | Alta (BioProcess International)                               | Alta                                 | Alta – parametros independientes de escala como pH, DO y temperatura                  | Alta                                       | Fundamenta teóricamente la existencia de componentes comunes entre escalas                      |

---

## 6. Corpus documental seleccionado

| ID doc | Documento seleccionado                                    | Pregunta asociada | Fragmentos/páginas relevantes                                                                                                                                            | Estado                 |
| ------ | --------------------------------------------------------- | ----------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ---------------------- |
| D01    | BioLector XT Microbioreactor – Beckman Coulter            | ALC-04            | Página principal: sensores ópticos, parámetros monitoreados (biomasa, fluorescencia, pH, DO), módulo de microfluidica, temperatura, agitación (rpm)                      | Incluido – verificable |
| D02    | BioLector XT Modules – Beckman Coulter                    | ALC-04            | Sección de módulos: control de temperatura y agitación, módulos de gaseado (O2, CO2, N2), módulo microfluidico                                                           | Incluido – verificable |
| D03    | BIOSTAT® B – Sartorius (página oficial)                   | ALC-04            | Sección especificaciones: recipiente de vidrio borosilicato (1-10 L), control de temperatura, pH, DO, agitación, gaseado con hasta 4 MFC, bombas peristálticas           | Incluido – verificable |
| D04    | Sartorius 10 – BIOSTAT B – A*STAR A*SEF                   | ALC-04            | Ficha completa: volumen de trabajo (5 L: 0.6–5 L; 10 L: 1.5–10 L), sensores (pH, pO2, temperatura, espuma, nivel, sustrato), agitación (rpm), gaseado (air, O2, CO2, N2) | Incluido – verificable |
| D06    | Anaerobic cultivation – BioLector XT (Nota de aplicación) | ALC-04            | Parámetros en uso real: temperatura 37°C, 600 rpm, biomasa (gain 3), pH (LG1), DO (RF), volumen de inicio 2000 µL, volumen máximo 2400 µL                                | Incluido – verificable |
| D07    | Parts of a stirred-tank bioreactor – Cytiva               | ALC-04            | Sección completa: recipiente, impeler, bafles, sparger, sensores, sistema de control, gaseado, control de temperatura, puertos                                           | Incluido – verificable |
| D08    | Exploring Principles of Bioreactor Scale-Up – BPI         | ALC-04            | Sección de parámetros: pH, temperatura, DO como parámetros independientes de escala; agitación y flujo de gas como dependientes de escala                                | Incluido – verificable |
| D09    | MCBO: Mammalian Cell Bioprocessing Ontology – bioRxiv     | ALC-04            | Secciones de clases OWL: CellCultureSystem, CultureEnvironmentalCondition, BFO separación occurrents/continuants                                                         | Incluido – verificable |
| D12    | Stirred-Tank Bioreactor Scalability – BPI 2024            | ALC-04            | Sección de parámetros de escala: pH, temperatura, DO como constantes de escala; agitación y flujo de gas como ajustables                                                 | Incluido – verificable |

---

## 7. Respuesta basada en evidencia

### Respuesta a ALC-04: ¿Qué componentes comunes permiten describir estos tres biorreactores en una misma ontología?

Los tres sistemas —BioLector XT, Sartorius 5 L y Sartorius 10 L— comparten un conjunto identificable de **componentes funcionales** que permiten su descripción bajo una misma ontología. La evidencia documental permite organizar estos componentes en cinco categorías:

---

#### 7.1 Recipiente de cultivo (Culture Vessel)

**Evidencia explícita:**

El BioLector XT utiliza **placas de microtitulación (MTP) en formato ANSI/SLAS SBS de 48 pocillos**, con volúmenes de trabajo de 800 a 2400 µL por pocillo (D01, D06). Los sistemas Sartorius emplean **recipientes de vidrio borosilicato autoclavable** (_Univessel® Glass_) disponibles en volúmenes de 1, 2, 5 y 10 L (D03); para el de 5 L el volumen de trabajo es 0.6–5 L y para el de 10 L es 1.5–10 L (D04).

**Inferencia razonable:** Aunque los recipientes difieren radicalmente en tipo y escala (MTP de polímero desechable vs. vidrio reutilizable con camisa), ambos cumplen la función ontológica de **contener el cultivo** y definen el volumen de trabajo. Pueden representarse como subclases de `CultureVessel`.

---

#### 7.2 Sensores (Sensors)

**Evidencia explícita:**

Los tres sistemas comparten medición en línea de:

| Parámetro                     | BioLector XT                                        | Sartorius 5 L                                 | Sartorius 10 L                      |
| ----------------------------- | --------------------------------------------------- | --------------------------------------------- | ----------------------------------- |
| **pH**                        | Sensor óptico pre-calibrado (HP8, LG1)              | Electrodo de pH                               | Electrodo de pH                     |
| **Oxígeno disuelto (DO/pO2)** | Sensor óptico (Pst3, RF)                            | Sensor pO2 (memosens)                         | Sensor pO2 (memosens)               |
| **Temperatura**               | Sensor en cámara de cultivo                         | Sensor de temperatura con termopozo           | Sensor de temperatura con termopozo |
| **Biomasa**                   | Sensor óptico de dispersión de luz (backscattering) | No estándar (inferido: turbidímetro opcional) | No estándar (turbidímetro opcional) |

Fuentes: D01, D04, D06 (BioLector XT); D03, D04 (Sartorius 5 L y 10 L).

El BIOSTAT B también incluye sensores de **espuma (foam), nivel, sustrato** como estándar (D04), que no están reportados en el BioLector XT.

---

#### 7.3 Sistema de control de agitación (Agitation Control System)

**Evidencia explícita:**

- BioLector XT: agitación orbital (shaking) controlada en rpm; la cámara de cultivo controla la frecuencia de agitación. Velocidad mencionada: 600 rpm en cultivos documentados (D06).
- Sartorius 5 L: agitación mecánica por impeler, velocidad 20–1500 rpm (D04).
- Sartorius 10 L: agitación mecánica por impeler, velocidad 20–800 rpm (D04).

**Inferencia razonable:** El mecanismo físico difiere (orbital vs. impeler rotatorio), pero el concepto funcional —control de velocidad de mezcla para transferencia de masa y oxígeno— es equivalente. Ambos son instancias del concepto `AgitationSystem` con la propiedad `hasAgitationSpeed` expresada en rpm.

---

#### 7.4 Sistema de control de temperatura (Temperature Control System)

**Evidencia explícita:**

- BioLector XT: control de temperatura de la cámara de cultivo; condiciones documentadas a 37°C (D06).
- Sartorius BIOSTAT B: control de temperatura mediante chaqueta del recipiente y/o manta calefactora, rango 0–80°C (D04); el sistema incluye loop de enfriamiento y chiller opcional (D03).

Los tres sistemas presentan un mecanismo para mantener la temperatura de cultivo en un setpoint definido, con un sensor de retroalimentación.

---

#### 7.5 Sistema de gaseado (Gassing System)

**Evidencia explícita:**

- BioLector XT: control de O2 (1–100%), CO2 (1–12%), N2 y aire mediante módulos opcionales; gaseado por la tapa de gaseado (_gassing lid_) sobre la MTP (D02, D07).
- Sartorius BIOSTAT B: sistema de gaseado con hasta 4 controladores de flujo másico (MFC) para aire, O2, CO2 y N2; spargers tipo poroso o L-type; flujo total máximo 20 lpm (D04, D10, D11).

**Inferencia razonable:** Los Sartorius utilizan sparger físico dentro del recipiente mientras el BioLector XT gasea desde la tapa (espacio de cabeza), lo que es una diferencia de implementación, pero funcionalmente ambos controlan la composición gaseosa en el cultivo. La propiedad `hasGasComposition` y la clase `GassingSystem` son comunes.

---

#### 7.6 Sistema de control y software (Control System / Software)

**Evidencia explícita:**

- BioLector XT: software BioLection para configuración de perfiles de fed-batch, descarga de datos en tiempo real, interfaz multiusuario (D01).
- Sartorius BIOSTAT B: sistema DCU (Digital Control Unit) con pantalla táctil de 19", conectividad Ethernet, módulo de control de agitación, temperatura, gaseado y bombas (D03, D10).

Ambos sistemas incluyen una **unidad de control centralizada** que recibe señales de sensores y actúa sobre actuadores.

---

#### 7.7 Modos de proceso (Process Modes)

**Evidencia explícita:**

- BioLector XT: batch, fed-batch (perfiles constante, lineal, exponencial, pulsado), continuo (D01, D02, D06).
- Sartorius BIOSTAT B: batch, fed-batch, continuo, perfusión (D03, D12).

Los tres sistemas soportan al menos los modos **batch** y **fed-batch**, con estrategias de adición de sustrato.

---

#### 7.8 Variables operativas comunes (Common Process Variables)

Según la literatura de escalado (D08, D12), las variables **pH, temperatura y DO** son parámetros **independientes de escala** mantenidos constantes en el escalado entre sistemas. Esto confirma que son los candidatos más sólidos para clases o propiedades compartidas en la ontología.

---

#### 7.9 Información no establecida en el corpus

- El BioLector XT **no tiene sparger físico** equivalente al de los Sartorius; el gaseado opera de forma distinta. No se puede afirmar que compartan la clase `Sparger` como componente.
- No se localizó evidencia documentada del sensor de espuma en el BioLector XT.
- Los detalles exactos del controlador PID del BioLector XT no están disponibles en las fuentes consultadas.
- No se pudo acceder al contenido completo de los PDFs de Sartorius (brochures), lo que limita la extracción de especificaciones precisas.

---

## 8. Tabla de afirmaciones y evidencia

| ID evidencia | Afirmación                                                                                                                                                   | Tipo      | Documento     | Página/sección                                      | Fragmento o resumen fiel                                                                                                                | Confianza | Validación experta                  |
| ------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------ | --------- | ------------- | --------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- | --------- | ----------------------------------- |
| E01          | El BioLector XT mide en línea biomasa, fluorescencia, pH y DO usando sensores ópticos pre-calibrados                                                         | Explícita | D01, D05      | Página principal / brochure p.1                     | "...enables real-time evaluation of biomass, fluorescence, pH, dissolved oxygen...operates with online, pre-calibrated optical sensors" | Alta      | No requerida                        |
| E02          | El BioLector XT controla temperatura y velocidad de agitación de la cámara de cultivo                                                                        | Explícita | D02           | Sección de módulos                                  | "The system controls the shaking speed and the temperature inside the cultivation chamber"                                              | Alta      | No requerida                        |
| E03          | El BioLector XT tiene volúmenes de trabajo de 800–2400 µL por pocillo                                                                                        | Explícita | D01, D06      | Especificaciones / nota de aplicación               | Volumen de inicio 2000 µL, máximo 2400 µL en cultivaciones documentadas                                                                 | Alta      | No requerida                        |
| E04          | El BIOSTAT B opera con recipientes de 5 L (0.6–5 L) y 10 L (1.5–10 L)                                                                                        | Explícita | D04           | Ficha técnica A\*SEF                                | "Working volume: 5L (0.6-5L); 10L (1.5-10L)"                                                                                            | Alta      | No requerida                        |
| E05          | El BIOSTAT B incluye sensores de pH, pO2, temperatura, espuma, nivel y sustrato                                                                              | Explícita | D04           | Ficha técnica A\*SEF – Sensors                      | "Sensors: pH, pO2, Temperature, Foam, Level, Substrate addition..."                                                                     | Alta      | No requerida                        |
| E06          | El BIOSTAT B tiene agitación mecánica de 20–1500 rpm para el recipiente de 5 L y 20–800 rpm para el de 10 L                                                  | Explícita | D04           | Ficha técnica A\*SEF                                | "Permitted stirring speed: 5L (20-1500rpm); 10L (20-800rpm)"                                                                            | Alta      | No requerida                        |
| E07          | El BIOSTAT B soporta gaseado con aire, O2, CO2 y N2 mediante MFC hasta 20 lpm total                                                                          | Explícita | D04, D11      | Ficha técnica A\*SEF / Nota de aplicación Sartorius | "Gas flow: air, O2, CO2\*, N2 (max. total flow rate 20 lpm)"                                                                            | Alta      | No requerida                        |
| E08          | El BIOSTAT B soporta modos batch, fed-batch, continuo y perfusión                                                                                            | Explícita | D03           | Página Sartorius – Process Design                   | "...run your Biostat® B in batch, fed-batch, continuous or perfusion mode"                                                              | Alta      | No requerida                        |
| E09          | pH, temperatura y DO son parámetros independientes de escala mantenidos constantes entre biorreactores                                                       | Explícita | D08, D12      | Artículos BPI (2024, 2026)                          | "...maintaining constant scale-independent parameters such as pH, temperature, and dissolved oxygen (DO)"                               | Alta      | No requerida                        |
| E10          | Los biorreactores de tanque agitado (STR) incluyen como componentes: recipiente, impeler, bafles, sparger, sensores, sistema de control y sistema de gaseado | Explícita | D07           | Cytiva – "Parts of a stirred-tank bioreactor"       | Enumeración completa de componentes STR                                                                                                 | Alta      | No requerida                        |
| E11          | El BioLector XT soporta gaseado con O2 (1–100%) y CO2 (1–12%)                                                                                                | Explícita | D01           | Página Danaher/Beckman                              | "Gassing with O2 within a range of 1%–100% and with CO2 within 1%–12%"                                                                  | Alta      | No requerida                        |
| E12          | La ontología MCBO separa material entities (continuants, e.g., biorreactor, sensores) de processes (occurrents) siguiendo principios BFO                     | Explícita | D09           | Sección metodológica MCBO                           | "MCBO strictly separates occurrents (processes) from continuants (material entities)"                                                   | Alta      | Recomendada para adopción en diseño |
| E13          | El BioLector XT soporta modos batch, fed-batch (con perfiles flexibles) y condiciones anaerobias                                                             | Explícita | D01, D02, D06 | Múltiples secciones                                 | Perfiles de alimentación: constante, lineal, exponencial, pulsado-DO                                                                    | Alta      | No requerida                        |
| E14          | El sistema de control DO del BIOSTAT B opera en cascada modificando agitación y flujo de O2                                                                  | Explícita | D10           | Brochure BIOSTAT B-DCU – Cascade Gassing Control    | Control DO en cascada: stirrer speed → air flow → O2 percentage                                                                         | Alta      | No requerida                        |
| E15          | El BioLector XT opera con placa de microtitulación (MTP) en formato ANSI/SLAS SBS de 48 pocillos                                                             | Explícita | D01, D05      | Página principal / brochure                         | "based on a standard ANSI/SLAS (SBS) microtiter plate (MTP) format"                                                                     | Alta      | No requerida                        |

---

## 9. Conceptos ontológicos candidatos

| Concepto candidato         | Tipo sugerido                     | Definición basada en evidencia                                                                                                                       | Fuente asociada    | Estado                                            |
| -------------------------- | --------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------ | ------------------------------------------------- |
| `Bioreactor`               | Clase                             | Sistema cerrado que provee un entorno controlado para el cultivo biológico, con componentes para medición y control de variables operativas          | D07, D08           | Candidato                                         |
| `CultureVessel`            | Clase                             | Recipiente que contiene el medio de cultivo y los microorganismos; subcomponente físico de un biorreactor                                            | D01, D03, D04, D07 | Candidato                                         |
| `MicrotiterPlate`          | Subclase de `CultureVessel`       | Placa de microtitulación en formato ANSI/SLAS SBS con múltiples pocillos, usada como recipiente en el BioLector XT                                   | D01, D15           | Candidato                                         |
| `GlassVessel`              | Subclase de `CultureVessel`       | Recipiente de vidrio borosilicato autoclavable, utilizado en sistemas Sartorius 5 L y 10 L                                                           | D03, D04           | Candidato                                         |
| `Sensor`                   | Clase                             | Dispositivo que mide una variable del proceso (física, química o biológica) y genera una señal de observación                                        | D01, D04, D07      | Candidato                                         |
| `pHSensor`                 | Subclase de `Sensor`              | Sensor que mide el pH del medio de cultivo; puede ser óptico (BioLector XT) o electroquímico (Sartorius)                                             | D01, D04, D06      | Candidato                                         |
| `DissolvedOxygenSensor`    | Subclase de `Sensor`              | Sensor que mide la concentración de oxígeno disuelto (DO/pO2) en el medio                                                                            | D01, D04, D06      | Candidato                                         |
| `TemperatureSensor`        | Subclase de `Sensor`              | Sensor que mide la temperatura del medio o la cámara de cultivo                                                                                      | D02, D04           | Candidato                                         |
| `BiomassSensor`            | Subclase de `Sensor`              | Sensor que mide la densidad celular (biomasa); óptico por backscattering en BioLector XT                                                             | D01, D06           | Candidato                                         |
| `FoamSensor`               | Subclase de `Sensor`              | Sensor de detección de espuma; reportado para sistemas Sartorius; no confirmado en BioLector XT                                                      | D04                | Candidato (requiere validación para BioLector XT) |
| `Actuator`                 | Clase                             | Dispositivo que modifica una condición del proceso en respuesta a señales del controlador                                                            | D07, D10           | Candidato                                         |
| `AgitationSystem`          | Subclase de `Actuator`            | Sistema que provee agitación mecánica u orbital al cultivo para favorecer la mezcla y transferencia de masa                                          | D02, D04, D07      | Candidato                                         |
| `GassingSystem`            | Subclase de `Actuator`            | Sistema que controla el suministro de gases (aire, O2, CO2, N2) al recipiente de cultivo                                                             | D04, D07, D11      | Candidato                                         |
| `TemperatureControlSystem` | Subclase de `Actuator`            | Sistema que mantiene la temperatura del cultivo en un setpoint definido mediante calefacción y/o enfriamiento                                        | D02, D03, D04      | Candidato                                         |
| `PeristalticPump`          | Subclase de `Actuator`            | Bomba peristáltica para adición de ácido, base, antiespumante o sustrato; presente en sistemas Sartorius                                             | D03, D07           | Candidato                                         |
| `ControlSystem`            | Clase                             | Unidad de control (hardware + software) que recibe señales de sensores y envía comandos a actuadores; incluye la lógica PID y la interfaz de usuario | D01, D03, D10      | Candidato                                         |
| `ProcessMode`              | Clase                             | Modalidad de operación del biorreactor que define la estrategia de adición de nutrientes y retiro de producto                                        | D01, D03, D08      | Candidato                                         |
| `BatchMode`                | Subclase de `ProcessMode`         | Modo en que todos los nutrientes se suministran al inicio y no se añaden más durante el cultivo                                                      | D01, D03           | Candidato                                         |
| `FedBatchMode`             | Subclase de `ProcessMode`         | Modo en que se añade sustrato de forma controlada durante el cultivo                                                                                 | D01, D03, D06      | Candidato                                         |
| `OperationalVariable`      | Clase                             | Variable medida o controlada durante el proceso de cultivo; equivale a un parámetro de proceso                                                       | D08, D12           | Candidato                                         |
| `pHValue`                  | Subclase de `OperationalVariable` | Variable que representa el pH del medio de cultivo; independiente de escala                                                                          | D08, D12           | Candidato                                         |
| `DissolvedOxygenValue`     | Subclase de `OperationalVariable` | Variable que representa la concentración de oxígeno disuelto; independiente de escala                                                                | D08, D12           | Candidato                                         |
| `TemperatureValue`         | Subclase de `OperationalVariable` | Variable que representa la temperatura del cultivo; independiente de escala                                                                          | D08, D12           | Candidato                                         |
| `AgitationSpeed`           | Subclase de `OperationalVariable` | Variable que representa la velocidad de agitación (rpm); dependiente de escala                                                                       | D04, D08           | Candidato                                         |
| `WorkingVolume`            | Propiedad de dato                 | Volumen efectivo de cultivo en el recipiente; varía entre sistemas (µL para BioLector XT, L para Sartorius)                                          | D01, D04           | Candidato                                         |
| `OperationScale`           | Clase o propiedad                 | Categoría que clasifica el tamaño del sistema (microscala, escala de banco, piloto)                                                                  | D08                | Candidato                                         |

---

## 10. Relaciones ontológicas candidatas

| Relación candidata   | Dominio sugerido                             | Rango sugerido                                         | Significado                                                                                         | Evidencia asociada | Estado                                  |
| -------------------- | -------------------------------------------- | ------------------------------------------------------ | --------------------------------------------------------------------------------------------------- | ------------------ | --------------------------------------- |
| `hasComponent`       | `Bioreactor`                                 | `Sensor \| Actuator \| CultureVessel \| ControlSystem` | Un biorreactor tiene como componentes físicos sensores, actuadores, recipiente y sistema de control | D07, D01, D03      | Candidato                               |
| `hasSensor`          | `Bioreactor`                                 | `Sensor`                                               | Un biorreactor tiene uno o más sensores que miden variables del proceso                             | D01, D04, D07      | Candidato                               |
| `hasActuator`        | `Bioreactor`                                 | `Actuator`                                             | Un biorreactor tiene actuadores que modifican las condiciones del cultivo                           | D02, D03, D07      | Candidato                               |
| `hasCultureVessel`   | `Bioreactor`                                 | `CultureVessel`                                        | Un biorreactor contiene un recipiente de cultivo                                                    | D01, D03, D04      | Candidato                               |
| `hasControlSystem`   | `Bioreactor`                                 | `ControlSystem`                                        | Un biorreactor posee una unidad de control que gestiona sensores y actuadores                       | D01, D03, D10      | Candidato                               |
| `measuresParameter`  | `Sensor`                                     | `OperationalVariable`                                  | Un sensor mide una variable operativa específica del proceso                                        | D01, D04, D06      | Candidato                               |
| `controlsParameter`  | `Actuator`                                   | `OperationalVariable`                                  | Un actuador controla o modifica una variable operativa                                              | D02, D04, D10      | Candidato                               |
| `hasWorkingVolume`   | `CultureVessel`                              | `xsd:decimal`                                          | Un recipiente de cultivo tiene un volumen de trabajo expresado en unidades (µL, mL, L)              | D01, D04           | Candidato                               |
| `operatesInMode`     | `Bioreactor`                                 | `ProcessMode`                                          | Un biorreactor puede operar en uno o más modos de proceso                                           | D01, D03, D08      | Candidato                               |
| `isScaleOf`          | `Bioreactor`                                 | `OperationScale`                                       | Un biorreactor pertenece a una escala de operación específica                                       | D08, D12           | Candidato                               |
| `hasAgitationSpeed`  | `AgitationSystem`                            | `xsd:decimal`                                          | Un sistema de agitación tiene una velocidad de trabajo (rpm) con rango mínimo y máximo              | D04, D06           | Candidato                               |
| `hasGasType`         | `GassingSystem`                              | `GasType`                                              | Un sistema de gaseado suministra uno o más tipos de gas (aire, O2, CO2, N2)                         | D04, D11           | Candidato                               |
| `isScaleIndependent` | `OperationalVariable`                        | `xsd:boolean`                                          | Indica si una variable operativa es independiente de la escala del biorreactor                      | D08, D12           | Candidato (requiere validación experta) |
| `isInstanceOf`       | `BioLectorXT \| Sartorius5L \| Sartorius10L` | `Bioreactor`                                           | Los tres equipos son individuos de la clase Bioreactor                                              | D01, D03, D04      | Candidato                               |

---

## 11. Triadas RDF candidatas

```
# TRIADAS PARA ESTRUCTURA GENERAL

BioLectorXT  rdf:type  :Bioreactor
  → Documento: D01 | Beckman Coulter official page | Estado: Soportada

Sartorius5L  rdf:type  :Bioreactor
  → Documento: D03, D04 | Sartorius official / A*SEF | Estado: Soportada

Sartorius10L  rdf:type  :Bioreactor
  → Documento: D03, D04 | Sartorius official / A*SEF | Estado: Soportada

# TRIADAS PARA COMPONENTES COMPARTIDOS

:Bioreactor  :hasComponent  :Sensor
  → Documentos: D07, D01, D04 | Cytiva (STR components) + fabricantes | Estado: Soportada

:Bioreactor  :hasComponent  :Actuator
  → Documentos: D07, D02, D03 | Cytiva + Beckman + Sartorius | Estado: Soportada

:Bioreactor  :hasComponent  :CultureVessel
  → Documentos: D01, D03 | Fabricantes oficiales | Estado: Soportada

:Bioreactor  :hasComponent  :ControlSystem
  → Documentos: D01, D03, D10 | Fabricantes oficiales | Estado: Soportada

# TRIADAS PARA SENSORES

BioLectorXT  :hasSensor  :pHSensor
  → Documento: D01, D06 | Beckman Coulter | Estado: Soportada

BioLectorXT  :hasSensor  :DissolvedOxygenSensor
  → Documento: D01, D06 | Beckman Coulter | Estado: Soportada

BioLectorXT  :hasSensor  :TemperatureSensor
  → Documento: D02 | Beckman Coulter modules page | Estado: Soportada

BioLectorXT  :hasSensor  :BiomassSensor
  → Documento: D01 | Beckman Coulter | Estado: Soportada

Sartorius5L  :hasSensor  :pHSensor
  → Documento: D04 | A*SEF / Sartorius | Estado: Soportada

Sartorius5L  :hasSensor  :DissolvedOxygenSensor
  → Documento: D04 | A*SEF / Sartorius | Estado: Soportada

Sartorius5L  :hasSensor  :TemperatureSensor
  → Documento: D04 | A*SEF / Sartorius | Estado: Soportada

Sartorius5L  :hasSensor  :FoamSensor
  → Documento: D04 | A*SEF / Sartorius | Estado: Soportada

Sartorius10L  :hasSensor  :pHSensor
  → Documento: D04 | A*SEF / Sartorius | Estado: Soportada

Sartorius10L  :hasSensor  :DissolvedOxygenSensor
  → Documento: D04 | A*SEF / Sartorius | Estado: Soportada

Sartorius10L  :hasSensor  :TemperatureSensor
  → Documento: D04 | A*SEF / Sartorius | Estado: Soportada

# TRIADAS PARA ACTUADORES

BioLectorXT  :hasActuator  :AgitationSystem
  → Documento: D02 | "The system controls the shaking speed" | Estado: Soportada

BioLectorXT  :hasActuator  :GassingSystem
  → Documento: D01, D02 | O2 1–100%, CO2 1–12%, N2 | Estado: Soportada

BioLectorXT  :hasActuator  :TemperatureControlSystem
  → Documento: D02 | "controls temperature inside the cultivation chamber" | Estado: Soportada

Sartorius5L  :hasActuator  :AgitationSystem
  → Documento: D04 | 20–1500 rpm | Estado: Soportada

Sartorius5L  :hasActuator  :GassingSystem
  → Documento: D04, D11 | Air, O2, CO2, N2 MFC | Estado: Soportada

Sartorius5L  :hasActuator  :TemperatureControlSystem
  → Documento: D04 | 0–80°C | Estado: Soportada

Sartorius5L  :hasActuator  :PeristalticPump
  → Documento: D03 | Peristaltic pumps for pH and foam control | Estado: Soportada

Sartorius10L  :hasActuator  :AgitationSystem
  → Documento: D04 | 20–800 rpm | Estado: Soportada

Sartorius10L  :hasActuator  :GassingSystem
  → Documento: D04 | Air, O2, CO2, N2 MFC | Estado: Soportada

Sartorius10L  :hasActuator  :TemperatureControlSystem
  → Documento: D04 | 0–80°C | Estado: Soportada

# TRIADAS PARA RECIPIENTE

BioLectorXT  :hasCultureVessel  :MicrotiterPlate
  → Documento: D01 | "ANSI/SLAS (SBS) microtiter plate (MTP) format" | Estado: Soportada

Sartorius5L  :hasCultureVessel  :GlassVessel
  → Documento: D03, D04 | Borosilicate glass autoclavable vessel | Estado: Soportada

Sartorius10L  :hasCultureVessel  :GlassVessel
  → Documento: D03, D04 | Borosilicate glass autoclavable vessel | Estado: Soportada

# TRIADAS PARA VOLUMEN DE TRABAJO

:MicrotiterPlate  :hasWorkingVolume  "0.0008–0.0024"  # en litros
  → Documento: D01, D06 | 800–2400 µL | Estado: Soportada

:GlassVessel_5L  :hasWorkingVolume  "0.6–5"  # en litros
  → Documento: D04 | A*SEF ficha técnica | Estado: Soportada

:GlassVessel_10L  :hasWorkingVolume  "1.5–10"  # en litros
  → Documento: D04 | A*SEF ficha técnica | Estado: Soportada

# TRIADAS PARA MODOS DE PROCESO

BioLectorXT  :operatesInMode  :BatchMode
  → Documento: D01 | Estado: Soportada

BioLectorXT  :operatesInMode  :FedBatchMode
  → Documento: D01, D06 | Estado: Soportada

Sartorius5L  :operatesInMode  :BatchMode
  → Documento: D03 | Estado: Soportada

Sartorius5L  :operatesInMode  :FedBatchMode
  → Documento: D03 | Estado: Soportada

Sartorius10L  :operatesInMode  :BatchMode
  → Documento: D03 | Estado: Soportada

Sartorius10L  :operatesInMode  :FedBatchMode
  → Documento: D03 | Estado: Soportada

# TRIADAS PARA VARIABLES INDEPENDIENTES DE ESCALA

:pHValue  :isScaleIndependent  "true"
  → Documentos: D08, D12 | BPI artículos | Estado: Parcialmente soportada (requiere validación experta)

:DissolvedOxygenValue  :isScaleIndependent  "true"
  → Documentos: D08, D12 | BPI artículos | Estado: Parcialmente soportada (requiere validación experta)

:TemperatureValue  :isScaleIndependent  "true"
  → Documentos: D08, D12 | BPI artículos | Estado: Parcialmente soportada (requiere validación experta)
```

---

## 12. Sinónimos y variantes terminológicas

| Término principal          | Sinónimos o variantes documentadas                                                               | Idioma | Documento de soporte |
| -------------------------- | ------------------------------------------------------------------------------------------------ | ------ | -------------------- |
| `DissolvedOxygen`          | DO, pO2, dissolved oxygen concentration, oxygen saturation, DOT                                  | EN/ES  | D01, D04, D06, D12   |
| `pH`                       | pH value, pH sensor, ácido-base, regulación de pH                                                | EN/ES  | D01, D04, D06        |
| `Biomass`                  | biomass signal, backscattering, OD (optical density), turbidity                                  | EN     | D01, D06             |
| `AgitationSystem`          | shaking, stirring, impeller, agitation, mixing, shaker frequency                                 | EN     | D01, D02, D04, D06   |
| `GassingSystem`            | gassing, aeration, sparger, gas mixing, gas flow, gassing lid                                    | EN     | D04, D07, D11        |
| `CultureVessel`            | culture vessel, bioreactor vessel, fermentation vessel, MTP, well plate, Univessel, glass vessel | EN     | D01, D03, D04        |
| `ControlSystem`            | control tower, DCU, Digital Control Unit, controller, BioLection software                        | EN     | D01, D03, D10        |
| `FedBatchMode`             | fed-batch, fed-batch cultivation, substrate feeding, feeding strategy                            | EN     | D01, D06, D08        |
| `TemperatureControlSystem` | temperature control, heating blanket, jacket, chiller, thermostat                                | EN     | D02, D04             |
| `WorkingVolume`            | working volume, volumen de trabajo, cultivation volume, vessel volume                            | EN/ES  | D01, D04             |
| `Bioreactor`               | fermenter, fermentor, biorreactor, microbioreactor, cultivation system                           | EN/ES  | D01, D03, D04, D07   |

---

## 13. Vacíos, riesgos y decisiones pendientes

### Información faltante

1. **Manual de usuario completo del BioLector XT (m2p-labs/Beckman Coulter):** No fue posible acceder al manual técnico completo, que contendría especificaciones exactas del controlador PID, rangos de temperatura, y detalles del sistema de medición óptica.
2. **Brochure/manual completo del BIOSTAT B de Sartorius:** Los PDFs oficiales de Sartorius no fueron accedidos en su contenido completo (D10, D11 sólo parcialmente). Se requiere suministrar estos documentos.
3. **Sensor de biomasa en los Sartorius:** No se confirmó si los Sartorius 5 L y 10 L incluyen sensor de biomasa en línea de forma estándar (el turbidímetro aparece como opcional en D04). Esto crea una asimetría con el BioLector XT.
4. **Sensor de espuma en BioLector XT:** No hay evidencia documentada de un sensor de espuma en el BioLector XT; en los Sartorius está documentado como estándar.

### Ambigüedades terminológicas

- **"Agitación":** El BioLector XT usa agitación orbital (shaking); los Sartorius usan agitación mecánica con impeler. Deben ser subclases diferentes de `AgitationSystem` o distinguirse mediante una propiedad `hasAgitationType`.
- **"Gaseado":** El gaseado en el BioLector XT ocurre desde la tapa (headspace gassing), mientras en los Sartorius es por sparger sumergido. La propiedad `hasGassingMethod` podría distinguir estos casos.
- **"DO sensor":** El BioLector XT usa sensores ópticos no invasivos (fluorescencia); los Sartorius típicamente usan electrodos amperométricos o sensores ópticos Memosens. Aunque miden la misma variable, el principio de medición difiere.

### Configuraciones dependientes del equipo

- Los módulos del BioLector XT (O2 up/down regulation, CO2 up regulation, módulo microfluidico) son opcionales; la ontología deberá manejar componentes opcionales vs. obligatorios.
- El BIOSTAT B puede configurarse como single o twin (doble); la ontología deberá prever configuraciones de múltiples recipientes por controlador.

### Datos que requieren validación con expertos

- La clasificación de `isScaleIndependent` para pH, DO y temperatura debe ser validada por expertos en bioprocesos para el caso específico BioLector XT ↔ Sartorius 5 L ↔ Sartorius 10 L.
- La equivalencia funcional entre el módulo microfluidico del BioLector XT y las bombas peristálticas del BIOSTAT B para adición de sustrato y control de pH.
- Si el BioLector XT puede o no ser clasificado como biorreactor de tanque agitado (STR) o requiere una categoría propia (microbioreactor / high-throughput screening system).

### Documentos adicionales necesarios

- Manual de usuario del BioLector XT (m2p-labs, disponible solo tras registro en Beckman Coulter)
- Brochure técnico BIOSTAT® B (SBI1513-E) completo en PDF
- Notas de aplicación de escalado BioLector XT → Sartorius (si disponibles)
- Especificaciones del sistema BioLection software

---

## 14. Registro metodológico para el documento de investigación

La pregunta ALC-04 busca identificar los componentes comunes a los sistemas BioLector XT (Beckman Coulter / m2p-labs), Sartorius 5 L y Sartorius 10 L (ambos basados en el controlador BIOSTAT® B de Sartorius Stedim Biotech), con el objetivo de establecer la base conceptual compartida de una ontología OWL/RDF para su representación unificada. La estrategia de búsqueda se centró en fuentes primarias de los fabricantes —páginas oficiales de producto, brochures técnicos y notas de aplicación— complementadas con recursos técnicos de fabricantes independientes (Cytiva), publicaciones de la industria de bioprocesos (BioProcess International) y un preprint de ontología de bioprocesos (MCBO, bioRxiv 2026). Se emplearon términos de búsqueda en inglés enfocados en componentes, sensores, actuadores y parámetros de proceso para cada equipo, así como en principios de escalado de biorreactores. Los criterios de inclusión priorizaron documentos con autoría verificable, fecha clara y evidencia técnica extractable (especificaciones, tablas, definiciones). Se excluyeron fuentes sin trazabilidad o de naturaleza comercial no verificable. El corpus final incluyó nueve documentos clave, entre los cuales se identificaron los siguientes componentes comunes con soporte documental explícito: recipiente de cultivo (`CultureVessel`), sensores de pH, oxígeno disuelto y temperatura (`pHSensor`, `DissolvedOxygenSensor`, `TemperatureSensor`), sistema de agitación (`AgitationSystem`), sistema de gaseado (`GassingSystem`), sistema de control de temperatura (`TemperatureControlSystem`) y unidad de control de proceso (`ControlSystem`). Las variables pH, temperatura y DO fueron confirmadas como parámetros independientes de escala mediante dos artículos técnicos de BioProcess International (2024 y 2026). Los conceptos ontológicos candidatos propuestos incluyen veintitrés clases y propiedades organizadas en cinco categorías funcionales, con triadas RDF soportadas por al menos un documento verificable por afirmación. Las principales limitaciones incluyen la falta de acceso al contenido completo de los manuales de usuario y brochures técnicos en PDF, la diferencia en el mecanismo de agitación y gaseado entre el BioLector XT y los sistemas Sartorius, y la necesidad de validación experta para la asignación de la propiedad `isScaleIndependent` en el contexto específico de los tres equipos. Las relaciones y conceptos identificados son preliminares y requieren revisión por expertos en bioprocesos y en ingeniería ontológica antes de su formalización en OWL.

---

## 15. Estado final

- **Nivel de confianza general:** Alto (para componentes soportados por fuentes primarias de fabricante); Medio (para relaciones cruzadas y propiedad de independencia de escala)
- **Estado de la respuesta:** Soportada
- **Estado del corpus:** Suficiente para identificación de componentes comunes principales; Parcial para detalles técnicos profundos (requiere acceso a manuales completos)
- **Próxima acción recomendada:**
  1. Suministrar al investigador el manual de usuario completo del BioLector XT y el brochure técnico completo del BIOSTAT® B para extracción de especificaciones detalladas.
  2. Validar con experto en bioprocesos la equivalencia funcional entre el módulo microfluidico del BioLector XT y las bombas peristálticas del BIOSTAT B.
  3. Validar con experto en ontologías si el BioLector XT debe ser subclase de `HighThroughputScreeningSystem` o de `Bioreactor` directamente.
  4. Formalizar los conceptos y relaciones candidatos en Protégé OWL como versión preliminar (v0.1) de la ontología.
  5. Ejecutar análisis de preguntas de competencia (competency questions) para verificar la cobertura del esquema propuesto.
