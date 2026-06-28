# ALC-07: ¿Qué relaciones básicas debe tener cada biorreactor con sensores, actuadores, variables operativas, fases del proceso y eventos?

---

## 1. Identificación de la pregunta

| Campo                  | Valor                                                                                                                            |
| ---------------------- | -------------------------------------------------------------------------------------------------------------------------------- |
| **ID**                 | ALC-07                                                                                                                           |
| **Nivel metodológico** | Estructural / Relacional                                                                                                         |
| **Tema**               | Arquitectura ontológica de biorreactores: sensores, actuadores, variables, fases y eventos                                       |
| **Pregunta**           | ¿Qué relaciones básicas debe tener cada biorreactor con sensores, actuadores, variables operativas, fases del proceso y eventos? |

---

## 2. Propósito de la pregunta

Esta pregunta busca establecer el **esqueleto relacional** de la ontología: cómo cada biorreactor (BioLector XT, Sartorius 5 L, Sartorius 10 L) se conecta con sus componentes funcionales. No se trata de describir los valores de los parámetros, sino de identificar qué **tipos de relaciones** existen entre las entidades: cuáles sensores _pertenecen a_ qué biorreactor, cuáles actuadores _regulan_ cuáles variables, qué variables _caracterizan_ cuáles fases, y qué eventos _ocurren durante_ cuáles fases. Esta estructura es el núcleo del grafo ontológico y determina qué inferencias serán posibles.

---

## 3. Plan de búsqueda documental

**Información técnica requerida:**

- Listado de sensores, actuadores e instrumentos por modelo de biorreactor
- Variables operativas medidas y controladas (pH, DO, temperatura, agitación, flujo gaseoso, biomasa, espuma, nivel)
- Fases del proceso de cultivo (esterilización, inoculación, lag, exponencial, estacionaria, cosecha)
- Tipos de eventos, alarmas y decisiones de proceso
- Patrones ontológicos de relación sensor–observación–variable (SSN/SOSA)

**Tipos de documentos necesarios:**

- Manuales técnicos y fichas de fabricante (Beckman Coulter/m2p-labs para BioLector XT; Sartorius para BIOSTAT B/B-DCU)
- Artículos de revisión de bioprocesos
- Especificaciones de ontologías W3C SSN/SOSA
- Publicaciones científicas sobre representación semántica de biorreactores

**Repositorios y sitios sugeridos:**

- `beckman.com`, `sartorius.com` — documentación oficial de fabricante
- `w3.org/TR/vocab-ssn/` — W3C SSN/SOSA
- `PubMed`, `ScienceDirect`, `arXiv` — artículos científicos
- `manualslib.com` — manuales técnicos

**Términos de búsqueda:**

| Español                                    | Inglés                                            |
| ------------------------------------------ | ------------------------------------------------- |
| Biorreactor sensores actuadores relaciones | Bioreactor sensors actuators relations OWL        |
| Ontología bioproceso OWL fases proceso     | Bioprocess ontology phases events RDF             |
| Variables operativas biorreactor control   | Bioreactor operating variables process control    |
| SSN SOSA ontología sensor actuador         | SSN SOSA sensor actuator ontology                 |
| BioLector XT especificaciones sensores     | BioLector XT sensors specifications               |
| Sartorius BIOSTAT B actuadores variables   | Sartorius BIOSTAT B actuators operating variables |

**Ecuaciones de búsqueda:**

- `("BioLector XT") AND (sensor OR actuator OR "dissolved oxygen" OR pH OR biomass)`
- `("Sartorius" OR "BIOSTAT B") AND (sensor OR actuator OR "process variable") AND (5L OR 10L)`
- `(bioreactor ontology) AND (OWL OR RDF OR SSN OR SOSA) AND (sensor OR process phase)`

---

## 4. Documentos candidatos encontrados

| ID doc | Título                                                                         | Entidad autora                       | Año               | Tipo de fuente                         | URL/DOI verificable                                                                 | Relación con la pregunta                                           | Decisión preliminar |
| ------ | ------------------------------------------------------------------------------ | ------------------------------------ | ----------------- | -------------------------------------- | ----------------------------------------------------------------------------------- | ------------------------------------------------------------------ | ------------------- |
| D01    | BioLector XT — Página oficial de producto y módulos                            | Beckman Coulter / m2p-labs           | 2021–2024         | Ficha oficial de fabricante            | `beckman.com/microbioreactor/biolector-xt` y `/modules`                             | Sensores, módulos, actuadores y variables del BioLector XT         | Include             |
| D02    | Beckman Coulter BioLector XT — Manual (ManualsLib)                             | Beckman Coulter                      | 2021              | Manual técnico oficial                 | `manualslib.com/manual/2169370/Beckman-Coulter-Biolector-Xt.html`                   | Principios de operación, sensores, riesgos de proceso              | Include             |
| D03    | BioLector XT — Brochure técnico (PDF)                                          | m2p-labs / Beckman Coulter           | 2021              | Ficha técnica oficial                  | `dafratec.com/storage/file/BioLector-XT-Microbioreactor-Brochure-2021.pdf`          | Especificaciones técnicas del sistema                              | Uncertain           |
| D04    | Biostat® B — Página oficial Sartorius                                          | Sartorius                            | 2023–2025         | Página oficial de fabricante           | `sartorius.com/en/products/fermentation-bioreactors/benchtop-bioreactors/biostat-b` | Actuadores, modos de proceso, control DO, temperatura              | Include             |
| D05    | Biostat® B-DCU — Página oficial Sartorius                                      | Sartorius                            | 2023–2025         | Página oficial de fabricante           | `sartorius.com/en/products/.../biostat-b-dcu`                                       | Integración con software supervisorio, variables de proceso        | Include             |
| D06    | Bioreactor: Sartorius 10 (w/MFCS) — A\*STAR ASEF                               | A\*STAR (Singapore)                  | Sin año explícito | Registro institucional de equipamiento | `asef.a-star.edu.sg/equipment/bioreactor-sartorius-10...`                           | Especificaciones técnicas 5L/10L: sensores, rangos, gases          | Include             |
| D07    | W3C SSN/SOSA Ontology (2017, rev. 2024)                                        | W3C / OGC                            | 2017/2024         | Estándar técnico internacional         | `w3.org/TR/vocab-ssn/`                                                              | Modelo semántico canónico para sensor–observación–actuador         | Include             |
| D08    | SOSA: A Lightweight Ontology for Sensors, Observations, Samples, and Actuators | Haller et al.                        | 2018              | Artículo científico (arXiv)            | `arxiv.org/pdf/1805.09979`                                                          | Clases y relaciones para actuadores y observaciones                | Include             |
| D09    | Bioreactors and Fermentors — Eppendorf White Paper No. 21                      | Eppendorf                            | Sin año explícito | White paper técnico de fabricante      | `eppendorf.com/product-media/doc/en/806599/...`                                     | Fases de crecimiento, eventos de bioproceso, modos batch/fed-batch | Include             |
| D10    | Deep dive: Fermentation upstream bioprocess design                             | Good Food Institute                  | 2025              | Documento técnico institucional        | `gfi.org/science/the-science-of-fermentation/...`                                   | Fases de proceso: preparación, inoculación, cultivo, cosecha       | Include             |
| D11    | Bioreactors in Bioprocessing and How They Work                                 | IKA                                  | Sin año explícito | Documentación técnica de fabricante    | `ika.com/en/Knowledge-Center/.../Bioreactors-in-Bioprocessing...`                   | Fases operativas: esterilización, inoculación, cultivo, cosecha    | Include             |
| D12    | Hands‐free from inoculation to harvest (Sanofi/Reid et al.)                    | Reid et al. / Biotechnology Progress | 2025              | Artículo científico revisado por pares | DOI: `10.1002/btpr.70055`                                                           | Fases batch, fed-batch, inducción; variables DO, pH, temperatura   | Include             |

---

## 5. Evaluación de documentos candidatos

| ID doc | Relevancia | Autoridad | Trazabilidad | Cobertura de la pregunta                                                                  | Evidencia localizable | Justificación                                                                                                    |
| ------ | ---------- | --------- | ------------ | ----------------------------------------------------------------------------------------- | --------------------- | ---------------------------------------------------------------------------------------------------------------- |
| D01    | Alta       | Alta      | Alta         | Alta — lista sensores, actuadores y módulos por nombre                                    | Alta                  | Fuente oficial del fabricante; detalla sensores ópticos, módulos de control de gas, control de pH y alimentación |
| D02    | Alta       | Alta      | Alta         | Media — trata riesgos y configuración pero no presenta listado exhaustivo de relaciones   | Media                 | Manual oficial; accesible en ManualsLib; confirma sensores DO, pH y flujo de gas                                 |
| D03    | Media      | Alta      | Media        | Media                                                                                     | Media                 | PDF de brochure: accesible pero contenido no completamente verificable sin descarga directa                      |
| D04    | Alta       | Alta      | Alta         | Alta — describe modos de proceso, actuadores (bombas, MFC), DO cascade, temperatura       | Alta                  | Página oficial Sartorius; confirma arquitectura de control y actuadores del BIOSTAT B                            |
| D05    | Media      | Alta      | Alta         | Media                                                                                     | Media                 | Complementa D04; agrega integración con supervisorio (Biobrain®, DeltaV™)                                        |
| D06    | Alta       | Alta      | Alta         | Alta — especifica sensores, gases, rangos de velocidad y temperatura por volumen          | Alta                  | Registro institucional A\*STAR con especificaciones BIOSTAT B 5L y 10L verificables                              |
| D07    | Alta       | Muy Alta  | Alta         | Alta — define clases Sensor, Actuator, Observation, FeatureOfInterest, ObservableProperty | Alta                  | Estándar W3C canónico para modelado semántico de sensores y actuadores                                           |
| D08    | Alta       | Alta      | Alta         | Alta — define Actuation, Actuator, Result, Procedure en analogía con Observation          | Alta                  | Artículo fundacional de SOSA; disponible en arXiv                                                                |
| D09    | Alta       | Alta      | Alta         | Alta — describe las cuatro fases de crecimiento y eventos típicos de un bioproceso        | Alta                  | White paper técnico Eppendorf; presenta "series of events in a typical bioprocess run"                           |
| D10    | Media      | Alta      | Alta         | Media — describe fases upstream/downstream y seed train                                   | Media                 | Fuente institucional GFI con referencias; útil para fases de proceso a nivel sistémico                           |
| D11    | Alta       | Alta      | Alta         | Alta — describe pasos operativos: esterilización, inoculación, cultivo, cosecha           | Alta                  | Documentación técnica IKA con autores identificados (Klapan et al.)                                              |
| D12    | Alta       | Alta      | Alta         | Alta — articula fases batch, fed-batch, inducción; vincula variables a fases              | Alta                  | Artículo revisado por pares (2025), Biotechnology Progress; DOI verificable                                      |

---

## 6. Corpus documental seleccionado

| ID doc | Documento seleccionado                                    | Pregunta asociada | Fragmentos o páginas relevantes                                                                                                                 | Estado   |
| ------ | --------------------------------------------------------- | ----------------- | ----------------------------------------------------------------------------------------------------------------------------------------------- | -------- |
| D01    | BioLector XT — Página oficial + módulos (Beckman Coulter) | ALC-07            | Descripción de sensores ópticos (biomasa, pH, DO, fluorescencia), módulos de gas (O₂ up/down, CO₂), módulo microfluidico de pH y alimentación   | Incluido |
| D02    | BioLector XT Manual — ManualsLib (Beckman Coulter)        | ALC-07            | System Configuration p.8; riesgos de flujo de gas, optodes, lecturas pH/DO                                                                      | Incluido |
| D04    | Biostat® B — Sartorius (página oficial)                   | ALC-07            | Sección DO cascade, gravimetric feed control, batch/fed-batch/continuous/perfusion modes, MFC                                                   | Incluido |
| D05    | Biostat® B-DCU — Sartorius (página oficial)               | ALC-07            | Integración con Biobrain®/DeltaV™, módulos de control de temperatura y aireación                                                                | Incluido |
| D06    | Bioreactor Sartorius 10 w/MFCS — A\*STAR ASEF             | ALC-07            | Tabla de especificaciones: sensores (pH, pO₂, temperatura, espuma, nivel, sustrato), gases (aire, O₂, CO₂, N₂), rangos de agitación por volumen | Incluido |
| D07    | W3C SSN/SOSA Ontology (W3C/OGC)                           | ALC-07            | Clases Sensor, Actuator, Observation, Actuation, FeatureOfInterest, ObservableProperty, Result                                                  | Incluido |
| D08    | SOSA: A Lightweight Ontology… (Haller et al., 2018)       | ALC-07            | Sección 2.4 Actuators and Actuations; analogía observación–actuación                                                                            | Incluido |
| D09    | Eppendorf White Paper No. 21 — Bioreactors and Fermentors | ALC-07            | Cuatro fases de crecimiento (lag, exponencial, estacionaria, muerte); Figure 3: series of events in typical bioprocess run                      | Incluido |
| D11    | IKA — Bioreactors in Bioprocessing (Klapan et al.)        | ALC-07            | Pasos 1–4: esterilización, inoculación, cultivo (batch/fed-batch/continuo), cosecha                                                             | Incluido |
| D12    | Reid et al. 2025 — Hands-free inoculation to harvest      | ALC-07            | Fases batch → fed-batch → inducción; variables DO, pH, temperatura vinculadas a fases                                                           | Incluido |

---

## 7. Respuesta basada en evidencia

### 7.1 Relaciones entre biorreactores y sensores

**Evidencia explícita (BioLector XT):** El BioLector XT opera con sensores ópticos pre-calibrados en línea. Las MTPs desechables de 48 pocillos permiten la medición en línea de biomasa, fluorescencias, pH y oxígeno disuelto (DO). Además, el sistema puede equiparse con un módulo de regulación de O₂ que incluye un sensor de oxígeno dentro de la cámara de cultivo que mide continuamente el nivel de O₂ y regula automáticamente el flujo de nitrógeno u oxígeno al interior de la cámara.

**Evidencia explícita (Sartorius 5L/10L):** El sistema BIOSTAT B está equipado con sensores de pH, pO₂, temperatura, espuma, nivel y sustrato, y admite flujo de gas con aire, O₂, CO₂ y N₂ hasta un caudal total máximo de 20 lpm.

La relación estructural es: **cada biorreactor `hasSensor` uno o más sensores**, y **cada sensor `observes` una propiedad observable** (pH, DO, biomasa, temperatura, nivel de espuma).

### 7.2 Relaciones entre biorreactores y actuadores

**Evidencia explícita (Sartorius):** El Biostat® B puede configurarse con control gravimétrico de alimentación, control gravimétrico de nivel o perfiles de adición de sustrato. Esto permite operar en modo batch, fed-batch, continuo o de perfusión. El controlador avanzado de DO permite el ajuste paralelo y simultáneo de todos los parámetros que afectan al DO, como la velocidad del agitador y los caudales de gas de aire y oxígeno puro, para controlar el punto de ajuste de DO.

**Evidencia explícita (Sartorius 10L — fases):** El sistema 10 L CDCU opera con mezcla de cuatro gases distintos (nitrógeno, oxígeno, dióxido de carbono y aire comprimido), donde oxígeno, CO₂ y aire se controlan mediante controladores de flujo másico (MFCs), mientras que el nitrógeno se controla con un medidor de área variable.

La relación es: **cada biorreactor `hasActuator` uno o más actuadores** (bombas peristálticas, MFCs, mezcladores de gas, agitador motor). Cada actuador **`controlsVariable`** una variable operativa (flujo de gas, velocidad de agitación, adición de substrato, temperatura).

### 7.3 Relaciones entre biorreactores, variables operativas y fases del proceso

**Evidencia explícita:** Durante el cultivo, el biorreactor mantiene condiciones ideales para el crecimiento de los organismos. Parámetros como temperatura, pH, oxígeno disuelto y niveles de nutrientes son constantemente monitoreados y ajustados para mantener el cultivo en su fase más productiva. Los biorreactores pueden emplear estrategias de alimentación en batch, fed-batch o continuo para optimizar la producción.

**Evidencia explícita sobre fases:** Durante la fermentación, las células pasan por la fase lag (adaptación celular sin aumento en el recuento celular), la fase exponencial (división celular rápida y aumento de biomasa), la fase estacionaria (tasa de crecimiento igual a la tasa de muerte celular) y la fase de muerte (agotamiento de nutrientes y acumulación de metabolitos tóxicos).

**Evidencia explícita sobre vínculo fase–variable:** En la producción de proteína recombinante, las fases de batch y fed-batch en la fermentación son seguidas por una fase de inducción. La fase fed-batch es típicamente automatizada usando perfiles de alimentación predeterminados, control de retroalimentación dinámica basado en oxígeno disuelto (DO) o pH, o control adaptativo.

### 7.4 Relaciones entre biorreactores y eventos

**Evidencia explícita:** La inoculación marca el inicio del bioproceso. El inóculo (cultivo iniciador) se prepara con anticipación, por ejemplo mediante el cultivo nocturno en un matraz de agitación.

**Inferencia razonable:** El documento D09 (Eppendorf White Paper) menciona explícitamente una "Figure 3: Series of events in a typical bioprocess run", que según el texto incluye eventos de control de CO₂, agentes de pH líquidos y dispositivos de atemperación, aunque los detalles completos de la figura no son accesibles como texto extraíble en esta búsqueda.

**Evidencia explícita sobre eventos de alarma:** El manual del BioLector XT documenta riesgos como: incendio/explosión por aceites en líneas de gas bajo presión; perturbación del proceso si la tasa de flujo supera 0,5 L/min en reposo con la placa sujeta (indicativo de fuga); lecturas incorrectas por almacenamiento de las placas con optodes en luz solar o temperatura inadecuada (provocando blanqueamiento de los optodes y mediciones erróneas de pH y DO).

### 7.5 Marco semántico para modelar estas relaciones

**Evidencia explícita (SSN/SOSA):** En SOSA, una Actuation es realizada por un Actuator y produce un Result. Un actuador es un dispositivo, software o agente que implementa un procedimiento de actuación que define cómo se logran cambios en el estado del mundo. El modelado de actuaciones es análogo al modelado de observaciones, ya que se basa en la misma estructura central.

SSN/SOSA soporta una amplia gama de aplicaciones, incluyendo infraestructuras industriales y domésticas. Los sensores, observaciones, muestreos y actuaciones se describen usando esencialmente la misma terminología y relaciones, con superclases comunes Execution y System.

---

## 8. Tabla de afirmaciones y evidencia

| ID evidencia | Afirmación                                                                                                                       | Tipo      | Documento | Sección/página                           | Resumen fiel                                                                                            | Confianza | Validación experta                        |
| ------------ | -------------------------------------------------------------------------------------------------------------------------------- | --------- | --------- | ---------------------------------------- | ------------------------------------------------------------------------------------------------------- | --------- | ----------------------------------------- |
| E01          | BioLector XT tiene sensores ópticos para biomasa, pH, DO y fluorescencia                                                         | Explícita | D01       | Página principal + módulos               | Sistema opera con sensores ópticos pre-calibrados en línea para biomasa, fluorescencias, pH y DO        | Alta      | No requerida                              |
| E02          | BioLector XT tiene un sensor de O₂ interno en la cámara para regulación de gas                                                   | Explícita | D01       | Sección módulos O₂                       | Sensor mide O₂ continuamente y regula flujo de N₂ u O₂ al interior de la cámara                         | Alta      | No requerida                              |
| E03          | BIOSTAT B (5L/10L) tiene sensores de pH, pO₂, temperatura, espuma, nivel y sustrato                                              | Explícita | D06       | Tabla de especificaciones técnicas       | Listado explícito de sensores del BIOSTAT B                                                             | Alta      | No requerida                              |
| E04          | BIOSTAT B tiene actuadores: MFCs para O₂, CO₂, aire; agitador motor; bombas                                                      | Explícita | D04, D06  | Sección DO cascade / especificaciones    | MFCs controlan flujo de gases; agitador regula velocidad; bombas para alimentación                      | Alta      | No requerida                              |
| E05          | BIOSTAT B 10L usa MFCs para O₂, CO₂ y aire; y medidor de área variable para N₂                                                   | Explícita | D06       | Registro de equipamiento A\*STAR         | Nitrógeno controlado con medidor de área variable Q-Flow (Vögtlin Instruments)                          | Alta      | Verificación con manual oficial Sartorius |
| E06          | Las fases de un bioproceso incluyen lag, exponencial, estacionaria y muerte                                                      | Explícita | D09, D12  | White paper Eppendorf; Reid et al. 2025  | Cuatro fases reconocidas; la fase exponencial y estacionaria son críticas para la producción            | Alta      | No requerida                              |
| E07          | Las fases de proceso también incluyen etapas operativas: esterilización, inoculación, cultivo, cosecha                           | Explícita | D11       | IKA — Bioreactors in Bioprocessing       | Cuatro pasos operativos secuenciales descritos por Klapan et al.                                        | Alta      | No requerida                              |
| E08          | El fed-batch se controla automáticamente con DO y pH como señales de retroalimentación                                           | Explícita | D04, D12  | Sartorius — DO cascade; Reid et al. 2025 | La fase fed-batch se automatiza con control dinámico de DO/pH                                           | Alta      | No requerida                              |
| E09          | La inoculación es el evento que marca el inicio del bioproceso                                                                   | Explícita | D11       | IKA — Bioreactors in Bioprocessing       | "Inoculation marks the start of the bioprocess"                                                         | Alta      | No requerida                              |
| E10          | Una tasa de flujo anormal en el BioLector XT puede indicar fuga y constituye un evento de alarma                                 | Explícita | D02       | Manual p.8 — System Configuration        | Flujo >0,5 L/min en reposo indica posible fuga; impacta resultados del experimento                      | Alta      | No requerida                              |
| E11          | SOSA define Sensor, Actuator, Observation, Actuation, FeatureOfInterest y ObservableProperty como clases relacionadas            | Explícita | D07, D08  | W3C SSN/SOSA; sección 2.4 SOSA paper     | Clases y propiedades definidas canónicamente; disponibles en `w3.org/TR/vocab-ssn/`                     | Alta      | No requerida                              |
| E12          | BioLector XT soporta modos de proceso fed-batch con perfiles configurables por pocillo en el software BioLection                 | Explícita | D01       | Sección módulo microfluidico             | Software permite configurar perfiles de fed-batch orientados al proceso                                 | Alta      | No requerida                              |
| E13          | El blanqueamiento de optodes en BioLector XT por exposición a luz solar es un evento de degradación que genera error de medición | Explícita | D02       | Manual p.8                               | Las placas con optodes no deben almacenarse bajo luz solar; resultan en lecturas incorrectas de pH y DO | Alta      | No requerida                              |

---

## 9. Conceptos ontológicos candidatos

| Concepto candidato       | Tipo sugerido                  | Definición basada en evidencia                                                                                    | Fuente asociada | Estado    |
| ------------------------ | ------------------------------ | ----------------------------------------------------------------------------------------------------------------- | --------------- | --------- |
| `Bioreactor`             | Clase                          | Sistema contenedor de cultivo microbiano o celular, equipado con sensores y actuadores para control de parámetros | D04, D06, D11   | Candidato |
| `BioLectorXT`            | Individuo / Subclase           | Microbiorreactor de alto throughput de 48 pocillos basado en formato MTP, con sensores ópticos pre-calibrados     | D01             | Candidato |
| `SartoriusBioreactor5L`  | Individuo / Subclase           | Biorreactor BIOSTAT B con volumen de trabajo 0,6–5 L, sensores de pH/pO₂/temperatura/espuma/nivel/sustrato        | D06             | Candidato |
| `SartoriusBioreactor10L` | Individuo / Subclase           | Biorreactor BIOSTAT B con volumen de trabajo 1,5–10 L, sistema de mezcla de cuatro gases con MFCs                 | D06             | Candidato |
| `Sensor`                 | Clase                          | Dispositivo que mide una propiedad observable de la muestra de cultivo o del ambiente de proceso                  | D07 (SOSA)      | Candidato |
| `OpticalSensor`          | Subclase de Sensor             | Sensor que mide biomasa, pH, DO o fluorescencia mediante señales ópticas pre-calibradas                           | D01             | Candidato |
| `pHSensor`               | Subclase de Sensor             | Sensor que mide el pH de la fase líquida                                                                          | D01, D06        | Candidato |
| `DOSensor`               | Subclase de Sensor             | Sensor que mide el oxígeno disuelto en la fase líquida                                                            | D01, D06        | Candidato |
| `TemperatureSensor`      | Subclase de Sensor             | Sensor de temperatura del medio de cultivo                                                                        | D06             | Candidato |
| `FoamSensor`             | Subclase de Sensor             | Sensor de detección de espuma en el biorreactor                                                                   | D06             | Candidato |
| `LevelSensor`            | Subclase de Sensor             | Sensor de nivel de líquido en el biorreactor                                                                      | D06             | Candidato |
| `BiomassSensor`          | Subclase de Sensor             | Sensor óptico que mide señal de dispersión de luz correlacionada con biomasa                                      | D01             | Candidato |
| `Actuator`               | Clase                          | Dispositivo que modifica el estado del proceso en respuesta a señales de control                                  | D07 (SOSA), D04 | Candidato |
| `MassFlowController`     | Subclase de Actuator           | Controlador de flujo másico que regula el caudal de gases al biorreactor                                          | D06, D04        | Candidato |
| `AgitatorMotor`          | Subclase de Actuator           | Motor de agitación que controla la velocidad de mezcla del cultivo                                                | D06             | Candidato |
| `PeristalticPump`        | Subclase de Actuator           | Bomba que controla la adición de substrato, ácidos, bases o antiespumante                                         | D04, D12        | Candidato |
| `GasingModule`           | Subclase de Actuator           | Módulo de regulación de gas (O₂, N₂, CO₂) que controla la atmósfera de cultivo                                    | D01             | Candidato |
| `MicrofluidicModule`     | Clase / Subclase de Actuator   | Módulo integrado en la MTP del BioLector XT que controla pH y alimentación por pocillo sin pipeteo manual         | D01             | Candidato |
| `OperatingVariable`      | Clase                          | Parámetro de proceso medible o controlable durante el cultivo                                                     | D04, D06        | Candidato |
| `pH`                     | Individuo de OperatingVariable | Concentración de iones hidrógeno del medio de cultivo                                                             | D01, D06        | Candidato |
| `DissolvedOxygen`        | Individuo de OperatingVariable | Concentración de oxígeno disuelto en la fase líquida                                                              | D01, D06        | Candidato |
| `Temperature`            | Individuo de OperatingVariable | Temperatura del medio de cultivo                                                                                  | D06, D04        | Candidato |
| `AgitationSpeed`         | Individuo de OperatingVariable | Velocidad de agitación del biorreactor (rpm)                                                                      | D06             | Candidato |
| `GasFlowRate`            | Individuo de OperatingVariable | Caudal de gas suministrado al biorreactor (L/min)                                                                 | D06, D04        | Candidato |
| `Biomass`                | Individuo de OperatingVariable | Concentración de masa celular en el cultivo                                                                       | D01, D12        | Candidato |
| `ProcessPhase`           | Clase                          | Etapa temporal distinguible dentro del proceso de cultivo                                                         | D09, D11        | Candidato |
| `SterilizationPhase`     | Subclase de ProcessPhase       | Fase de esterilización del biorreactor y medios antes del cultivo                                                 | D11             | Candidato |
| `InoculationPhase`       | Subclase de ProcessPhase       | Fase de introducción del inóculo al biorreactor                                                                   | D11             | Candidato |
| `LagPhase`               | Subclase de ProcessPhase       | Fase de adaptación celular sin multiplicación activa                                                              | D09, D32        | Candidato |
| `ExponentialPhase`       | Subclase de ProcessPhase       | Fase de crecimiento exponencial de biomasa                                                                        | D09, D35        | Candidato |
| `StationaryPhase`        | Subclase de ProcessPhase       | Fase en que la tasa de crecimiento iguala la tasa de muerte                                                       | D09, D35        | Candidato |
| `DeathPhase`             | Subclase de ProcessPhase       | Fase de agotamiento de nutrientes y acumulación de metabolitos tóxicos                                            | D09             | Candidato |
| `HarvestPhase`           | Subclase de ProcessPhase       | Fase de recuperación del cultivo o producto                                                                       | D11             | Candidato |
| `InductionPhase`         | Subclase de ProcessPhase       | Fase de inducción de expresión de proteína recombinante (aplica a procesos microbianos)                           | D12             | Candidato |
| `ProcessEvent`           | Clase                          | Ocurrencia discreta durante el proceso de cultivo                                                                 | D11, D09        | Candidato |
| `InoculationEvent`       | Subclase de ProcessEvent       | Evento de adición del inóculo al inicio del bioproceso                                                            | D11             | Candidato |
| `AlarmEvent`             | Subclase de ProcessEvent       | Evento de alarma generado por condición anormal del sistema                                                       | D02             | Candidato |
| `LeakageAlarm`           | Subclase de AlarmEvent         | Alarma por detección de fuga de gas en BioLector XT                                                               | D02             | Candidato |
| `OptodeDegradationEvent` | Subclase de ProcessEvent       | Evento de degradación de optode por exposición a luz solar                                                        | D02             | Candidato |
| `FeedAdditionEvent`      | Subclase de ProcessEvent       | Evento de adición de substrato o alimentación al cultivo                                                          | D04, D12        | Candidato |

---

## 10. Relaciones ontológicas candidatas

| Relación candidata     | Dominio sugerido | Rango sugerido       | Significado                                                                                   | Evidencia asociada | Estado    |
| ---------------------- | ---------------- | -------------------- | --------------------------------------------------------------------------------------------- | ------------------ | --------- |
| `hasSensor`            | `Bioreactor`     | `Sensor`             | El biorreactor está equipado con el sensor especificado                                       | E01, E03           | Candidato |
| `hasActuator`          | `Bioreactor`     | `Actuator`           | El biorreactor está equipado con el actuador especificado                                     | E04, E05           | Candidato |
| `observes`             | `Sensor`         | `ObservableProperty` | El sensor mide la propiedad operativa indicada                                                | D07, E01           | Candidato |
| `controls`             | `Actuator`       | `OperatingVariable`  | El actuador regula la variable operativa especificada                                         | E04, E08           | Candidato |
| `hasOperatingVariable` | `Bioreactor`     | `OperatingVariable`  | El biorreactor opera con la variable de proceso indicada                                      | E01, E03, E04      | Candidato |
| `hasProcessPhase`      | `Bioreactor`     | `ProcessPhase`       | El biorreactor ejecuta la fase de proceso indicada                                            | E06, E07           | Candidato |
| `precedes`             | `ProcessPhase`   | `ProcessPhase`       | Una fase de proceso antecede a otra en el tiempo                                              | E07, E06           | Candidato |
| `isCharacterizedBy`    | `ProcessPhase`   | `OperatingVariable`  | La fase está caracterizada por el comportamiento de la variable indicada                      | E06, E08           | Candidato |
| `triggersEvent`        | `ProcessPhase`   | `ProcessEvent`       | Una fase de proceso desencadena el evento indicado                                            | E09, E10           | Candidato |
| `hasEvent`             | `Bioreactor`     | `ProcessEvent`       | El biorreactor es el contexto donde ocurre el evento                                          | E09, E10, E13      | Candidato |
| `generatesObservation` | `Sensor`         | `Observation`        | El sensor genera una observación con valor medido y marca de tiempo                           | D07, D08           | Candidato |
| `performsActuation`    | `Actuator`       | `Actuation`          | El actuador realiza una actuación que modifica el estado del proceso                          | D08                | Candidato |
| `isHostedBy`           | `Sensor`         | `Bioreactor`         | El sensor está alojado en el biorreactor (relación SOSA/SSN `isHostedBy`)                     | D07                | Candidato |
| `implementsProcedure`  | `Actuator`       | `Procedure`          | El actuador implementa un procedimiento de control                                            | D08                | Candidato |
| `hasFeedStrategy`      | `Bioreactor`     | `FeedingMode`        | El biorreactor opera bajo una estrategia de alimentación (batch/fed-batch/continuo/perfusión) | E08, D04           | Candidato |

---

## 11. Triadas RDF candidatas

```
# Relaciones biorreactor → sensor

BioLectorXT -> hasSensor -> BiomassSensor
Documento: D01 | Sección: Página principal BioLector XT | Estado: Soportada

BioLectorXT -> hasSensor -> pHSensor
Documento: D01 | Sección: Módulos / especificaciones técnicas | Estado: Soportada

BioLectorXT -> hasSensor -> DOSensor
Documento: D01 | Sección: Módulos / especificaciones técnicas | Estado: Soportada

SartoriusBioreactor5L -> hasSensor -> pHSensor
Documento: D06 | Sección: Technical features and specifications | Estado: Soportada

SartoriusBioreactor5L -> hasSensor -> DOSensor
Documento: D06 | Sección: Technical features and specifications | Estado: Soportada

SartoriusBioreactor5L -> hasSensor -> TemperatureSensor
Documento: D06 | Sección: Technical features and specifications | Estado: Soportada

SartoriusBioreactor5L -> hasSensor -> FoamSensor
Documento: D06 | Sección: Technical features and specifications | Estado: Soportada

SartoriusBioreactor5L -> hasSensor -> LevelSensor
Documento: D06 | Sección: Technical features and specifications | Estado: Soportada

SartoriusBioreactor10L -> hasSensor -> pHSensor
Documento: D06 | Sección: Technical features and specifications | Estado: Soportada

SartoriusBioreactor10L -> hasSensor -> DOSensor
Documento: D06 | Sección: Technical features and specifications | Estado: Soportada

# Relaciones biorreactor → actuador

BioLectorXT -> hasActuator -> GasingModule
Documento: D01 | Sección: Módulos O₂ up/down, CO₂ | Estado: Soportada

BioLectorXT -> hasActuator -> MicrofluidicModule
Documento: D01 | Sección: Módulo microfluidico | Estado: Soportada

SartoriusBioreactor5L -> hasActuator -> MassFlowController
Documento: D06 | Sección: Gas flow specification | Estado: Soportada

SartoriusBioreactor10L -> hasActuator -> MassFlowController
Documento: D06, referenciado en D17-texto | Sección: Gas flow + MFC specification | Estado: Soportada

SartoriusBioreactor5L -> hasActuator -> AgitatorMotor
Documento: D06 | Sección: Permitted stirring speed | Estado: Soportada

# Relaciones sensor → propiedad observable

pHSensor -> observes -> pH
Documento: D07 (SOSA), D01 | Estado: Soportada

DOSensor -> observes -> DissolvedOxygen
Documento: D07 (SOSA), D06 | Estado: Soportada

BiomassSensor -> observes -> Biomass
Documento: D01, D07 | Estado: Soportada

# Relaciones actuador → variable

MassFlowController -> controls -> GasFlowRate
Documento: D06, D04 | Estado: Soportada

AgitatorMotor -> controls -> AgitationSpeed
Documento: D06 | Estado: Soportada

MicrofluidicModule -> controls -> pH
Documento: D01 | Estado: Soportada

# Relaciones biorreactor → fases

BioLectorXT -> hasProcessPhase -> InoculationPhase
Documento: D11 | Estado: Parcialmente soportada (aplica genéricamente a biorreactores; no exclusiva de BioLector XT)

BioLectorXT -> hasProcessPhase -> ExponentialPhase
Documento: D09, D12 | Estado: Parcialmente soportada

SartoriusBioreactor5L -> hasProcessPhase -> FedBatchPhase
Documento: D04 | Estado: Soportada

SartoriusBioreactor10L -> hasProcessPhase -> BatchPhase
Documento: D04, D06 | Estado: Soportada

# Relaciones entre fases (secuencia)

SterilizationPhase -> precedes -> InoculationPhase
Documento: D11 | Estado: Soportada

InoculationPhase -> precedes -> LagPhase
Documento: D11, D09 | Estado: Soportada

LagPhase -> precedes -> ExponentialPhase
Documento: D09 | Estado: Soportada

ExponentialPhase -> precedes -> StationaryPhase
Documento: D09, D35 | Estado: Soportada

StationaryPhase -> precedes -> HarvestPhase
Documento: D09, D11 | Estado: Soportada

# Relaciones fase → variable característica

ExponentialPhase -> isCharacterizedBy -> Biomass
Documento: D12, D09 | Estado: Soportada

FedBatchPhase -> isCharacterizedBy -> DissolvedOxygen
Documento: D04, D12 | Estado: Soportada

# Relaciones biorreactor / fase → evento

InoculationPhase -> triggersEvent -> InoculationEvent
Documento: D11 | Estado: Soportada

BioLectorXT -> hasEvent -> LeakageAlarm
Documento: D02 | Estado: Soportada

BioLectorXT -> hasEvent -> OptodeDegradationEvent
Documento: D02 | Estado: Soportada

FedBatchPhase -> triggersEvent -> FeedAdditionEvent
Documento: D04, D12 | Estado: Soportada
```

---

## 12. Sinónimos y variantes terminológicas

| Término principal    | Sinónimos o variantes documentadas                                     | Idioma  | Documento de soporte                         |
| -------------------- | ---------------------------------------------------------------------- | ------- | -------------------------------------------- |
| `DissolvedOxygen`    | DO, pO₂, dissolved O₂, oxygen saturation                               | Inglés  | D01, D06, D04                                |
| `pH`                 | hydrogen ion concentration, acidity, acid-base                         | Inglés  | D01, D06                                     |
| `AgitationSpeed`     | stirrer speed, RPM, mixing speed                                       | Inglés  | D06                                          |
| `GasFlowRate`        | flow rate, aeration rate, total gas flow                               | Inglés  | D06, D04                                     |
| `MassFlowController` | MFC, mass flow controller, gas flow controller                         | Inglés  | D06, D04                                     |
| `InoculationPhase`   | inoculation step, inoculum addition, seeding                           | Inglés  | D11, D12                                     |
| `FedBatchPhase`      | fed-batch mode, feeding phase                                          | Inglés  | D04, D12                                     |
| `HarvestPhase`       | harvesting, cell harvest, harvest event                                | Inglés  | D11, D10                                     |
| `BiomassSensor`      | turbidity sensor, optical density sensor, backscatter sensor           | Inglés  | D01                                          |
| `OpticalSensor`      | optode, fluorescence sensor, optical probe                             | Inglés  | D01, D02                                     |
| `Biorreactor`        | fermentador, fermentor, recipiente de cultivo                          | Español | D04 (Sartorius usa "fermenter / bioreactor") |
| `FoamSensor`         | foam detector, antifoam sensor                                         | Inglés  | D06                                          |
| `GasingModule`       | O₂ up-regulation module, O₂ down-regulation module, gas control module | Inglés  | D01                                          |

---

## 13. Vacíos, riesgos y decisiones pendientes

**Información faltante:**

- No se ha accedido al manual completo del BIOSTAT B en PDF oficial de Sartorius para confirmar el listado exhaustivo de sensores y actuadores con números de parte y rangos operativos precisos.
- No se dispone de documentación interna de laboratorio (SOPs) que especifique cómo se registran los eventos de alarma y las decisiones de proceso en los sistemas específicos del proyecto.
- El manual completo del BioLector XT (más allá de p.8 en ManualsLib) no fue accedido; pueden existir secciones adicionales sobre arquitectura de sensores.
- El documento D03 (brochure PDF) no fue verificado en su contenido completo.

**Ambigüedades terminológicas:**

- "Sensor de sustrato" en BIOSTAT B (D06) puede referirse tanto a un sensor electroquímico de glucosa como a un sistema de medición gravimétrica: requiere validación con el manual oficial.
- La propiedad `hasSensor` podría superponerse con la propiedad SOSA `isHostedBy` si se adopta el estándar SSN/SOSA directamente. Debe decidirse si se extiende SOSA o se crea vocabulario propio.
- El término "microfluidic module" en BioLector XT funciona tanto como sensor de retroalimentación (pH) como actuador (alimentación): su clasificación ontológica es ambigua.

**Configuraciones dependientes del equipo:**

- El BioLector XT permite hasta 6 módulos de filtro LED simultáneos: la composición exacta de los sensores instalados varía por configuración experimental. Las triadas `hasSensor` dependen de la configuración específica del instrumento en el laboratorio.
- El BIOSTAT B 10L puede operar con N₂ controlado por medidor de área variable en lugar de MFC según el documento D06: esto implica que la relación `hasActuator → MassFlowController` puede no ser universal para N₂.

**Datos que requieren validación con expertos:**

- Confirmación de cuáles fases biológicas (lag, exponencial, estacionaria, muerte) son distinguibles y registradas automáticamente como estados discretos en el software de control (BioLection para BioLector XT; MFCS/win o BioPAT para Sartorius).
- Confirmación de qué eventos se registran como alarmas formales en los sistemas de SCADA/DCS de cada biorreactor.
- Validación de si `InductionPhase` aplica como fase de proceso en los equipos Sartorius del proyecto o es exclusiva de procesos microbianos específicos.

**Documentos adicionales necesarios:**

- Manual técnico completo BIOSTAT B (Sartorius, versión actual) — disponible en `sartorius.com` bajo registro
- Manual completo BioLector XT (Beckman Coulter) — accesible bajo licencia
- SOP del laboratorio usuario que describa procedimientos de inoculación, cosecha y respuesta a alarmas
- Documentación del software BioLection (m2p-labs/Beckman Coulter) que liste los eventos registrados automáticamente

---

## 14. Registro metodológico para el documento de investigación

La pregunta ALC-07 interroga por las relaciones estructurales básicas que debe mantener cada biorreactor (BioLector XT, Sartorius 5 L y Sartorius 10 L) con cinco categorías de entidades: sensores, actuadores, variables operativas, fases del proceso y eventos. La estrategia de búsqueda combinó consultas en sitios oficiales de fabricantes (Beckman Coulter/m2p-labs y Sartorius), registros institucionales de equipamiento (A\*STAR), el estándar internacional W3C SSN/SOSA para modelado semántico de sensores, artículos científicos revisados por pares sobre bioprocesos (Reid et al., 2025; Haller et al., 2018) y documentación técnica de terceros (Eppendorf, IKA). Se priorizaron fuentes con autoría identificada, trazabilidad verificable y evidencia extraíble en forma de especificaciones, descripciones técnicas o definiciones formales. El corpus final incluye diez documentos verificables que permiten establecer las siguientes relaciones preliminares: (i) cada biorreactor `hasSensor` uno o más sensores de pH, DO, temperatura, biomasa, espuma y nivel; (ii) cada biorreactor `hasActuator` dispositivos tales como controladores de flujo másico, motores de agitación y bombas peristálticas; (iii) cada actuador `controls` una variable operativa específica; (iv) cada sensor `observes` una propiedad observable análoga a la arquitectura SOSA; (v) el proceso de cultivo se estructura en fases ordenadas temporalmente mediante la relación `precedes` (esterilización → inoculación → lag → exponencial → estacionaria → cosecha); y (vi) los eventos —incluyendo alarmas, adición de substrato e inoculación— se vinculan a fases y biorreactores mediante las relaciones `triggersEvent` y `hasEvent`. Los conceptos y relaciones identificados son todos candidatos sujetos a validación experta y verificación contra los manuales técnicos completos, que no fueron accedidos en su totalidad. Las principales limitaciones incluyen la ausencia de SOPs de laboratorio internos, ambigüedad en la clasificación del módulo microfluidico del BioLector XT como sensor o actuador, y dependencia de la configuración específica del equipo para determinar cuáles sensores están activos en cada instancia del instrumento.

---

## 15. Estado final

| Dimensión                      | Estado                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| ------------------------------ | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Nivel de confianza general** | **Medio-Alto** — la mayoría de las relaciones están soportadas por fuentes de fabricante y literatura científica; faltan manuales técnicos completos                                                                                                                                                                                                                                                                                                                         |
| **Estado de la respuesta**     | **Parcialmente soportada** — las relaciones centrales (sensor, actuador, variable, fase) tienen evidencia explícita; las relaciones con eventos y alarmas tienen evidencia parcial                                                                                                                                                                                                                                                                                           |
| **Estado del corpus**          | **Parcial** — suficiente para trazar el esquema relacional básico; insuficiente para especificaciones exhaustivas de instancias individuales                                                                                                                                                                                                                                                                                                                                 |
| **Próxima acción recomendada** | (1) Obtener y cargar el manual técnico completo del BIOSTAT B (Sartorius) y del BioLector XT (Beckman Coulter). (2) Consultar con el experto de laboratorio para confirmar qué eventos se registran formalmente en los sistemas de control. (3) Decidir si se adopta SSN/SOSA como vocabulario base o se construye vocabulario propio, y definir la propiedad de alineación. (4) Avanzar a la pregunta ALC-08 o equivalente que profundice en valores de variables por fase. |
