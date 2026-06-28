# ALC-03: ¿Cómo se diferencian conceptualmente BioLector XT, Sartorius 5 L y Sartorius 10 L como sistemas de bioproceso?

---

## 1. Identificación de la pregunta

| Campo                  | Descripción                                                                                                    |
| ---------------------- | -------------------------------------------------------------------------------------------------------------- |
| **ID**                 | ALC-03                                                                                                         |
| **Nivel metodológico** | Conceptual-analítico                                                                                           |
| **Tema**               | Diferenciación ontológica de sistemas de bioproceso por escala, tecnología y propósito funcional               |
| **Pregunta**           | ¿Cómo se diferencian conceptualmente BioLector XT, Sartorius 5 L y Sartorius 10 L como sistemas de bioproceso? |

---

## 2. Propósito de la pregunta

La pregunta busca establecer las diferencias conceptuales fundamentales entre tres sistemas de bioproceso que operan en escalas radicalmente distintas: uno perteneciente al dominio del microbioreactor de alto rendimiento (BioLector XT) y dos al dominio del biorreactor de tanque agitado a escala de banco de laboratorio (Sartorius 5 L y 10 L). Esta distinción es indispensable para la ontología porque determina:

- Las **clases raíz** bajo las cuales cada sistema debe clasificarse.
- Las **propiedades de datos** específicas de cada escala (volumen de trabajo, velocidad de agitación, número de cultivos paralelos).
- Las **relaciones funcionales** de escalado y equivalencia entre sistemas.
- Los **principios operativos** que gobiernan cada plataforma (agitación orbital vs. impeller mecánico; medición óptica en línea vs. sensorización electroquímica).

Sin esta diferenciación conceptual, la ontología no podría representar correctamente el continuo de escalas que va desde el tamizaje en microscala hasta la optimización a escala de laboratorio superior.

---

## 3. Plan de búsqueda documental

### 3.1 Información técnica requerida

- Principio de operación de cada sistema (microbiorreactor de placa vs. biorreactor de tanque agitado).
- Volúmenes de trabajo (mínimo y máximo) por sistema.
- Número de cultivos paralelos posibles.
- Variables operativas controladas (temperatura, pH, DO, agitación).
- Tipo de sensores utilizados (ópticos pre-calibrados vs. electroquímicos in situ).
- Modo de agitación (orbital/shake vs. impeller mecánico).
- Aplicaciones declaradas por el fabricante.
- Posición de cada sistema en la cadena de desarrollo de bioprocesos.

### 3.2 Tipos de documentos necesarios

- Fichas técnicas y páginas de producto de los fabricantes (Beckman Coulter / m2p-labs; Sartorius).
- Manuales técnicos oficiales (si accesibles en línea).
- Artículos científicos revisados por pares que hayan utilizado uno o más de estos sistemas.
- Notas de aplicación de fabricante.
- Artículos de revisión sobre escalado en bioprocesos.

### 3.3 Repositorios y sitios sugeridos

- Sitio oficial Beckman Coulter: `beckman.com/microbioreactor/biolector-xt`
- Sitio oficial Sartorius: `sartorius.com/en/products/fermentation-bioreactors`
- PubMed / PMC (artículos de bioprocesos con BioLector o Biostat B)
- Scientific Reports / Nature
- Danaher Life Sciences (distribuidora de Beckman Coulter)
- A\*STAR SEF (registro técnico de equipos de laboratorio con especificaciones)

### 3.4 Términos de búsqueda

**Español:** BioLector XT microbiorreactor, Sartorius Biostat B 5 litros 10 litros, biorreactor tanque agitado banco de laboratorio, escalado de bioprocesos, microplaca de microtitulación FlowerPlate, diferencia conceptual escala microbiorreactor

**Inglés:** BioLector XT microbioreactor specifications, Sartorius Biostat B 5L 10L working volume, stirred tank bioreactor bench-scale, bioprocess scale-up microtiter plate, FlowerPlate well volume, BioLector vs stirred tank conceptual difference

### 3.5 Ecuaciones de búsqueda sugeridas

```
("BioLector XT" OR "BioLector Pro") AND ("microtiter plate" OR "FlowerPlate") AND ("bioprocess development" OR "scale-up")

("Sartorius" OR "Biostat B") AND ("5L" OR "5 liter" OR "10L" OR "10 liter") AND ("working volume" OR "stirred tank" OR "scale-down")

("BioLector" OR "microbioreactor") AND ("Sartorius" OR "bench-scale bioreactor") AND ("scale" OR "conceptual difference")
```

---

## 4. Documentos candidatos encontrados

| ID doc | Título                                                                                                              | Entidad autora                                                     | Año                               | Tipo de fuente                              | URL/DOI verificable                                                                                       | Relación con la pregunta                                                                                              | Decisión preliminar |
| ------ | ------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------ | --------------------------------- | ------------------------------------------- | --------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------- | ------------------- |
| D01    | BioLector XT Microbioreactor – Product Page                                                                         | Beckman Coulter / m2p-labs (Danaher)                               | 2021                              | Página de producto oficial del fabricante   | `beckman.com/microbioreactor/biolector-xt`                                                                | Descripción del BioLector XT: tecnología, sensores, placas, aplicaciones                                              | Include             |
| D02    | Next-Generation BioLector XT Microbioreactor – Press Release                                                        | Beckman Coulter Life Sciences                                      | 2021                              | Comunicado de prensa oficial del fabricante | `beckman.com/news/next-generation-biolector-xt-microbioreactor`                                           | Características diferenciales del BioLector XT respecto a generaciones anteriores                                     | Include             |
| D03    | Biostat® B – Benchtop Bioreactor Controller                                                                         | Sartorius                                                          | Vigente (consultado 2025–2026)    | Página de producto oficial del fabricante   | `sartorius.com/en/products/fermentation-bioreactors/benchtop-bioreactors/biostat-b`                       | Especificaciones del Biostat B 1–10 L, incluyendo 5 L y 10 L                                                          | Include             |
| D04    | Bioreactor: Sartorius 10 (w/MFCS) – BIOSTAT B – A\*STAR SEF                                                         | A\*STAR (institución de investigación pública de Singapur)         | S/f (datos técnicos verificables) | Registro técnico de equipo institucional    | `asef.a-star.edu.sg/equipment/bioreactor-sartorius-10-w-mfcs-biostat-b-sifbi`                             | Especificaciones técnicas del Biostat B para volúmenes 2 L, 5 L y 10 L (rpm, gas, temperatura, sensores)              | Include             |
| D05    | Benchtop Bioreactors for Microbial Fermentation                                                                     | Sartorius                                                          | Vigente                           | Página de categoría del fabricante          | `sartorius.com/en/products/fermentation-bioreactors/benchtop-bioreactors`                                 | Descripción conceptual de la plataforma Biostat B como modelo de escala descendente                                   | Include             |
| D06    | High-Throughput Shaken Microbioreactors                                                                             | Genetic Engineering & Biotechnology News (con autoría de m2p-labs) | 2024                              | Artículo técnico con autoría verificable    | `genengnews.com/insights/high-throughput-shaken-microbioreactors/`                                        | Principio de funcionamiento del BioLector y FlowerPlate, OTR, escalado hacia fermentador de laboratorio               | Include             |
| D07    | Scale-up from microtiter plate to laboratory fermenter (Kensy et al.)                                               | Kensy F. et al. – BMC Biotechnology / PMC                          | 2009                              | Artículo científico revisado por pares      | `pmc.ncbi.nlm.nih.gov/articles/PMC2806293/`                                                               | Validación de escalado de MTP (200 µL) a fermentador de 1.4 L; relevante para entender relación BioLector–biorreactor | Include             |
| D08    | An automated workflow for enhancing microbial bioprocess optimization on a novel microbioreactor platform (PMC)     | Ochsner A.M. et al. – PMC                                          | 2012                              | Artículo científico revisado por pares      | `pmc.ncbi.nlm.nih.gov/articles/PMC3526558/`                                                               | Uso del BioLector en FlowerPlate a 1 mL; escalado a 1 L y 20 L                                                        | Include             |
| D09    | Simplifying the Scaling Process Between Bioreactors                                                                 | Sartorius (Science Snippets)                                       | S/f                               | Artículo técnico del fabricante             | `sartorius.com/en/knowledge/science-snippets/simplifying-the-scaling-process-between-bioreactors-1040122` | Principios de escalado geométrico del Biostat; diseño de tanque agitado y proporciones constantes                     | Include             |
| D10    | High-throughput microbioreactor provides a capable tool for early stage bioprocess development (Scientific Reports) | Lubrano C. et al. – Scientific Reports / Nature                    | 2021                              | Artículo científico revisado por pares      | DOI: 10.1038/s41598-021-81633-6                                                                           | Uso del BioLector con FlowerPlates a 800 µL para E. coli                                                              | Include             |
| D11    | BioLector XT Microbioreactor – Danaher Life Sciences                                                                | Danaher Life Sciences                                              | 2024–2025                         | Página de distribución oficial              | `lifesciences.danaher.com/us/en/products/family/biolector-xt-microbioreactors.html`                       | Descripción del BioLector XT; link a documentación técnica (Technical Data Sheet)                                     | Uncertain           |
| D12    | Bioprocess Control in Microscale: Scalable Fermentations in Disposable and User-Friendly Microfluidic Systems (PMC) | Funke M. et al. – PMC                                              | 2010                              | Artículo científico revisado por pares      | `pmc.ncbi.nlm.nih.gov/articles/PMC3000389/`                                                               | Descripción de tecnología microfluidica BioLector; escalado hacia biorreactores de gran escala                        | Include             |
| D13    | Biostat B – Remma (especificaciones técnicas detalladas)                                                            | Remma (revendedor europeo)                                         | S/f                               | Ficha técnica de revendedor                 | `remma.fr/en/model/biostat-b-benchtop-bioreactor`                                                         | Especificaciones técnicas del Biostat B (temperatura, motor, RPM, volumen compatible)                                 | Uncertain           |

---

## 5. Evaluación de documentos candidatos

| ID doc | Relevancia | Autoridad  | Trazabilidad | Cobertura de la pregunta | Evidencia localizable | Justificación                                                                                                                                                 |
| ------ | ---------- | ---------- | ------------ | ------------------------ | --------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| D01    | Alta       | Alta       | Alta         | Alta                     | Alta                  | Fuente primaria del fabricante; describe BioLector XT directamente con sus características diferenciales.                                                     |
| D02    | Alta       | Alta       | Alta         | Media                    | Alta                  | Comunicado oficial del fabricante con declaraciones específicas sobre tecnología del BioLector XT.                                                            |
| D03    | Alta       | Alta       | Alta         | Alta                     | Alta                  | Fuente primaria Sartorius para Biostat B; cubre el rango 1–10 L incluyendo los 5 L y 10 L de interés.                                                         |
| D04    | Alta       | Alta       | Alta         | Alta                     | Alta                  | Registro técnico institucional (A\*STAR) con especificaciones numéricas verificables del Biostat B para 5 L y 10 L.                                           |
| D05    | Alta       | Alta       | Alta         | Media                    | Alta                  | Proporciona contexto conceptual del uso de los Sartorius como modelos de escala descendente.                                                                  |
| D06    | Alta       | Media-Alta | Media        | Alta                     | Alta                  | Autoría vinculada a m2p-labs (creadora del BioLector); describe principio de operación y FlowerPlate. Publicado en GEN, revista especializada.                |
| D07    | Media      | Alta       | Alta         | Media                    | Alta                  | Artículo clásico (PMC, revisado por pares) que establece escalabilidad MTP→fermentador; contextualiza la posición del BioLector en el pipeline de desarrollo. |
| D08    | Alta       | Alta       | Alta         | Alta                     | Alta                  | Artículo PMC con uso explícito de BioLector en FlowerPlate a 1 mL; validación de escalado; compara tres escalas (1 mL, 1 L, 20 L).                            |
| D09    | Alta       | Alta       | Alta         | Media                    | Alta                  | Fuente Sartorius oficial que explica la arquitectura de escalado geométrico de sus biorreactores (relevante para Sartorius 5 L vs 10 L).                      |
| D10    | Alta       | Alta       | Alta         | Alta                     | Alta                  | Artículo Scientific Reports 2021; uso del BioLector con FlowerPlates a 800 µL para E. coli; provee evidencia reciente del volumen de trabajo.                 |
| D11    | Media      | Alta       | Media        | Media                    | Media                 | Página de distribución oficial Danaher; contiene enlace a Technical Data Sheet no accesible directamente sin registro. Marcado como Uncertain.                |
| D12    | Alta       | Alta       | Alta         | Alta                     | Alta                  | Artículo PMC (Funke et al.) que describe la plataforma microfluidica BioLector y su posición en el continuo de escalado; tecnología de referencia.            |
| D13    | Media      | Media      | Baja         | Media                    | Media                 | Revendedor comercial europeo; especificaciones pueden ser derivadas de material del fabricante. Sin autoría directa de Sartorius. Uncertain.                  |

---

## 6. Corpus documental seleccionado

| ID doc | Documento seleccionado                                                              | Pregunta asociada | Fragmentos o páginas relevantes                                                                                       | Estado   |
| ------ | ----------------------------------------------------------------------------------- | ----------------- | --------------------------------------------------------------------------------------------------------------------- | -------- |
| D01    | BioLector XT – Product Page (Beckman Coulter)                                       | ALC-03            | Descripción de plataforma MTP, sensores ópticos pre-calibrados, 48 pocillos, alimentación microfluidica, aplicaciones | Incluido |
| D02    | Next-Generation BioLector XT – Press Release (Beckman Coulter)                      | ALC-03            | Características nuevas del BioLector XT: gassing 100% O₂, anaerobiosis, FlowerPlate, automatización                   | Incluido |
| D03    | Biostat® B – Benchtop Bioreactor Controller (Sartorius oficial)                     | ALC-03            | Rango de volumen 1–10 L, gassing hasta 4 MFC, DO cascade control, modos batch/fed-batch/perfusión                     | Incluido |
| D04    | Bioreactor: Sartorius 10 (BIOSTAT B) – A\*STAR SEF                                  | ALC-03            | Especificaciones: volúmenes de trabajo 5 L (0.6–5 L), 10 L (1.5–10 L); RPM; gases; temperatura; lista de sensores     | Incluido |
| D05    | Benchtop Bioreactors – Sartorius (categoría)                                        | ALC-03            | Contexto conceptual: escala de banco, uso como modelo de escala descendente, modos de proceso                         | Incluido |
| D06    | High-Throughput Shaken Microbioreactors (GEN / m2p-labs)                            | ALC-03            | OTR FlowerPlate hasta 0.2 mol/L/h; validación de escalado MTP a biorreactor 1.4 L; medición en línea                  | Incluido |
| D07    | Scale-up from MTP to laboratory fermenter (Kensy et al., BMC Biotech)               | ALC-03            | Escalado a 200 µL → 1.4 L; kLa como criterio de escala; posición del BioLector en el pipeline                         | Incluido |
| D08    | Automated workflow for microbioreactor optimization (PMC, 2012)                     | ALC-03            | Uso de BioLector a 1 mL con FlowerPlate B; escalado a 1 L y 20 L; criterios de escalado (DO > 20%)                    | Incluido |
| D09    | Simplifying the Scaling Process Between Bioreactors (Sartorius)                     | ALC-03            | Diseño clásico STR; relaciones geométricas constantes entre escalas; herramienta BioPAT Process Insights              | Incluido |
| D10    | High-throughput microbioreactor – early stage bioprocess (Scientific Reports, 2021) | ALC-03            | FlowerPlate B a 800 µL; shaking 1400 rpm; monitoreo de biomasa cada 15 min                                            | Incluido |
| D12    | Bioprocess Control in Microscale (Funke et al., PMC, 2010)                          | ALC-03            | Tecnología microfluidica BioLector; escalado confiable a procesos a gran escala; base de desarrollo de procesos       | Incluido |

---

## 7. Respuesta basada en evidencia

### 7.1 Dimensiones de diferenciación conceptual

Los tres sistemas objeto de estudio se diferencian en al menos cinco dimensiones conceptuales fundamentales:

---

### Dimensión 1: Escala operativa (volumen de trabajo)

**BioLector XT** opera en la escala de **microscala** (microescala). En cultivaciones con BioLector en FlowerPlates, el volumen de llenado es de 1 mL, lo que resulta en una OTRMax de 80 mmol·L⁻¹·h⁻¹. En cultivaciones con el sistema BioLector (m2p-labs GmbH), los precultivos se realizan en FlowerPlates de 48 pocillos con 800 µL de medio. Esto ubica al BioLector XT en el rango de cientos de microlitros por pocillo, con hasta 48 cultivos simultáneos.

**Sartorius 5 L y 10 L (Biostat B)** operan en la escala de **biorreactores de tanque agitado a nivel de banco de laboratorio**. Las especificaciones técnicas del Biostat B indican volúmenes de trabajo de: 5 L (0.6–5 L) y 10 L (1.5–10 L), con velocidades de agitación permitidas de 5 L (20–1500 rpm) y 10 L (20–800 rpm), y flujo de gas de aire, O₂, CO₂ y N₂ con caudal total máximo de 20 lpm.

---

### Dimensión 2: Principio de cultivo y agitación

**BioLector XT** utiliza **agitación orbital** (shaking) de placas de microtitulación. El desarrollo de nuevas geometrías de pocillo en forma de flor, realizadas en la FlowerPlate, proporciona condiciones de transferencia de oxígeno ilimitadas (OTR hasta 0.2 mol/L/h) para la mayoría de las aplicaciones de fermentación microbiana, evitando así la necesidad de control activo de pH.

**Sartorius 5 L y 10 L** utilizan **agitación mecánica por impeller** (turbina) en un tanque agitado clásico. Los biorreactores Sartorius tienen un diseño clásico de tanque agitado con eje central agitado desde arriba, una relación constante entre la altura del recipiente y el diámetro del recipiente, y relaciones constantes entre el diámetro del impeller y el diámetro del recipiente.

---

### Dimensión 3: Paralelismo y rendimiento

**BioLector XT** es un sistema de **alto rendimiento** (high-throughput). El nuevo BioLector XT Microbioreactor permite el tamizaje de cepas de alto rendimiento, el monitoreo de parámetros de cultivo y la optimización de estrategias de alimentación. Las características populares del microbiorreactor BioLector incluyen placas de microtitulación (MTPs) de 48 pocillos desechables con mediciones en línea y control simultáneo de pH y alimentación gestionado por tecnología microfluidica patentada.

**Sartorius 5 L y 10 L** son sistemas de **un único cultivo por recipiente** (o dos en configuración twin). El Biostat B puede usarse en configuración individual o doble (twin), con opciones de recipientes de vidrio reutilizables para tanque agitado, recipiente de uso único Univessel SU o bolsas Flexsafe RM de mezcla tipo wave.

---

### Dimensión 4: Tipo de sensores y monitoreo

**BioLector XT** emplea **sensores ópticos pre-calibrados** y medición no invasiva. El microbiorreactor BioLector XT se basa en un formato estándar de placa de microtitulación ANSI/SLAS (SBS) y opera con sensores ópticos en línea pre-calibrados. El BioLector XT Microbioreactor es ideal para cultivos microbianos, fúngicos y de algas con evaluaciones en tiempo real de biomasa, pH, oxígeno disuelto (DO) y fluorescencia para aerobios y anaerobios.

**Sartorius 5 L y 10 L (Biostat B)** emplean una suite de **sensores electroquímicos y fisicoquímicos in situ**. Los sensores del Biostat B incluyen: pH, pO₂, temperatura, espuma, nivel, adición de sustrato, mezcla de gases, agitación, control gravimétrico de alimentación y cosecha, control de flujo de gas total constante, presión del recipiente, redox y turbidez.

---

### Dimensión 5: Función en el pipeline de desarrollo de bioprocesos

**BioLector XT** está posicionado en la **fase temprana de desarrollo**: tamizaje de cepas, optimización de medios y condiciones. El BioLector microfluidico permite fermentaciones a microscala rentables y amigables con el usuario que proporcionan una alta salida de información y simulan bioprocesos a gran escala. Esta es la base obligatoria para el desarrollo confiable de procesos y el posterior escalado.

**Sartorius 5 L y 10 L** están posicionados en la **fase de caracterización y optimización del proceso** y como **modelo de escala descendente** (scale-down model). El Biostat B proporciona funcionalidad mejorada y un nivel incomparable de opciones para procesos de cultivo celular y microbiano, lo que lo convierte en el modelo ideal de escala descendente para los procesos a gran escala. En el desarrollo de procesos, las tareas pueden variar desde la definición de los parámetros óptimos del proceso hasta la obtención de material para el proceso de aguas abajo o el desarrollo de ensayos o la realización de estudios en animales.

---

### 7.2 Relación de escalado entre los tres sistemas

La escalabilidad de las MTPs a los fermentadores de tanque agitado (STFs) podría hacerlos idealmente adecuados como microbiorreactor y como unidad de reactor de escala descendente. Esta escalabilidad combinada con el alto rendimiento y el monitoreo en línea de parámetros de proceso importantes crea una herramienta muy poderosa para la investigación y el desarrollo de bioprocesos.

La relación entre los tres sistemas puede entenderse como un **continuo escalar**: BioLector XT (µL–mL) → Sartorius 5 L (0.6–5 L) → Sartorius 10 L (1.5–10 L). Un experimento de escalado en un biorreactor de 15 L (10 L de volumen de trabajo), similar al proceso a 1.5 L, es el punto de partida para la optimización de los parámetros identificados a esa escala. La diferencia conceptual entre Sartorius 5 L y Sartorius 10 L es principalmente cuantitativa (mayor volumen, menor RPM máxima), mientras que la diferencia entre BioLector XT y ambos Sartorius es **cualitativa y funcional** (plataforma de tamizaje paralelo vs. plataforma de proceso individual de tanque agitado).

---

## 8. Tabla de afirmaciones y evidencia

| ID evidencia | Afirmación                                                                                                                                              | Tipo de evidencia | Documento               | Página/sección                              | Fragmento o resumen                                                                                      | Confianza  | Validación experta                                   |
| ------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------- | ----------------------- | ------------------------------------------- | -------------------------------------------------------------------------------------------------------- | ---------- | ---------------------------------------------------- |
| E01          | BioLector XT opera con placas de 48 pocillos en formato ANSI/SLAS                                                                                       | Explícita         | D01, D03                | Página de producto                          | Plataforma basada en MTP formato estándar SBS, 48 pocillos desechables                                   | Alta       | No requerida                                         |
| E02          | El volumen de cultivo por pocillo del BioLector está en el rango de 800–1000 µL                                                                         | Explícita         | D08, D10                | Sección de métodos (PMC)                    | Cultivaciones a 800 µL (FlowerPlate B) y 1 mL (FlowerPlate genérico)                                     | Alta       | Recomendada para valores exactos por modelo de plato |
| E03          | El Sartorius Biostat B 5 L tiene volumen de trabajo de 0.6–5 L                                                                                          | Explícita         | D04                     | Sección de especificaciones técnicas        | Volumen de trabajo 5L (0.6–5L)                                                                           | Alta       | No requerida                                         |
| E04          | El Sartorius Biostat B 10 L tiene volumen de trabajo de 1.5–10 L                                                                                        | Explícita         | D04                     | Sección de especificaciones técnicas        | Volumen de trabajo 10L (1.5–10L)                                                                         | Alta       | No requerida                                         |
| E05          | El Sartorius 5 L permite agitación de 20–1500 rpm; el 10 L de 20–800 rpm                                                                                | Explícita         | D04                     | Especificaciones técnicas A\*STAR           | Stirring speed: 5L (20–1500rpm); 10L (20–800rpm)                                                         | Alta       | Recomendada (puede variar por versión)               |
| E06          | El BioLector XT utiliza sensores ópticos pre-calibrados (no electroquímicos in situ)                                                                    | Explícita         | D01, D08                | Página de producto; artículo PMC            | Sensores ópticos en línea pre-calibrados; medición de biomasa por backscatter, pH y DO por fluorescencia | Alta       | No requerida                                         |
| E07          | El Biostat B 10 L lleva sensores de pH, pO₂, temperatura, espuma, nivel, redox y turbidez                                                               | Explícita         | D04                     | Especificaciones técnicas A\*STAR           | Lista de sensores documentada explícitamente                                                             | Alta       | Recomendada (versiones B vs. B-DCU)                  |
| E08          | El BioLector XT está diseñado para tamizaje de alto rendimiento en fase temprana                                                                        | Explícita         | D01, D02, D12           | Páginas de producto y artículo Funke et al. | "High-throughput strain screenings", "base obligatoria para el desarrollo confiable de procesos"         | Alta       | No requerida                                         |
| E09          | El Biostat B es el modelo estándar de industria para caracterización y scale-down                                                                       | Explícita         | D04, D05                | Páginas Sartorius; A\*STAR SEF              | "Ideal scale-down model for your large-scale process"                                                    | Alta       | No requerida                                         |
| E10          | La FlowerPlate proporciona OTR hasta 0.2 mol/L/h para cultivos microbianos                                                                              | Explícita         | D06                     | Artículo GEN/m2p-labs                       | OTR hasta 0.2 mol/L/h; evita necesidad de control activo de pH                                           | Media-Alta | Recomendada (condición específica de llenado)        |
| E11          | El Sartorius 10 L soporta flujo de gas de hasta 20 lpm (aire, O₂, CO₂, N₂)                                                                              | Explícita         | D04                     | Especificaciones técnicas A\*STAR           | Gas flow: max. total flow rate 20 lpm                                                                    | Alta       | No requerida                                         |
| E12          | La diferencia Sartorius 5 L → 10 L es principalmente de escala volumétrica; la diferencia BioLector XT → Sartorius es cualitativa (principio operativo) | Inferida          | D03, D04, D06, D08, D09 | Múltiples secciones                         | Inferencia a partir de comparación de especificaciones y declaraciones de posicionamiento                | Media      | Requerida                                            |
| E13          | El Biostat B puede operar en modos batch, fed-batch, continuo y perfusión                                                                               | Explícita         | D03                     | Página de producto Sartorius                | "batch, fed-batch, continuous or perfusion mode"                                                         | Alta       | No requerida                                         |
| E14          | El BioLector XT permite gassing con O₂ de 1%–100% y CO₂ de 1%–12%                                                                                       | Explícita         | D01, D02                | Página de producto y press release          | "Gassing with O2 within a range of 1%–100% and with CO2 within 1%–12%"                                   | Alta       | No requerida                                         |

---

## 9. Conceptos ontológicos candidatos

| Concepto candidato        | Tipo sugerido                         | Definición basada en evidencia                                                                                                                                                               | Fuente asociada | Estado    |
| ------------------------- | ------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------- | --------- |
| `BioprocessSystem`        | Clase                                 | Clase raíz que agrupa todos los sistemas instrumentales utilizados en bioprocesos, independientemente de la escala o el principio operativo                                                  | D01, D03        | Candidato |
| `Microbioreactor`         | Subclase de `BioprocessSystem`        | Sistema de bioproceso que opera en escala de microscala (µL a pocos mL), generalmente en formato de placa de microtitulación, con medición en línea no invasiva                              | D01, D06, D12   | Candidato |
| `StirredTankBioreactor`   | Subclase de `BioprocessSystem`        | Sistema de bioproceso que utiliza agitación mecánica por impeller en un recipiente cerrado y controlado; plataforma estándar de desarrollo y producción a escala de laboratorio y superior   | D03, D04, D09   | Candidato |
| `BioLectorXT`             | Individuo de `Microbioreactor`        | Instancia específica de microbiorreactor de placa de alto rendimiento, fabricado por m2p-labs / Beckman Coulter, que opera con FlowerPlates de 48 pocillos y sensores ópticos pre-calibrados | D01, D02, D10   | Candidato |
| `SartoriusBiostatB5L`     | Individuo de `StirredTankBioreactor`  | Instancia del Biostat B de Sartorius configurada con recipiente de 5 L (volumen de trabajo 0.6–5 L), con agitación de 20–1500 rpm                                                            | D03, D04        | Candidato |
| `SartoriusBiostatB10L`    | Individuo de `StirredTankBioreactor`  | Instancia del Biostat B de Sartorius configurada con recipiente de 10 L (volumen de trabajo 1.5–10 L), con agitación de 20–800 rpm                                                           | D03, D04        | Candidato |
| `MicrotiterPlate`         | Clase                                 | Recipiente de cultivo desechable en formato de placa de pocillos (estándar ANSI/SLAS/SBS) utilizado en microbiorreactores de agitación orbital                                               | D01, D08, D12   | Candidato |
| `FlowerPlate`             | Subclase de `MicrotiterPlate`         | Placa de microtitulación con geometría de pocillo en forma de flor, patentada por m2p-labs, que maximiza la transferencia de oxígeno y el mezclado                                           | D06, D08        | Candidato |
| `WorkingVolume`           | Propiedad de dato (datatype property) | Volumen de cultivo efectivo en operación dentro de un sistema de bioproceso; expresado en µL, mL o L según la escala                                                                         | D04, D08, D10   | Candidato |
| `OperatingScale`          | Propiedad de objeto (object property) | Relación que ubica a un sistema de bioproceso dentro del continuo escalar (microscala, escala de banco, escala piloto, escala de producción)                                                 | D06, D08, D09   | Candidato |
| `OpticalSensor`           | Clase                                 | Sensor que utiliza principios fotónicos (backscatter, fluorescencia, absorción) para la medición en línea no invasiva de parámetros de cultivo                                               | D01, D08        | Candidato |
| `ElectrochemicalSensor`   | Clase                                 | Sensor que utiliza principios electroquímicos (potenciométrico, amperométrico) para la medición de pH, pO₂ u otros parámetros en bioprocesos                                                 | D04             | Candidato |
| `ProcessMode`             | Clase                                 | Categoría del modo operativo de un bioproceso: batch, fed-batch, continuo, perfusión                                                                                                         | D03             | Candidato |
| `GassingSystem`           | Clase                                 | Subsistema de control del suministro de gases a un biorreactor (aire, O₂, CO₂, N₂); incluye spargers, mezcladores de gas y MFCs                                                              | D03, D04, D14   | Candidato |
| `HighThroughputScreening` | Concepto auxiliar                     | Función del sistema BioLector XT orientada al tamizaje paralelo masivo de cepas, medios y condiciones de proceso en la fase más temprana del desarrollo                                      | D01, D02, D08   | Candidato |
| `ScaleDownModel`          | Concepto auxiliar                     | Función del Sartorius Biostat B orientada a replicar a pequeña escala las condiciones de biorreactores a gran escala para el desarrollo y caracterización del proceso                        | D04, D05, D09   | Candidato |

---

## 10. Relaciones ontológicas candidatas

| Relación candidata         | Dominio sugerido        | Rango sugerido            | Significado                                                                                  | Evidencia asociada | Estado    |
| -------------------------- | ----------------------- | ------------------------- | -------------------------------------------------------------------------------------------- | ------------------ | --------- |
| `hasWorkingVolume`         | `BioprocessSystem`      | `xsd:decimal` (en mL o L) | Volumen nominal de cultivo en operación                                                      | E02, E03, E04      | Candidato |
| `hasMaxWorkingVolume`      | `BioprocessSystem`      | `xsd:decimal`             | Volumen máximo de trabajo permitido                                                          | D04                | Candidato |
| `hasMinWorkingVolume`      | `BioprocessSystem`      | `xsd:decimal`             | Volumen mínimo de trabajo permitido                                                          | D04                | Candidato |
| `usesAgitationPrinciple`   | `BioprocessSystem`      | `AgitationPrinciple`      | Principio de agitación empleado (orbital vs. impeller)                                       | D06, D09           | Candidato |
| `usesCultureVessel`        | `BioprocessSystem`      | `CultureVessel`           | Recipiente de cultivo utilizado (MTP/FlowerPlate vs. Univessel Glass/SU)                     | D01, D03           | Candidato |
| `hasSensorType`            | `BioprocessSystem`      | `SensorType`              | Tipo de sensor principal empleado para monitoreo en línea                                    | D01, D04           | Candidato |
| `supportsParallelCultures` | `BioprocessSystem`      | `xsd:integer`             | Número de cultivos simultáneos soportados                                                    | D01, D03           | Candidato |
| `isPositionedAt`           | `BioprocessSystem`      | `DevelopmentStage`        | Etapa del pipeline de desarrollo en que se posiciona el sistema                              | D01, D04, D12      | Candidato |
| `isScalableFrom`           | `BioprocessSystem`      | `BioprocessSystem`        | Relación de escalado desde un sistema de menor escala hacia otro de mayor escala             | D07, D08, D09      | Candidato |
| `functionsAs`              | `BioprocessSystem`      | `BioprocessFunction`      | Función principal del sistema (HighThroughputScreening, ScaleDownModel, ProcessOptimization) | D01, D04, D05      | Candidato |
| `hasMaxAgitationSpeed`     | `StirredTankBioreactor` | `xsd:decimal` (en rpm)    | Velocidad máxima de agitación por impeller                                                   | E05                | Candidato |
| `hasGassingSystem`         | `BioprocessSystem`      | `GassingSystem`           | Subsistema de suministro de gases asociado                                                   | D03, D04, E14      | Candidato |
| `manufactureddBy`          | `BioprocessSystem`      | `Organization`            | Fabricante del sistema de bioproceso                                                         | D01, D03           | Candidato |
| `supportsProcessMode`      | `BioprocessSystem`      | `ProcessMode`             | Modos operativos soportados (batch, fed-batch, continuo, perfusión)                          | D03, E13           | Candidato |

---

## 11. Triadas RDF candidatas

```
# T01 – BioLector XT como individuo de la clase Microbioreactor
BioLectorXT  ->  rdf:type  ->  Microbioreactor
Soporte: D01, D02 | Estado: Soportada

# T02 – Sartorius Biostat B 5L como individuo de StirredTankBioreactor
SartoriusBiostatB5L  ->  rdf:type  ->  StirredTankBioreactor
Soporte: D03, D04 | Estado: Soportada

# T03 – Sartorius Biostat B 10L como individuo de StirredTankBioreactor
SartoriusBiostatB10L  ->  rdf:type  ->  StirredTankBioreactor
Soporte: D03, D04 | Estado: Soportada

# T04 – Microbioreactor como subclase de BioprocessSystem
Microbioreactor  ->  rdfs:subClassOf  ->  BioprocessSystem
Soporte: D01, D06 | Estado: Soportada (inferida de la estructura conceptual del dominio)

# T05 – StirredTankBioreactor como subclase de BioprocessSystem
StirredTankBioreactor  ->  rdfs:subClassOf  ->  BioprocessSystem
Soporte: D03, D09 | Estado: Soportada

# T06 – BioLector XT tiene volumen de trabajo de trabajo aproximado de 800–1000 µL por pocillo
BioLectorXT  ->  hasWorkingVolumePerWell  ->  "800-1000 µL"
Soporte: D08 (800 µL), D10 (800 µL), D08 (1 mL) | Estado: Soportada (requiere precisión por modelo de plato)

# T07 – Sartorius Biostat B 5L tiene volumen de trabajo máximo de 5 L
SartoriusBiostatB5L  ->  hasMaxWorkingVolume  ->  "5"
Soporte: D04 | Estado: Soportada

# T08 – Sartorius Biostat B 10L tiene volumen de trabajo máximo de 10 L
SartoriusBiostatB10L  ->  hasMaxWorkingVolume  ->  "10"
Soporte: D04 | Estado: Soportada

# T09 – Sartorius Biostat B 5L tiene volumen de trabajo mínimo de 0.6 L
SartoriusBiostatB5L  ->  hasMinWorkingVolume  ->  "0.6"
Soporte: D04 | Estado: Soportada

# T10 – Sartorius Biostat B 10L tiene volumen de trabajo mínimo de 1.5 L
SartoriusBiostatB10L  ->  hasMinWorkingVolume  ->  "1.5"
Soporte: D04 | Estado: Soportada

# T11 – BioLector XT usa principio de agitación orbital (shaking)
BioLectorXT  ->  usesAgitationPrinciple  ->  OrbitalShaking
Soporte: D06, D08 | Estado: Soportada

# T12 – Sartorius Biostat B usa principio de agitación por impeller mecánico
SartoriusBiostatB5L  ->  usesAgitationPrinciple  ->  MechanicalImpellerAgitation
SartoriusBiostatB10L  ->  usesAgitationPrinciple  ->  MechanicalImpellerAgitation
Soporte: D03, D04, D09 | Estado: Soportada

# T13 – BioLector XT usa sensores ópticos pre-calibrados
BioLectorXT  ->  hasSensorType  ->  OpticalSensor
Soporte: D01, D08 | Estado: Soportada

# T14 – Sartorius Biostat B 10L usa sensores electroquímicos (pH, pO₂)
SartoriusBiostatB10L  ->  hasSensorType  ->  ElectrochemicalSensor
Soporte: D04 | Estado: Soportada

# T15 – BioLector XT soporta 48 cultivos paralelos
BioLectorXT  ->  supportsParallelCultures  ->  "48"
Soporte: D01, D03 | Estado: Soportada

# T16 – Sartorius Biostat B (single) soporta 1 cultivo; en twin, 2
SartoriusBiostatB5L  ->  supportsParallelCultures  ->  "1"
Soporte: D03, D43 | Estado: Soportada

# T17 – BioLector XT funciona como sistema de tamizaje de alto rendimiento
BioLectorXT  ->  functionsAs  ->  HighThroughputScreening
Soporte: D01, D02 | Estado: Soportada

# T18 – Sartorius Biostat B 5L y 10L funcionan como modelo de escala descendente
SartoriusBiostatB5L  ->  functionsAs  ->  ScaleDownModel
SartoriusBiostatB10L  ->  functionsAs  ->  ScaleDownModel
Soporte: D04, D05 | Estado: Soportada

# T19 – BioLector XT es escalable hacia Sartorius 5L (relación de escalado)
BioLectorXT  ->  isScalableFrom  ->  SartoriusBiostatB5L
Soporte: D07, D08, D12 | Estado: Parcialmente soportada (inferida de evidencia general de escalado MTP→STR; requiere validación con datos experimentales propios)

# T20 – Sartorius 5L es escalable hacia Sartorius 10L
SartoriusBiostatB5L  ->  isScalableFrom  ->  SartoriusBiostatB10L
Soporte: D09, D47 | Estado: Parcialmente soportada (relación cuantitativa de escala; requiere validación de criterios específicos de escalado)

# T21 – BioLector XT soporta gasificación con O₂ de 1%–100%
BioLectorXT  ->  hasO2GassingRange  ->  "1-100%"
Soporte: D01, D02 | Estado: Soportada

# T22 – Sartorius Biostat B 10L tiene agitación máxima de 800 rpm
SartoriusBiostatB10L  ->  hasMaxAgitationSpeed  ->  "800"
Soporte: D04 | Estado: Soportada

# T23 – Sartorius Biostat B 5L tiene agitación máxima de 1500 rpm
SartoriusBiostatB5L  ->  hasMaxAgitationSpeed  ->  "1500"
Soporte: D04 | Estado: Soportada

# T24 – BioLector XT es fabricado por Beckman Coulter / m2p-labs
BioLectorXT  ->  manufacturedBy  ->  BeckmanCoulterLifeSciences
Soporte: D01, D02 | Estado: Soportada

# T25 – Sartorius Biostat B es fabricado por Sartorius
SartoriusBiostatB5L  ->  manufacturedBy  ->  Sartorius
SartoriusBiostatB10L  ->  manufacturedBy  ->  Sartorius
Soporte: D03, D04 | Estado: Soportada

# T26 – Sartorius Biostat B soporta modos batch, fed-batch, continuo y perfusión
SartoriusBiostatB5L  ->  supportsProcessMode  ->  FedBatch
SartoriusBiostatB10L  ->  supportsProcessMode  ->  Perfusion
Soporte: D03 | Estado: Soportada

# T27 – BioLector XT usa FlowerPlate como recipiente de cultivo
BioLectorXT  ->  usesCultureVessel  ->  FlowerPlate
Soporte: D01, D06, D08 | Estado: Soportada

# T28 – FlowerPlate es un individuo (o subclase) de MicrotiterPlate
FlowerPlate  ->  rdfs:subClassOf  ->  MicrotiterPlate
Soporte: D06 | Estado: Soportada
```

---

## 12. Sinónimos y variantes terminológicas

| Término principal         | Sinónimos o variantes documentadas                                                                                 | Idioma | Documento de soporte |
| ------------------------- | ------------------------------------------------------------------------------------------------------------------ | ------ | -------------------- |
| `BioLector XT`            | BioLector XT Microbioreactor, BioLector (genérico), BioLector Pro (predecesor), RoboLector (variante automatizada) | EN     | D01, D02, D06        |
| `Microbioreactor`         | MBR, micro-bioreactor, microbiorreactor, microscale bioreactor, high-throughput bioreactor                         | EN/ES  | D01, D06, D08        |
| `Sartorius Biostat B 5L`  | BIOSTAT B 5L, Biostat B 5 liter, Sartorius 5 L bioreactor, Univessel 5 L                                           | EN     | D03, D04             |
| `Sartorius Biostat B 10L` | BIOSTAT B 10L, Biostat B 10 liter, Sartorius 10 L bioreactor, Sartorius 10 (w/MFCS)                                | EN     | D03, D04             |
| `FlowerPlate`             | Flower plate, MTP with flower-shaped wells, FlowerPlate B, FlowerPlate BOH                                         | EN     | D06, D08, D10        |
| `MicrotiterPlate`         | MTP, microtiter plate, microwell plate, SBS plate, ANSI/SLAS plate                                                 | EN     | D01, D08             |
| `StirredTankBioreactor`   | STR, stirred tank reactor, stirred tank fermenter, STF, tanque agitado                                             | EN/ES  | D03, D04, D09        |
| `WorkingVolume`           | Culture volume, fermentation volume, volumen de trabajo, volumen de cultivo                                        | EN/ES  | D04, D08             |
| `OrbitalShaking`          | Shaking agitation, orbital agitation, agitación orbital                                                            | EN/ES  | D06, D08             |
| `ImpellerAgitation`       | Mechanical agitation, turbine agitation, motor-driven agitation                                                    | EN     | D03, D04, D09        |
| `ScaleDownModel`          | Scale-down model, SDM, modelo de escala descendente                                                                | EN/ES  | D04, D05, D09        |
| `HighThroughputScreening` | HTS, high-throughput, tamizaje de alto rendimiento                                                                 | EN/ES  | D01, D02             |
| `DissolvedOxygen`         | DO, pO₂, OD (oxígeno disuelto), dissolved oxygen in liquid phase                                                   | EN/ES  | D01, D04             |

---

## 13. Vacíos, riesgos y decisiones pendientes

### 13.1 Información faltante

- **Volumen exacto por pocillo del BioLector XT**: Los documentos consultados refieren 800 µL y 1 mL en distintos artículos científicos y para distintos modelos de placa (FlowerPlate B vs. FlowerPlate BOH). La página oficial de producto no especifica un único valor numérico de volumen por pocillo. Se requiere el **Technical Data Sheet oficial** del BioLector XT (disponible en `beckman.com` pero con acceso restringido por registro) para confirmar el rango exacto de volumen de trabajo por pocillo para cada tipo de placa.

- **Versión exacta del Biostat B**: Sartorius ofrece al menos dos variantes del Biostat B (modelo B básico y modelo B-DCU con mayor nivel de automatización). No se ha confirmado si los sistemas denominados "Sartorius 5 L" y "Sartorius 10 L" en el proyecto corresponden al Biostat B estándar o al B-DCU. La lista de sensores puede diferir entre versiones.

- **Protocolo de escalado específico entre BioLector XT y Sartorius**: No se encontró documentación que describa explícitamente el criterio de escalado utilizado en el laboratorio del proyecto entre estos tres sistemas específicos. Los documentos científicos disponibles validan el escalado genérico MTP→STR (por kLa o DO como criterio), pero no un protocolo estandarizado para esta combinación particular.

- **Número de modelo exacto (part number)**: Para fines ontológicos de identificación de individuo, se requieren los part numbers del fabricante para los Sartorius 5 L y 10 L específicos del proyecto.

### 13.2 Ambigüedades terminológicas

- "Sartorius 5 L" y "Sartorius 10 L" no son denominaciones oficiales del fabricante; son referencias al tamaño del recipiente dentro de la familia Biostat B. La ontología debe aclarar si estos son el mismo controlador (DCU) con diferentes recipientes (Univessel 5 L / Univessel 10 L) o controladores independientes.

- El término "FlowerPlate" puede referirse a múltiples variantes (FlowerPlate B, BOH, etc.) con diferentes propiedades de transferencia de oxígeno. La ontología debe manejar esta variabilidad.

- "Anaerobic" en el BioLector XT se refiere a condiciones creadas por gassing activo (excluyendo O₂), no a un diseño inherentemente anaeróbico. Esto puede inducir confusión terminológica.

### 13.3 Configuraciones dependientes del equipo

- La velocidad máxima de agitación del Sartorius 5 L (1500 rpm) y 10 L (800 rpm) puede variar según el tipo de impeller instalado y la versión del controlador.

- El sistema de gassing del Biostat B puede configurarse con 2 o 4 MFCs según la versión; esto afecta la representación ontológica del subsistema de gasificación.

- El BioLector XT puede operar con placas de 48 pocillos o con módulo microfluidico de 32 pocillos (32 reactores + 16 reservorios); esta diferencia arquitectural debe ser capturada en la ontología.

### 13.4 Datos que requieren validación con expertos

- Confirmación de que los "Sartorius 5 L" y "Sartorius 10 L" del proyecto son el modelo Biostat B (no Biostat B-DCU, Biostat A o similar).
- Confirmación del tipo de placas FlowerPlate usadas habitualmente con el BioLector XT del laboratorio.
- Criterios de escalado utilizados en la práctica del laboratorio para transferir condiciones entre el BioLector XT y los biorreactores Sartorius.
- Presencia o ausencia de sensores opcionales (redox, turbidez) en los equipos específicos del proyecto.

### 13.5 Documentos adicionales necesarios

1. **Technical Data Sheet oficial de BioLector XT** (`beckman.com`): para volúmenes exactos por pocillo, rango de temperatura, especificaciones de sensores por filtro óptico.
2. **Manual del operador o guía de usuario del Biostat B** (Sartorius, disponible mediante registro): para confirmar la lista completa de sensores, puertos y configuraciones disponibles.
3. **Brochure oficial del Biostat B** (como el PDF identificado en `sartorius.com/download/34576/broch-biostat-b-sbi1513-e-1--data.pdf`): requiere acceso directo para extracción de evidencia.
4. **Protocolo de escalado interno del laboratorio** (SOP): si existe documentación institucional sobre cómo se realiza el escalado entre BioLector XT y los Sartorius en el laboratorio del proyecto.

---

## 14. Registro metodológico para el documento de investigación

La pregunta ALC-03 analiza las diferencias conceptuales entre tres sistemas de bioproceso (BioLector XT, Sartorius Biostat B 5 L y Sartorius Biostat B 10 L) con el objetivo de establecer las bases para su representación ontológica en OWL/RDF. La estrategia de búsqueda combinó la consulta directa de fuentes primarias oficiales de fabricantes (Beckman Coulter / m2p-labs para el BioLector XT; Sartorius para los sistemas Biostat B), registros técnicos institucionales verificables (A\*STAR SEF) y artículos científicos revisados por pares recuperados desde PubMed Central (PMC), Scientific Reports y Genetic Engineering & Biotechnology News (GEN). Los criterios de selección priorizaron fuentes con autoría identificable, trazabilidad documental, fechas de publicación desde 2009 hasta 2026, y contenido con evidencia técnica directamente extraíble (especificaciones numéricas, declaraciones de posicionamiento, principios de operación). Se excluyeron páginas de revendedores sin autoría directa del fabricante cuando no aportaban información adicional verificable. El corpus definitivo incluyó once documentos que permiten establecer con evidencia explícita las siguientes diferencias conceptuales: (1) escala operativa (µL–mL vs. L), (2) principio de agitación (orbital vs. impeller mecánico), (3) capacidad de paralelismo (48 cultivos vs. 1–2 cultivos), (4) tipo de sensores (ópticos pre-calibrados vs. electroquímicos in situ) y (5) función en el pipeline de desarrollo de bioprocesos (tamizaje de alto rendimiento vs. optimización y modelo de escala descendente). A partir de esta evidencia se propusieron quince conceptos ontológicos candidatos (clases, subclases, individuos, propiedades de dato y conceptos auxiliares), catorce relaciones ontológicas candidatas y veintiocho triadas RDF candidatas. Las principales limitaciones incluyen la ausencia del Technical Data Sheet oficial del BioLector XT con el volumen exacto por pocillo según tipo de placa, la ambigüedad sobre la versión exacta del Biostat B utilizada en el proyecto (B vs. B-DCU) y la necesidad de un protocolo interno de escalado que documente la práctica experimental específica del laboratorio. Todos los conceptos, relaciones y triadas deben considerarse candidatos preliminares sujetos a validación por expertos en bioprocesos y en ingeniería ontológica antes de su incorporación definitiva a la ontología.

---

## 15. Estado final

| Parámetro                      | Estado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| ------------------------------ | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Nivel de confianza general** | **Alto** para la diferenciación conceptual cualitativa; **Medio** para valores numéricos específicos de volumen del BioLector XT por pocillo (falta TDS oficial)                                                                                                                                                                                                                                                                                                                                                                                    |
| **Estado de la respuesta**     | **Soportada** en sus dimensiones conceptuales principales; **Parcialmente soportada** en detalles numéricos específicos                                                                                                                                                                                                                                                                                                                                                                                                                             |
| **Estado del corpus**          | **Suficiente** para responder la pregunta conceptual; **Parcial** para especificaciones técnicas exhaustivas que requieren el TDS oficial y el manual del Biostat B                                                                                                                                                                                                                                                                                                                                                                                 |
| **Próxima acción recomendada** | (1) Suministrar el Technical Data Sheet oficial de BioLector XT al sistema para extracción de volúmenes exactos por pocillo y especificaciones de sensores. (2) Confirmar con experto del laboratorio si los Sartorius 5 L y 10 L son modelo Biostat B o Biostat B-DCU. (3) Validar con experto en bioprocesos las triadas de escalado T19–T20 (relaciones `isScalableFrom`) antes de incorporarlas a la ontología. (4) Incorporar los individuos, clases y propiedades candidatas en el editor OWL (Protégé) para revisión de consistencia lógica. |
