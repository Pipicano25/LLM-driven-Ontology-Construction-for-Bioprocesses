## Prompt maestro – ALC-07

### 1. Identificación de la pregunta

- **ID:** ALC-07
- **Nivel metodológico:** Ontológico-conceptual básico
- **Tema:** Arquitectura de relaciones bioreactor-sistema
- **Pregunta:** ¿Qué relaciones básicas debe tener cada biorreactor con sensores, actuadores, variables operativas, fases del proceso y eventos?

### 2. Propósito de la pregunta

Busca establecer el esqueleto relacional mínimo para la ontología OWL/RDF: qué entidades debe “conocer” un bioreactor (sensores que lo instrumentan, actuadores que lo controlan, variables que mide/regula, fases en las que opera y eventos que genera). Contribuye al corpus al extraer evidencia documental explícita de manuales de fabricante, evitando definiciones inventadas.

### 3. Plan de búsqueda documental

**Información técnica requerida:** listados de sensores, actuadores, variables controladas, modos de proceso y mecanismos de alarma para BioLector XT, Biostat B 5 L y 10 L.

**Tipos de documentos:** manuales técnicos, technical notes, brochures oficiales, datasheets.

**Repositorios:** beckman.com, media.beckman.com, sartorius.com

**Términos ES/EN:**

- ES: "BioLector XT sensores pH oxígeno", "Biostat B manual sensores actuadores"
- EN: "BioLector XT brochure sensors", "Biostat B bioreactor manual pH DO"

**Ecuaciones:** ("BioLector XT" AND sensors) OR ("Biostat B" AND "process control" AND sensors)

**Criterios:** inclusión 2021-2026, fuente fabricante; exclusión blogs sin trazabilidad.

### 4. Documentos candidatos encontrados

| ID documento | Título                                                              | Entidad autora                           | Año       | Tipo de fuente   | URL/DOI verificable                                                                                    | Relación con la pregunta                                                          | Decisión preliminar |
| ------------ | ------------------------------------------------------------------- | ---------------------------------------- | --------- | ---------------- | ------------------------------------------------------------------------------------------------------ | --------------------------------------------------------------------------------- | ------------------- |
| DOC-01       | Using the BioLector XT Microbioreactor Gassing Lid – Technical Note | Beckman Coulter Life Sciences / m2p-labs | 2021      | Technical note   | https://media.beckman.com/-/media/m2p-labs/pdfs/using-the-biolector-xt-microbioreactor-gassing-lid.pdf | Describe actuadores de gas y control software                                     | Include             |
| DOC-02       | BIOLECTOR XT Microbioreactor – Brochure                             | Beckman Coulter Life Sciences            | 2021-2023 | Brochure oficial | https://media.beckman.com/-/media/pdf-assets/brochures/biolector-xt-microbioreactor-brochure.ashx      | Lista sensores ópticos, variables, control pH, fases                              | Include             |
| DOC-03       | Biostat® B – The Multi-Talented Bioreactor                          | Sartorius Stedim Biotech                 | 2020-2022 | Brochure técnico | https://www.sartorius.com/download/34576/5/broch-biostat-b-sbi1513-e-1--data.pdf                       | Especifica sensores, actuadores, variables, modos de proceso, alarmas para 1-10 L | Include             |

### 5. Evaluación de documentos candidatos

| ID documento | Relevancia | Autoridad | Trazabilidad | Cobertura de la pregunta            | Evidencia localizable       | Justificación                                                                            |
| ------------ | ---------- | --------- | ------------ | ----------------------------------- | --------------------------- | ---------------------------------------------------------------------------------------- |
| DOC-01       | Alta       | Alta      | Alta         | Media – actuadores gas              | Sí – páginas 1-3            | Fuente fabricante, describe modos de gassing seleccionables en software                  |
| DOC-02       | Alta       | Alta      | Alta         | Alta – sensores, variables, control | Sí – múltiples secciones    | Define medición online de biomasa, pH, DO y control pH                                   |
| DOC-03       | Alta       | Alta      | Alta         | Alta – todo el alcance              | Sí – tabla especificaciones | Lista sensores pH, DO, temperatura, foam; actuadores bombas y MFC; modos batch/fed-batch |

### 6. Corpus documental seleccionado

| ID documento | Documento seleccionado     | Pregunta asociada | Fragmentos relevantes                                                          | Estado     |
| ------------ | -------------------------- | ----------------- | ------------------------------------------------------------------------------ | ---------- |
| DOC-01       | Technical Note Gassing Lid | ALC-07            | Introducción sensores pH/DO/biomasa; modos gassing                             | Verificado |
| DOC-02       | Brochure BioLector XT      | ALC-07            | Online measurement biomass, fluorescence, pH, DO; pH control by acid/alkali    | Verificado |
| DOC-03       | Brochure Biostat B         | ALC-07            | Sensores tabla; control tower aeration/pump/temp; modos proceso; alarm contact | Verificado |

### 7. Respuesta basada en evidencia

**Evidencia explícita:**

- Cada bioreactor integra sensores para variables clave. Biostat B documenta: Temperature Pt100 0–150°C, Dissolved oxygen 0–100%, pH 2–12, Foam, Level, Turbidity, Redox. BioLector XT documenta medición online de biomasa, fluorescencia, pH y DO con sensores ópticos pre-calibrados.
- Cada bioreactor integra actuadores. Biostat B: control tower contiene módulos de aeration, pump y temperature control; hasta cuatro bombas peristálticas internas; válvulas solenoide y controladores de flujo másico para gases. BioLector XT: gassing lid con modos seleccionables (air, N2, O2, CO2) y flujos 5–50 mL/min; agitación 100–1500 rpm; módulo microfluídico con microválvulas para alimentación y control pH.
- Variables operativas están asociadas a control automático. Biostat B: "Automatic pH Control" por adición ácido/base o CO2; "Automatic DO Control" con ajuste paralelo de agitador y flujos de gas. BioLector XT: "pH control by acid or/and alkali"; control de atmósfera (CO2, O2).
- Fases del proceso están declaradas como modos. Biostat B: aplicaciones listan Batch, Fed-batch, Continuous, Perfusion. BioLector XT: menciona batch y fed-batch anaeróbico.
- Eventos y alarmas: Biostat B incluye "potentialfree (common) alarm contact" y "Remote Alarming" en MFCS. BioLector XT gestiona eventos vía BioLection software (selección de modos, protocolos).

**Inferencia razonable:**

- La relación "bioreactor – hasSensor – sensor" es necesaria porque los documentos listan sensores como parte del sistema.
- La relación "sensor – measures – variable" se infiere de la tabla de rangos.
- La relación "actuador – controls – variable" se infiere de descripciones de control automático.

**Información no establecida en el corpus:**

- Taxonomía detallada de eventos (fallas específicas, alarmas por tipo) no está enumerada.
- Equivalencias funcionales exactas entre escalas 5 L vs 10 L vs microescala no están documentadas en los fragmentos; solo se indica rango de volúmenes de trabajo para Biostat B (5 L: 0.6–5 L, 10 L: 1.5–10 L).

### 8. Tabla de afirmaciones y evidencia

| ID evidencia | Afirmación                                                     | Tipo      | Documento | Página/sección          | Fragmento fiel                                                                           | Confianza | Validación experta       |
| ------------ | -------------------------------------------------------------- | --------- | --------- | ----------------------- | ---------------------------------------------------------------------------------------- | --------- | ------------------------ |
| E01          | Bioreactor mide pH, DO, biomasa online                         | Explícita | DOC-02    | Online Monitoring       | "Disposable 48 well MTPs enable online measurement of biomass, fluorescences, pH and DO" | Alta      | No                       |
| E02          | Biostat B tiene sensores pH 2-12, DO 0-100%, temperatura Pt100 | Explícita | DOC-03    | Process Control Sensors | Tabla sensores                                                                           | Alta      | No                       |
| E03          | Bioreactor controla pH por ácido/base                          | Explícita | DOC-03    | Automatic pH Control    | "Control the pH... by automatic acid and base addition"                                  | Alta      | No                       |
| E04          | BioLector XT controla pH por ácido/álcali                      | Explícita | DOC-02    | Specs                   | "pH control By acid or/and alkali"                                                       | Alta      | No                       |
| E05          | Actuadores incluyen bombas peristálticas (hasta 4)             | Explícita | DOC-03    | Pump Module             | "Up to four internal pumps can be selected per vessel"                                   | Alta      | No                       |
| E06          | Actuadores incluyen MFC y válvulas solenoide                   | Explícita | DOC-03    | Aeration                | "Optional mass flow controllers provide exact flow rate control"                         | Media     | Sí – modelos específicos |
| E07          | Modos de proceso: batch, fed-batch, continuous, perfusion      | Explícita | DOC-03    | Applications            | Tabla aplicaciones                                                                       | Alta      | No                       |
| E08          | Bioreactor genera alarmas remotas                              | Explícita | DOC-03    | MFCS                    | "Remote Alarming"                                                                        | Media     | Sí – tipos de alarma     |

### 9. Conceptos ontológicos candidatos

| Concepto candidato  | Tipo sugerido | Definición basada en evidencia                                    | Fuente       | Estado    |
| ------------------- | ------------- | ----------------------------------------------------------------- | ------------ | --------- |
| Bioreactor          | Clase         | Sistema que integra vessel, control tower y sensores para cultivo | DOC-03       | candidato |
| Sensor              | Clase         | Dispositivo que mide variable (pH, DO, temperatura)               | DOC-03 tabla | candidato |
| Actuator            | Clase         | Dispositivo que ejecuta acción (bomba, válvula, agitador)         | DOC-03       | candidato |
| OperationalVariable | Clase         | Parámetro medido/controlado (pH, DO, Biomass)                     | DOC-02       | candidato |
| ProcessPhase        | Clase         | Modo operacional (Batch, FedBatch)                                | DOC-03       | candidato |
| Event               | Clase         | Ocurrencia detectable (alarma)                                    | DOC-03       | candidato |
| pH_Sensor           | Subclase      | Sensor de pH 2-12                                                 | DOC-03       | candidato |
| DO_Sensor           | Subclase      | Sensor oxígeno 0-100%                                             | DOC-03       | candidato |

### 10. Relaciones ontológicas candidatas

| Relación candidata     | Dominio    | Rango               | Significado                           | Evidencia | Estado                 |
| ---------------------- | ---------- | ------------------- | ------------------------------------- | --------- | ---------------------- |
| hasSensor              | Bioreactor | Sensor              | bioreactor está equipado con sensor   | E02       | soportada              |
| hasActuator            | Bioreactor | Actuator            | bioreactor está equipado con actuador | E05, E06  | soportada              |
| measures               | Sensor     | OperationalVariable | sensor mide variable                  | E01       | soportada              |
| controls               | Actuator   | OperationalVariable | actuador regula variable              | E03, E04  | soportada              |
| operatesIn             | Bioreactor | ProcessPhase        | bioreactor ejecuta fase               | E07       | soportada              |
| generatesEvent         | Bioreactor | Event               | bioreactor produce evento/alarma      | E08       | parcialmente soportada |
| hasOperationalVariable | Bioreactor | OperationalVariable | variable asociada al sistema          | E01-E04   | soportada              |

### 11. Triadas RDF candidatas

- **Bioreactor -> hasSensor -> pH_Sensor** — DOC-03, tabla sensores — soportada
- **pH_Sensor -> measures -> pH** — DOC-03 — soportada
- **Bioreactor -> hasActuator -> PeristalticPump** — DOC-03, "up to four internal pumps" — soportada
- **PeristalticPump -> controls -> FeedRate** — inferida de "Automatic Feed Control" — requiere validación experta
- **BioLectorXT -> hasSensor -> DO_Sensor** — DOC-02, "online measurement of DO" — soportada
- **Bioreactor -> operatesIn -> FedBatch** — DOC-03 — soportada
- **Bioreactor -> generatesEvent -> Alarm** — DOC-03 "alarm contact" — parcialmente soportada

### 12. Sinónimos y variantes terminológicas

| Término principal   | Variantes         | Idioma | Documento                   |
| ------------------- | ----------------- | ------ | --------------------------- |
| Sensor              | probe, optode     | EN     | DOC-02 "optical sensors"    |
| Actuator            | pump, valve, MFC  | EN     | DOC-03                      |
| OperationalVariable | process parameter | EN     | DOC-03 "process parameters" |
| ProcessPhase        | operation mode    | EN     | DOC-03                      |

### 13. Vacíos, riesgos y decisiones pendientes

- No hay taxonomía exhaustiva de eventos/fallas en los manuales consultados; solo "alarm contact".
- Equivalencias funcionales entre BioLector XT (800-2400 µL) y Biostat 5 L/10 L no están detalladas.
- Falta evidencia explícita de relación sensor-actuador-variable en formato causa-efecto para todos los lazos de control.
- Necesario validar con expertos si "hasActuator" debe subdividirse en hasPump, hasGasController, hasAgitator.

### 14. Registro metodológico

Se analizó ALC-07 mediante búsqueda dirigida en documentación oficial de Beckman Coulter y Sartorius (2021-2023). Se recuperaron tres documentos verificables que listan sensores (pH, DO, temperatura, biomasa), actuadores (bombas, MFC, válvulas, agitación), variables operativas y modos de proceso. La selección aplicó criterios de autoridad de fabricante y trazabilidad de tablas técnicas. La evidencia permitió identificar relaciones básicas bioreactor-sensor-actuador-variable-fase-evento, formalizadas como clases y propiedades candidatas en inglés. Las limitaciones incluyen ausencia de taxonomía de alarmas y de mapeo inter-escala, que requieren validación experta posterior.

### 15. Estado final

- **Nivel de confianza general:** Medio
- **Estado de la respuesta:** Parcialmente soportada
- **Estado del corpus:** Parcial – suficiente para relaciones básicas, insuficiente para eventos detallados
- **Próxima acción recomendada:** Suministrar manuales de usuario completos de BioLector XT (BioLection software manual) y Biostat B DCU (sección alarmas/eventos) para extraer taxonomía de eventos y confirmar lazos de control específicos en 5 L y 10 L.
