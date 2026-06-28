# ALC-02 — Registro de análisis ontológico y evidencia documental

---

## 1. Identificación de la pregunta

- **ID:** ALC-02
- **Nivel metodológico:** Conceptual-definitorio (nivel de clasificación ontológica)
- **Tema:** Criterios mínimos de identidad funcional de un biorreactor frente a un recipiente de cultivo simple
- **Pregunta:** ¿Qué características mínimas debe tener un sistema para ser considerado biorreactor y no solo un recipiente de cultivo?

---

## 2. Propósito de la pregunta

Esta pregunta establece el **umbral de identidad ontológica** del concepto central del proyecto: `Bioreactor`. Sin una definición operativa clara de qué distingue un biorreactor de un simple recipiente de cultivo (matraz Erlenmeyer, placa Petri, tubo de cultivo), no es posible delimitar el alcance de la ontología ni asignar correctamente individuos a clases.

Para el corpus, esta pregunta contribuye a:

- Definir la clase `Bioreactor` con condiciones necesarias y suficientes
- Establecer subclases válidas (microbiorreactor, biorreactor de tanque agitado, etc.)
- Identificar propiedades esenciales (`hasTemperatureControl`, `hasAerationSystem`, `hasSterileBarrier`, etc.)
- Distinguir el BioLector XT, el Sartorius 5 L y el Sartorius 10 L como instancias legítimas de `Bioreactor` y no simplemente de `CultureVessel`

Para la base ontológica preliminar, habilita la articulación de la jerarquía `CultureVessel → Bioreactor → [subclases por escala o tipo]`.

---

## 3. Plan de búsqueda documental

### Información técnica requerida

- Definición formal o técnica de "biorreactor"
- Características físicas y funcionales mínimas: contención estéril, mezcla/agitación, transferencia de masa, monitoreo, control
- Diferencias documentadas entre biorreactor y recipiente de cultivo no instrumentado (matraz, placa)
- Estándares normativos aplicables (ASME BPE, ISO, FDA)
- Especificaciones técnicas de BioLector XT, Sartorius 5 L / 10 L que evidencien el cumplimiento de criterios

### Tipos de documentos necesarios

- Libros de texto de ingeniería de bioprocesos (revisados por pares)
- Estándares industriales vigentes (ASME BPE, ISO)
- Guías regulatorias (FDA, EMA, ICH)
- Fichas técnicas y manuales de fabricante (m2p-labs, Sartorius)
- Artículos científicos revisados por pares (2021–2026) en revistas de bioingeniería

### Repositorios, bases de datos y sitios oficiales sugeridos

- PubMed / PMC (artículos en acceso abierto)
- ScienceDirect / Elsevier (libros y artículos)
- m2p-labs.com (BioLector XT)
- sartorius.com (BIOSTAT A/B)
- ASME.org (BPE-2022/2024)
- FDA.gov (guías regulatorias)
- EMA.europa.eu (guías EMA/ICH)
- Frontiers in Bioengineering and Biotechnology
- Biotechnology & Bioengineering
- Bioprocess and Biosystems Engineering

### Términos de búsqueda

| Español                                             | Inglés                                             |
| --------------------------------------------------- | -------------------------------------------------- |
| biorreactor definición características mínimas      | bioreactor minimum characteristics definition      |
| recipiente de cultivo vs biorreactor                | culture vessel vs bioreactor                       |
| control pH temperatura oxígeno disuelto biorreactor | pH temperature dissolved oxygen bioreactor control |
| transferencia de masa biorreactor                   | mass transfer bioreactor                           |
| biorreactor estéril monitoreo sensores              | bioreactor sterile monitoring sensors              |
| norma ASME BPE equipo bioprocesos                   | ASME BPE bioprocessing equipment standard          |
| biorreactor frente matraz agitado diferencia        | bioreactor vs shake flask difference               |

### Ecuaciones de búsqueda sugeridas

```
("bioreactor" OR "fermenter") AND ("minimum requirements" OR "essential characteristics" OR "definition") AND ("culture vessel" OR "shake flask") [PubMed / Google Scholar]

("bioreactor") AND ("controlled environment" OR "sterile containment") AND ("mass transfer" OR "agitation") AND ("monitoring" OR "sensors") [ScienceDirect]

("BioLector XT" OR "BIOSTAT B") AND ("technical specifications" OR "data sheet") [sitios de fabricante]
```

### Criterios de inclusión y exclusión aplicables

Se aplican los criterios generales del proyecto: preferencia por fuentes 2021–2026, fuentes oficiales de fabricante, artículos revisados por pares y estándares técnicos. Se excluyen blogs sin referencias, contenido comercial sin autoría, y fuentes sin trazabilidad.

---

## 4. Documentos candidatos encontrados

| ID Doc | Título                                                                                                | Entidad autora                                                              |                          Año | Tipo de fuente                                      | URL/DOI verificable                                                                       | Relación con la pregunta                                                         | Decisión preliminar                                                |
| ------ | ----------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------- | ---------------------------: | --------------------------------------------------- | ----------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- | ------------------------------------------------------------------ |
| DOC-01 | Bioreactor – Overview (ScienceDirect Topics)                                                          | Elsevier / múltiples autores compilados                                     |    Continuo (act. 2021–2024) | Revisión compilada en plataforma académica          | https://www.sciencedirect.com/topics/immunology-and-microbiology/bioreactor               | Definición, requisitos, diferencia con recipiente simple                         | Include                                                            |
| DOC-02 | BioLector XT – Product Page / Technical Specifications                                                | m2p-labs GmbH / Beckman Coulter Life Sciences                               |                    2021–2026 | Documentación técnica oficial de fabricante         | https://www.m2p-labs.com/bioreactors/products/biolector-xt/                               | Verificación de características de monitoreo/control del BioLector XT            | Include                                                            |
| DOC-03 | ASME BPE-2022: Bioprocessing Equipment Standard                                                       | American Society of Mechanical Engineers (ASME)                             |                         2022 | Norma técnica internacional                         | https://www.asme.org/codes-standards/find-codes-standards/bpe-bioprocessing-equipment-(1) | Norma de diseño de equipos de bioprocesos; definición de bioprocessing equipment | Include (con reserva: acceso a contenido completo requiere compra) |
| DOC-04 | Bioprocess Engineering Principles, 2nd Ed.                                                            | Doran, P.M. (Elsevier/Academic Press)                                       |                         2012 | Libro de texto científico (revisado por pares)      | https://shop.elsevier.com/books/bioprocess-engineering-principles/doran/978-0-12-220851-5 | Características instrumentales mínimas de biorreactor; diferencia con matraz     | Include                                                            |
| DOC-05 | Time-Resolved Monitoring of OTR of CHO Cells in Shake Flasks                                          | Ihling et al. (Frontiers in Bioengineering)                                 |                         2021 | Artículo científico revisado por pares              | DOI: 10.3389/fbioe.2021.725498                                                            | Diferencia explícita entre matraz y biorreactor instrumentado                    | Include                                                            |
| DOC-06 | BIOSTAT B Specifications – A\*SEF / Sartorius Stedim                                                  | A\*STAR Scientific Equipment & Services Finder (especificaciones Sartorius) | N/D (datos de equipo actual) | Base de datos institucional con ficha técnica       | https://asef.a-star.edu.sg/equipment/bioreactor-sartorius-10-w-mfcs-biostat-b-sifbi       | Verificación de sensores y parámetros del Sartorius 5 L y 10 L                   | Include                                                            |
| DOC-07 | Implementation of Perforated Concentric Ring Walls for Gas-Liquid Mass Transfer of Shaken Bioreactors | Hansen et al. (Frontiers in Bioengineering)                                 |                         2022 | Artículo científico revisado por pares              | DOI: 10.3389/fbioe.2022.894295                                                            | Diferencia entre biorreactor agitado y STR en transferencia de masa y control    | Include                                                            |
| DOC-08 | Fermentation Process and Bioreactor Design: Concepts, Types and Operational Factors                   | Autor(es) no plenamente identificados en extracto de ResearchGate           |                         2025 | Artículo (ResearchGate)                             | https://www.researchgate.net/publication/393879897                                        | Definición de fermenter/biorreactor; características mínimas                     | Uncertain (autor y revista no verificados completamente)           |
| DOC-09 | Editorial: Insights in Bioprocess Engineering 2021/22                                                 | Zinn, M. & Rodrigues, L.R. (Frontiers in Bioengineering)                    |                         2023 | Editorial científica revisada por pares             | DOI: 10.3389/fbioe.2023.1237925                                                           | Contexto de tecnologías de biorreactor en bioingeniería actual                   | Uncertain (relevancia indirecta)                                   |
| DOC-10 | The Different Faces of a Bioreactor                                                                   | HEL Group                                                                   |                         2026 | Contenido técnico-comercial (fabricante de equipos) | https://helgroup.com/blog/biotechnology-blog/the-different-faces-of-a-bioreactor/         | Definición operativa de biorreactor y control de condiciones                     | Uncertain (blog de fabricante, sin referencias)                    |

---

## 5. Evaluación de documentos candidatos

| ID Doc | Relevancia | Autoridad | Trazabilidad | Cobertura de la pregunta | Evidencia localizable        | Justificación                                                                                                                                                                                     |
| ------ | ---------- | --------- | ------------ | ------------------------ | ---------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| DOC-01 | Alta       | Alta      | Alta         | Alta                     | Alta                         | Plataforma académica Elsevier con síntesis de múltiples fuentes revisadas por pares; contiene definiciones operativas y lista de requisitos de biorreactor                                        |
| DOC-02 | Alta       | Alta      | Alta         | Media                    | Alta                         | Documentación oficial del fabricante del BioLector XT; lista explícita de sensores (biomasa, pH, DO), control (temperatura, gaseo) y estrategias de alimentación                                  |
| DOC-03 | Alta       | Muy alta  | Alta         | Media                    | Baja (acceso pago)           | Norma ASME de referencia internacional; verifica la existencia y vigencia del documento, pero el contenido completo requiere adquisición                                                          |
| DOC-04 | Alta       | Muy alta  | Alta         | Alta                     | Alta (fragmentos accesibles) | Texto canónico de bioingeniería; el extracto verificable menciona explícitamente que un biorreactor de banco tiene instrumentos para medir y ajustar temperatura, pH, DO y velocidad de agitación |
| DOC-05 | Alta       | Alta      | Alta         | Alta                     | Alta                         | Artículo de acceso abierto en PMC; distingue explícitamente biorreactor instrumentado de matraz de agitación; cita ausencia de monitoreo en tiempo real como limitación del matraz                |
| DOC-06 | Alta       | Alta      | Media        | Alta                     | Alta                         | Ficha técnica de Sartorius BIOSTAT B en repositorio institucional de A\*STAR; lista de sensores (pH, pO2, temperatura, espuma, nivel, sustrato) y rangos de operación verificables                |
| DOC-07 | Alta       | Alta      | Alta         | Media                    | Alta                         | Artículo revisado por pares en Frontiers; compara cuantitativamente el biorreactor agitado vs STR en transferencia de masa (OTR) y discute la limitación del matraz en control                    |
| DOC-08 | Alta       | Media     | Baja         | Alta                     | Media                        | La definición encontrada es concreta y relevante pero no se pudo verificar revista, volumen ni autor institucional completo; requiere confirmación antes de incorporar al corpus                  |
| DOC-09 | Baja       | Alta      | Alta         | Baja                     | Baja                         | Editorial que provee contexto de tendencias, pero no responde directamente a la pregunta definitoria                                                                                              |
| DOC-10 | Media      | Media     | Baja         | Media                    | Media                        | Contenido de fabricante con fecha reciente (2026); define biorreactor operativamente pero carece de referencias verificables; puede usarse como apoyo no como fuente principal                    |

---

## 6. Corpus documental seleccionado

| ID Doc | Documento seleccionado                                                            | Pregunta asociada | Fragmentos o páginas relevantes                                                                                                                 | Estado               |
| ------ | --------------------------------------------------------------------------------- | ----------------- | ----------------------------------------------------------------------------------------------------------------------------------------------- | -------------------- |
| DOC-01 | Bioreactor – Overview (ScienceDirect Topics, Elsevier)                            | ALC-02            | Sección de definición, sección de requisitos mínimos de biorreactor (requisitos de Panda, 2011, citados en la plataforma)                       | Incluido             |
| DOC-02 | BioLector XT Product Page – m2p-labs / Beckman Coulter                            | ALC-02            | Lista de parámetros medidos (biomasa, pH, DO), parámetros controlados (temperatura, gaseo, alimentación), módulo microfluídico                  | Incluido             |
| DOC-03 | ASME BPE-2022 Standard                                                            | ALC-02            | Sección GR-1 (alcance y definiciones) — requiere compra; se incorpora con evidencia limitada                                                    | Incluido con reserva |
| DOC-04 | Doran, P.M. Bioprocess Engineering Principles, 2nd Ed. (2012)                     | ALC-02            | Capítulo 14 (sección 14.4, Monitoring and Control of Bioreactors); fragmento de escala progresiva (Step 13, texto accesible en repositorio NDL) | Incluido             |
| DOC-05 | Ihling et al. (2021), Frontiers in Bioengineering, DOI: 10.3389/fbioe.2021.725498 | ALC-02            | Abstract y sección Introduction; contraste explícito matraz vs biorreactor instrumentado                                                        | Incluido             |
| DOC-06 | BIOSTAT B Specifications – A\*SEF / Sartorius                                     | ALC-02            | Tabla de especificaciones técnicas: sensores, rangos de agitación, temperatura, volúmenes de trabajo 5 L y 10 L                                 | Incluido             |
| DOC-07 | Hansen et al. (2022), Frontiers in Bioengineering, DOI: 10.3389/fbioe.2022.894295 | ALC-02            | Abstract y sección de comparación de capacidad OTR entre matraz y STR                                                                           | Incluido             |

---

## 7. Respuesta basada en evidencia

### Síntesis de la respuesta

Un sistema puede ser considerado **biorreactor** y no un mero recipiente de cultivo cuando cumple simultáneamente al menos cuatro condiciones funcionales esenciales: **(1) contención estéril activa**, **(2) control activo del ambiente fisicoquímico**, **(3) gestión de transferencia de masa**, y **(4) capacidad de monitoreo en tiempo real de variables críticas del proceso**. Estas condiciones determinan la distinción con un recipiente de cultivo simple (matraz Erlenmeyer, placa de pocillos sin instrucción, tubo de cultivo).

A continuación se detalla cada criterio con soporte de evidencia:

---

#### 7.1 Contención estéril activa

**Evidencia explícita.** El corpus coincide en que el biorreactor es un **recipiente cerrado** capaz de operar en condiciones asépticas (DOC-01, DOC-04, DOC-06). DOC-01 cita que los biorreactores son "recipientes de cultivo diseñados con sistemas de entrada y salida de aire para la producción controlada y estéril de materiales biológicos". DOC-06 especifica que el BIOSTAT B opera entre −1 y +2.5 barg a 150 °C, lo que implica capacidad de esterilización in situ (SIP). DOC-04 identifica la esterilización como un tema propio del capítulo de biorreactores (sección 14.6). Un recipiente de cultivo ordinario (p.ej., matraz con tapón de algodón) solo provee una barrera pasiva y rudimentaria, no un sistema activo de control de esterilidad.

#### 7.2 Control activo del ambiente fisicoquímico

**Evidencia explícita.** DOC-04 (Doran) menciona explícitamente que un biorreactor de banco de escala 1–2 L está "equipado con instrumentos para medir y ajustar temperatura, pH, concentración de oxígeno disuelto y velocidad del agitador y otras variables del proceso". DOC-07 menciona que, a diferencia del matraz agitado, el STR ("stirred tank reactor") permite ajuste controlado de los parámetros. DOC-06 especifica el rango de control de temperatura del BIOSTAT B (0–80 °C). DOC-02 muestra que el BioLector XT ofrece "control de proceso flexible de pH, agitación, temperatura y gaseo". La ausencia de este control activo es el rasgo definitorio que separa al biorreactor del matraz: DOC-05 (Ihling et al.) declara explícitamente que, "en contraste con biorreactores instrumentados, en los matraces de agitación carecen de opciones confiables para el monitoreo no invasivo y en tiempo real del estado del cultivo".

#### 7.3 Gestión de transferencia de masa (aireación y mezcla)

**Evidencia explícita.** DOC-07 cuantifica que los STR alcanzan tasas de transferencia de oxígeno (OTR) de 100–150 mmol/L/h en escala relevante, mientras que los matraces de agitación están limitados por su menor transferencia gaseosa. DOC-01 lista entre los requisitos mínimos de un biorreactor el control de la concentración de oxígeno disuelto, la velocidad de agitación y otros parámetros para crear un "entorno aséptico controlado para los biocatalizadores". DOC-06 indica que el BIOSTAT B dispone de sparger poroso y tipo-L, y flujo de gas (aire, O₂, CO₂, N₂, hasta 20 lpm), lo que garantiza una gestión activa de la transferencia de oxígeno. El BioLector XT (DOC-02) controla activamente la concentración de O₂ o CO₂ del gas entrante hasta ≤ 100 % o ≤ 12 %, respectivamente.

#### 7.4 Monitoreo en tiempo real de variables críticas del proceso

**Evidencia explícita.** DOC-05 (Ihling et al.) fundamenta que la ausencia de monitoreo en tiempo real es una limitación característica del matraz frente al biorreactor. DOC-01 incluye entre los requisitos mínimos que el biorreactor sea "fácil de monitorear y/o controlar parámetros de reacción (como concentración de oxígeno disuelto, pH, temperatura, velocidad de agitación, valor redox, etc.)". DOC-06 lista los sensores del BIOSTAT B: pH, pO₂, temperatura, espuma, nivel y sustrato. DOC-02 enumera las mediciones en línea del BioLector XT: biomasa, fluorescencias, pH y DO, usando sensores ópticos precalibrados.

---

#### 7.5 Características adicionales frecuentemente mencionadas (inferencia razonable)

**Inferencia razonable basada en evidencia.** La literatura revisada sugiere además:

- **Sistema de muestreo aséptico** (para análisis fuera de línea sin comprometer la esterilidad) — mencionado en DOC-01 como elemento típico del sistema.
- **Sistema de control de espuma** — listado en DOC-06 (sensor de espuma) y descrito en DOC-01 como parte del diseño típico.
- **Sistema de alimentación controlada** — DOC-02 y DOC-04 lo citan como distinción de un biorreactor frente al modo batch simple del matraz.

**Información no establecida en el corpus:** No se encontró en los documentos incluidos una norma internacional (como ISO o ASME BPE) que defina formalmente un umbral mínimo cuantitativo unívoco (p.ej., "al menos 3 sensores") que distinga jurídicamente un biorreactor de un recipiente de cultivo. El ASME BPE-2022 (DOC-03) aborda requisitos de diseño de equipo de bioprocesos, pero el acceso al contenido completo no fue posible sin compra. Esta brecha debe cubrirse con validación experta o adquisición del estándar.

---

## 8. Tabla de afirmaciones y evidencia

| ID Ev | Afirmación                                                                                                                                                                           | Tipo de evidencia | Documento              | Página/Sección                                                     | Fragmento o resumen fiel                                                                                                                                                                                                                         | Confianza | Validación experta                                                       |
| ----- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ----------------- | ---------------------- | ------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | --------- | ------------------------------------------------------------------------ |
| EV-01 | Un biorreactor es un recipiente cerrado diseñado con sistemas de entrada/salida de gas para producción controlada y estéril                                                          | Explícita         | DOC-01                 | Overview, párrafo 1                                                | "Bioreactors are culture vessels designed with air inflow and outflow systems for the controlled and sterile production of mass quantities of biological materials."                                                                             | Alta      | No requerida                                                             |
| EV-02 | Un biorreactor de banco de 1–2 L está equipado con instrumentos para medir y ajustar temperatura, pH, DO y velocidad del agitador                                                    | Explícita         | DOC-04                 | Capítulo de bioingeniería de procesos, Step 13 (escala progresiva) | "The first stage may be a 1- or 2-litre bench-top bioreactor equipped with instruments for measuring and adjusting temperature, pH, dissolved oxygen concentration, stirrer speed, and other process variables"                                  | Alta      | No requerida                                                             |
| EV-03 | A diferencia de los biorreactores instrumentados, los matraces de agitación carecen de monitoreo no invasivo en tiempo real del estado del cultivo                                   | Explícita         | DOC-05                 | Abstract (Ihling et al. 2021)                                      | "In contrast to instrumented bioreactors, reliable options for non-invasive, time-resolved monitoring of the culture status in shake flasks are lacking."                                                                                        | Alta      | No requerida                                                             |
| EV-04 | Un biorreactor debe permitir fácilmente monitorear y/o controlar DO, pH, temperatura, velocidad de agitación, redox y otros parámetros para crear un entorno aséptico                | Explícita         | DOC-01                 | Sección de requisitos (Panda, 2011, citado en ScienceDirect)       | "Easy to monitor and/or control reaction parameters (such as dissolved oxygen concentration, pH, temperature, agitation rate, redox value) to create a controlled aseptic environment for biocatalysts."                                         | Alta      | Deseable (el doc original de Panda, 2011 no fue verificado directamente) |
| EV-05 | El BioLector XT mide en línea biomasa, fluorescencias, pH y DO con sensores ópticos precalibrados y controla pH, temperatura y gaseo                                                 | Explícita         | DOC-02                 | Product page m2p-labs                                              | "Disposable 48 well MTPs enable online measurement of biomass, fluorescences, pH and DO, while patented microfluidic technology supports simultaneous pH control and feeding. Flexible process control of pH, shaking, temperature and gassing." | Alta      | No requerida                                                             |
| EV-06 | El BIOSTAT B (Sartorius) dispone de sensores de pH, pO₂, temperatura, espuma, nivel y sustrato, con control de temperatura de 0–80 °C y agitación hasta 1500 rpm (5 L)               | Explícita         | DOC-06                 | Tabla de especificaciones técnicas A\*SEF                          | "Sensors: pH, pO2, Temperature, Foam, Level, Substrate / Temperature control: 0–80 °C / Permitted stirring speed: 5L (20–1500 rpm)"                                                                                                              | Alta      | Recomendable verificar con manual oficial de Sartorius                   |
| EV-07 | Los STR alcanzan OTR de 100–150 mmol/L/h frente a capacidades mucho menores de los matraces de agitación sin control de transferencia gaseosa activa                                 | Explícita         | DOC-07                 | Abstract (Hansen et al. 2022)                                      | "Whereas, in stirred tank reactors OTRs of 100–150 mmol/L/h can be achieved on production relevant scales [...]" vs. limitaciones del matraz                                                                                                     | Alta      | No requerida                                                             |
| EV-08 | ASME BPE-2022 es la norma internacional líder para diseño y fabricación de equipos usados en producción de biofarmacéuticos                                                          | Explícita         | DOC-03                 | Página oficial ASME                                                | "It is the leading Standard on how to design and build equipment and systems used in the production of biopharmaceuticals."                                                                                                                      | Alta      | El contenido normativo completo requiere adquisición del estándar        |
| EV-09 | La contención estéril activa del BIOSTAT B incluye operación hasta 150 °C (esterilización in situ)                                                                                   | Explícita         | DOC-06                 | Tabla técnica A\*SEF                                               | "Culture vessel design: -1 to +2.5 barg @ 150 °C"                                                                                                                                                                                                | Alta      | Confirmar con manual Sartorius BIOSTAT B                                 |
| EV-10 | Los matraces de agitación operan típicamente en modo batch sin control activo de pH ni DO, mientras que los biorreactores usan controladores PID con alimentación fed-batch continua | Inferida          | DOC-04, DOC-05, DOC-07 | Capítulo 14 Doran; Abstract Ihling; Comparativa Hansen             | El corpus contrasta repetidamente "batch sin control activo" (matraz) con "control de lazo cerrado" (biorreactor), sin enunciar explícitamente una definición umbral formal                                                                      | Media     | Requerida para formalizar como criterio ontológico                       |

---

## 9. Conceptos ontológicos candidatos

| Concepto candidato           | Tipo sugerido                                    | Definición basada en evidencia                                                                                                                                                                                                                                                                          | Fuente asociada                | Estado                                  |
| ---------------------------- | ------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------ | --------------------------------------- |
| `Bioreactor`                 | Clase                                            | Sistema fabricado diseñado para soportar un entorno biológicamente activo, que incluye al menos: contención estéril activa, control de variables fisicoquímicas (temperatura, pH, DO, agitación), gestión activa de transferencia de masa y monitoreo en tiempo real de parámetros críticos del proceso | DOC-01, DOC-04, DOC-05, DOC-07 | Candidato — requiere validación experta |
| `CultureVessel`              | Clase (superclase de `Bioreactor`)               | Cualquier recipiente capaz de contener un cultivo biológico, con o sin capacidades de control activo; incluye matraces, placas, tubos y biorreactores                                                                                                                                                   | DOC-05, DOC-07                 | Candidato                               |
| `InstrumentedBioreactor`     | Subclase de `Bioreactor`                         | Biorreactor equipado con sensores en línea para medición de al menos pH, DO y temperatura, y con actuadores de control de bucle cerrado (PID o equivalente)                                                                                                                                             | DOC-04, DOC-05, DOC-06         | Candidato                               |
| `MicroBioreactor`            | Subclase de `Bioreactor`                         | Biorreactor de muy pequeño volumen de trabajo (típicamente < 10 mL) basado en formato de placa de microtitulación o equivalente, con monitoreo óptico en línea                                                                                                                                          | DOC-02                         | Candidato                               |
| `ShakeFlask`                 | Subclase de `CultureVessel` (no de `Bioreactor`) | Recipiente de cultivo no instrumentado para operación en agitador orbital; sin control activo de pH, DO ni temperatura más allá del ambiente del agitador                                                                                                                                               | DOC-05, DOC-07                 | Candidato                               |
| `SterilizationSystem`        | Clase (componente)                               | Sistema que garantiza la contención aséptica del biorreactor, incluyendo esterilización in situ (SIP), filtración de aire de entrada/salida y puertos asépticos                                                                                                                                         | DOC-03, DOC-06                 | Candidato                               |
| `AgitationSystem`            | Clase (componente)                               | Sistema mecánico o pneumático responsable de la mezcla del contenido del biorreactor y la transferencia de masa gas-líquido; incluye impelidor, deflectores (baffles), motor y sparger                                                                                                                  | DOC-01, DOC-04, DOC-07         | Candidato                               |
| `ProcessSensor`              | Clase (componente)                               | Dispositivo que mide una variable del proceso (pH, DO, temperatura, biomasa, espuma, nivel) en tiempo real dentro del biorreactor                                                                                                                                                                       | DOC-02, DOC-06                 | Candidato                               |
| `ProcessActuator`            | Clase (componente)                               | Dispositivo que ejecuta una acción de control sobre una variable del proceso (calentador, bomba de ácido/base, válvula de gas, motor de agitación) en respuesta a una señal del sensor                                                                                                                  | DOC-02, DOC-06                 | Candidato                               |
| `ControlLoop`                | Clase (proceso)                                  | Bucle de control de proceso que vincula un sensor con un actuador para mantener una variable dentro de un rango de consigna (setpoint)                                                                                                                                                                  | DOC-04, DOC-05                 | Candidato                               |
| `OxygenTransferRate` (`OTR`) | Propiedad de dato                                | Tasa volumétrica de transferencia de oxígeno del gas al líquido (mmol/L/h), parámetro de ingeniería que distingue biorreactores de matraces en capacidad de suministro de O₂                                                                                                                            | DOC-07                         | Candidato                               |
| `WorkingVolume`              | Propiedad de dato                                | Volumen operativo del cultivo dentro del biorreactor (expresado en litros o mililitros), que lo clasifica en escala (micro, bench, piloto, producción)                                                                                                                                                  | DOC-06                         | Candidato                               |

---

## 10. Relaciones ontológicas candidatas

| Relación candidata       | Dominio sugerido         | Rango sugerido                                                               | Significado                                                                                     | Evidencia asociada         | Estado                                                |
| ------------------------ | ------------------------ | ---------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- | -------------------------- | ----------------------------------------------------- |
| `hasComponent`           | `Bioreactor`             | `AgitationSystem`, `SterilizationSystem`, `ProcessSensor`, `ProcessActuator` | Un biorreactor tiene componentes funcionales mínimos que lo diferencian de un recipiente simple | EV-01, EV-02, EV-05, EV-06 | Candidato                                             |
| `hasSensor`              | `Bioreactor`             | `ProcessSensor`                                                              | Un biorreactor tiene al menos un sensor de proceso en línea                                     | EV-05, EV-06               | Candidato                                             |
| `hasActuator`            | `Bioreactor`             | `ProcessActuator`                                                            | Un biorreactor tiene al menos un actuador de control                                            | EV-02, EV-05               | Candidato                                             |
| `monitorsVariable`       | `ProcessSensor`          | `ProcessVariable` (pH, DO, temperatura, etc.)                                | Un sensor mide una variable de proceso específica                                               | EV-05, EV-06               | Candidato                                             |
| `controlsVariable`       | `ControlLoop`            | `ProcessVariable`                                                            | Un bucle de control actúa sobre una variable de proceso                                         | EV-02, EV-04               | Candidato                                             |
| `isSubclassOf`           | `InstrumentedBioreactor` | `Bioreactor`                                                                 | El biorreactor instrumentado es una subclase específica de biorreactor                          | EV-02, EV-03               | Candidato                                             |
| `isDistinguishedFrom`    | `Bioreactor`             | `CultureVessel` (no instrumentado)                                           | Relación de distinción funcional basada en capacidades de monitoreo y control activo            | EV-03, EV-07               | Candidato (relación de diferenciación, no jerárquica) |
| `achievesOxygenTransfer` | `AgitationSystem`        | `OxygenTransferRate`                                                         | El sistema de agitación determina la OTR del biorreactor                                        | EV-07                      | Candidato                                             |
| `hasWorkingVolume`       | `Bioreactor`             | `WorkingVolume` (dato numérico con unidad)                                   | El biorreactor opera dentro de un rango de volúmenes definido                                   | EV-06                      | Candidato                                             |
| `enablesSterilization`   | `SterilizationSystem`    | `AsepticCondition`                                                           | El sistema de esterilización mantiene condiciones asépticas durante el proceso                  | EV-01, EV-09               | Candidato                                             |

---

## 11. Triadas RDF candidatas

```
# EV-01 / EV-04
:Bioreactor  rdf:type  owl:Class
:Bioreactor  rdfs:subClassOf  :CultureVessel
:Bioreactor  rdfs:comment  "A closed system that supports a biologically active environment through active control of physicochemical variables and aseptic containment"
→ Soportada / DOC-01, DOC-04

# EV-02
:BenchTopBioreactor  :hasSensor  :TemperatureSensor
:BenchTopBioreactor  :hasSensor  :pHSensor
:BenchTopBioreactor  :hasSensor  :DissolvedOxygenSensor
:BenchTopBioreactor  :hasSensor  :AgitationSpeedSensor
→ Soportada / DOC-04 (Doran, cap. 14)

# EV-03
:ShakeFlask  rdfs:subClassOf  :CultureVessel
:ShakeFlask  :lacksCapability  :RealTimeProcessMonitoring
:Bioreactor  :hasCapability  :RealTimeProcessMonitoring
→ Soportada / DOC-05 (Ihling et al. 2021)

# EV-05
:BioLectorXT  rdf:type  :MicroBioreactor
:BioLectorXT  :hasSensor  :BiomassSensor
:BioLectorXT  :hasSensor  :FluorescenceSensor
:BioLectorXT  :hasSensor  :pHSensor
:BioLectorXT  :hasSensor  :DissolvedOxygenSensor
:BioLectorXT  :hasActuator  :TemperatureController
:BioLectorXT  :hasActuator  :GasController
:BioLectorXT  :hasActuator  :FeedingPump
→ Soportada / DOC-02

# EV-06
:SartoriusBIOSTATB_5L  rdf:type  :StirredTankBioreactor
:SartoriusBIOSTATB_5L  :hasWorkingVolume  "0.6-5"^^xsd:string  # en litros
:SartoriusBIOSTATB_5L  :hasSensor  :pHSensor
:SartoriusBIOSTATB_5L  :hasSensor  :pO2Sensor
:SartoriusBIOSTATB_5L  :hasSensor  :TemperatureSensor
:SartoriusBIOSTATB_5L  :hasSensor  :FoamSensor
:SartoriusBIOSTATB_5L  :hasSensor  :LevelSensor
:SartoriusBIOSTATB_5L  :hasSensor  :SubstrateSensor
:SartoriusBIOSTATB_5L  :hasAgitationRange  "20-1500"^^xsd:string  # rpm
:SartoriusBIOSTATB_5L  :hasTemperatureControlRange  "0-80"^^xsd:string  # °C
→ Soportada / DOC-06

:SartoriusBIOSTATB_10L  rdf:type  :StirredTankBioreactor
:SartoriusBIOSTATB_10L  :hasWorkingVolume  "1.5-10"^^xsd:string  # en litros
:SartoriusBIOSTATB_10L  :hasAgitationRange  "20-800"^^xsd:string  # rpm
→ Soportada / DOC-06

# EV-07
:StirredTankBioreactor  :achievesOxygenTransfer  :HighOTR
:HighOTR  :hasTypicalRange  "100-150 mmol/L/h"^^xsd:string
:ShakeFlask  :achievesOxygenTransfer  :LowOTR
→ Soportada / DOC-07 (Hansen et al. 2022)

# EV-09
:SartoriusBIOSTATB  :enablesSterilization  :SteamSterilizationInPlace
:SteamSterilizationInPlace  :operatesAt  "150 °C"^^xsd:string
→ Soportada / DOC-06

# Triada de distinción funcional (criterio definitorio)
:Bioreactor  :requiresCapability  :ActiveProcessControl
:ActiveProcessControl  :includes  :TemperatureControl
:ActiveProcessControl  :includes  :pHControl
:ActiveProcessControl  :includes  :DissolvedOxygenControl
:ActiveProcessControl  :includes  :AgitationControl
→ Parcialmente soportada / DOC-01, DOC-04, DOC-05 / Requiere validación experta para formalizar umbral
```

---

## 12. Sinónimos y variantes terminológicas

| Término principal             | Sinónimos o variantes documentadas                                                       | Idioma | Documento de soporte                               |
| ----------------------------- | ---------------------------------------------------------------------------------------- | ------ | -------------------------------------------------- |
| Bioreactor                    | Fermentor / Fermenter / Bioreaction vessel / Bioprocessing vessel / Bioprocess container | EN     | DOC-01, DOC-07, DOC-08                             |
| Biorreactor                   | Fermentador / Reactor biológico / Recipiente de bioproceso                               | ES     | DOC-08                                             |
| Dissolved oxygen (DO)         | Dissolved O₂ / pO₂ / Oxígeno disuelto / DO saturation                                    | EN/ES  | DOC-02, DOC-05, DOC-06                             |
| Stirred tank bioreactor       | STR / CSTR (if continuous) / Tanque agitado / Reactor de tanque agitado                  | EN/ES  | DOC-07, DOC-06                                     |
| Shake flask                   | Erlenmeyer flask / Shaker flask / Matraz de agitación / Matraz Erlenmeyer                | EN/ES  | DOC-05, DOC-07                                     |
| Oxygen transfer rate          | OTR / Tasa de transferencia de oxígeno / Volumetric oxygen transfer rate                 | EN/ES  | DOC-07                                             |
| In situ sterilization         | SIP / Steam-in-Place / Esterilización in situ                                            | EN/ES  | DOC-03, DOC-06 (inferida del rango de temperatura) |
| Process analytical technology | PAT / Tecnología analítica de proceso                                                    | EN/ES  | DOC-01, DOC-09                                     |
| MicroBioreactor               | Miniaturized bioreactor / High-throughput bioreactor / Microbioreactor de placa          | EN     | DOC-02                                             |

---

## 13. Vacíos, riesgos y decisiones pendientes

### Información faltante

1. **Contenido completo de ASME BPE-2022 (DOC-03):** No fue posible acceder al texto de la norma sin adquirirla. La norma podría contener una definición formal de "bioproceessing vessel" o criterios de clasificación que enriquecerían considerablemente la base ontológica.
2. **Manual oficial de Sartorius BIOSTAT A/B para 5 L y 10 L:** La información de DOC-06 proviene de una base de datos institucional secundaria (A\*SEF), no del manual oficial de Sartorius. Debe verificarse directamente con la documentación de Sartorius (accesible en sartorius.com bajo solicitud o descarga directa).
3. **Hoja técnica oficial del BioLector XT:** DOC-02 es la página del fabricante; la "Technical Data Sheet" referenciada en la misma no fue accedida en texto completo.
4. **Definición regulatoria FDA/EMA de biorreactor:** No se encontró un documento de FDA o EMA que defina formalmente el término "bioreactor" en el contexto de la presente búsqueda; solo ICH Q10 y Q8 abordan el control del proceso, no la clasificación del equipo. Se recomienda buscar en CFR 21 Part 600 y en las EMA CHMP Biotech guidelines.

### Ambigüedades terminológicas

- El término **"fermenter"** y **"bioreactor"** se usan indistintamente en muchas fuentes (DOC-01, DOC-08), pero en contextos de cultivo celular animal se prefiere "bioreactor"; en fermentación microbiana se usa más "fermenter". La ontología debe contemplar esta distinción o tratar ambos como sinónimos dentro de la misma clase.
- El **BioLector XT** funciona en formato de placa de microtitulación (48 pocillos, 800–2400 µL por pocillo), lo que genera ambigüedad sobre si debe clasificarse como `Bioreactor` o como `HighThroughputCultureSystem`. La evidencia (DOC-02) lo denomina explícitamente "microbioreactor", pero su naturaleza es híbrida.

### Configuraciones dependientes del equipo

- Los rangos de volumen de trabajo, agitación y temperatura son específicos de cada modelo de BIOSTAT B (2 L, 5 L, 10 L). Las triadas RDF deben individualizarse por escala, no generalizarse.
- El BioLector XT tiene módulos opcionales (microfluídico, cámara anaeróbica, gasificación O₂/CO₂); los atributos de control de pH y alimentación son **opcionales** en la configuración base.

### Datos que requieren validación con expertos

- La definición funcional del "umbral mínimo" de biorreactor no ha sido establecida formalmente en ninguna norma que el corpus permita verificar completamente. La frontera entre un matraz con control de temperatura externo y un biorreactor es un área de gradación que requiere criterio experto.
- La clasificación del BioLector XT como `MicroBioreactor` (subclase de `Bioreactor`) debe confirmarse con el grupo de investigación, dado su formato no convencional.

### Documentos adicionales necesarios

- Manual técnico oficial Sartorius BIOSTAT B / BIOSTAT A (descargable desde sartorius.com)
- Ficha técnica oficial BioLector XT (m2p-labs / Beckman Coulter — "Technical Data Sheet")
- ASME BPE-2022 (adquirir vía ASME.org o biblioteca institucional)
- Texto completo de Doran (2012), Capítulo 14 (acceso a través de biblioteca)
- Guía EMA sobre sistemas de bioreactores para productos biológicos (CHMP/BWP)
- Definición de biorreactor en 21 CFR (FDA Code of Federal Regulations)

---

## 14. Registro metodológico para el documento de investigación

La pregunta ALC-02 indaga sobre las **características mínimas que distinguen un biorreactor de un simple recipiente de cultivo**, un criterio esencial para definir la clase nuclear `Bioreactor` en la ontología OWL/RDF del proyecto. La estrategia de búsqueda combinó consultas en plataformas académicas (ScienceDirect, PubMed/PMC), repositorios de acceso abierto (Frontiers in Bioengineering and Biotechnology), sitios oficiales de fabricantes (m2p-labs/Beckman Coulter, Sartorius) y bases de datos normativas (ASME). Los criterios de selección priorizaron fuentes del período 2021–2026, documentación oficial de fabricante, artículos revisados por pares y estándares técnicos verificables.

El corpus definitivo comprende siete documentos: la compilación ScienceDirect Topics sobre biorreactores (DOC-01); la página técnica oficial del BioLector XT de m2p-labs/Beckman Coulter (DOC-02); la norma ASME BPE-2022 (DOC-03, incorporada con acceso parcial al contenido); el texto canónico de Doran sobre ingeniería de bioprocesos (DOC-04); el artículo de Ihling et al. (2021) sobre monitoreo en matraces de agitación (DOC-05); las especificaciones del BIOSTAT B de Sartorius obtenidas del repositorio A\*SEF (DOC-06); y el artículo de Hansen et al. (2022) sobre transferencia de masa en sistemas agitados (DOC-07).

La evidencia extraída sustenta cuatro características mínimas: (i) **contención estéril activa**, que diferencia el recipiente cerrado y esterilizable del matraz con cierre pasivo; (ii) **control activo de variables fisicoquímicas** (temperatura, pH, oxígeno disuelto, agitación), ausente en sistemas no instrumentados; (iii) **gestión de transferencia de masa** mediante aireación activa (sparger, control de flujo gaseoso) y agitación mecánica o pneumática, con tasas de OTR cuantitativamente superiores a las del matraz; y (iv) **monitoreo en tiempo real de parámetros críticos** mediante sensores integrados en línea.

Los conceptos ontológicos preliminares identificados incluyen las clases `Bioreactor`, `CultureVessel`, `ShakeFlask`, `MicroBioreactor`, `StirredTankBioreactor`, `SterilizationSystem`, `AgitationSystem`, `ProcessSensor`, `ProcessActuator` y `ControlLoop`, junto con las propiedades `hasComponent`, `hasSensor`, `hasActuator`, `monitorsVariable`, `controlsVariable` y `hasWorkingVolume`. Todos estos candidatos deben considerarse preliminares hasta su validación por el equipo de investigación y de ontología.

Las limitaciones principales comprenden: el acceso restringido al texto completo de ASME BPE-2022; la ausencia de manuales oficiales de Sartorius y del BioLector XT en el corpus; la falta de una definición regulatoria formal (FDA/EMA) del término "biorreactor" en los documentos consultados; y la ambigüedad sobre el umbral funcional entre recipientes instrumentados parcialmente y biorreactores plenos. Estas brechas requieren adquisición de documentos normativos adicionales y validación experta antes de formalizar las clases y relaciones como parte de la ontología.

---

## 15. Estado final

| Criterio                       | Estado                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| ------------------------------ | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Nivel de confianza general** | **Medio-Alto** — la evidencia sobre los criterios esenciales es consistente y multifuente, pero la ausencia del texto completo de ASME BPE-2022 y de los manuales oficiales de Sartorius y BioLector XT limita la precisión técnica                                                                                                                                                                                                      |
| **Estado de la respuesta**     | **Parcialmente soportada** — los cuatro criterios mínimos identificados (contención estéril, control activo de variables, gestión de transferencia de masa, monitoreo en tiempo real) están respaldados por evidencia convergente, pero no existe en el corpus una definición formal y normativa unificada que establezca un umbral mínimo inequívoco                                                                                    |
| **Estado del corpus**          | **Parcial** — el corpus cubre la pregunta con suficiencia para la fase preliminar de la ontología, pero requiere incorporar ASME BPE-2022, manuales oficiales de Sartorius y documentación FDA/EMA antes de la formalización definitiva                                                                                                                                                                                                  |
| **Próxima acción recomendada** | (1) Adquirir ASME BPE-2022 (sección GR-1, Definitions) y manuales oficiales de Sartorius BIOSTAT B 5 L y 10 L; (2) Descargar la Technical Data Sheet del BioLector XT; (3) Revisar FDA 21 CFR y EMA CHMP BWP guidelines en busca de definición regulatoria de biorreactor; (4) Someter los cuatro criterios identificados a revisión del experto en bioprocesos del equipo antes de formalizar la clase `Bioreactor` en la ontología OWL |
