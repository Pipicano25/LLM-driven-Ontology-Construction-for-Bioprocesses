### 1. Identificación de la pregunta

- **ID:** ALC-08
- **Nivel metodológico:** Alcance y delimitación ontológica
- **Tema:** Ontología OWL/RDF para BioLector XT, Sartorius 5 L y Sartorius 10 L
- **Pregunta:** ¿Qué conceptos deben quedar fuera del alcance inicial para evitar que la ontología sea demasiado amplia?

### 2. Propósito de la pregunta

La pregunta busca definir límites explícitos antes de modelar. Sin exclusiones, la ontología tendería a absorber dominios adyacentes (downstream, gestión empresarial, biología molecular completa) y perdería las propiedades que la literatura exige: ser sobre un dominio específico, ser lo más pequeña posible y ser autocontenida. La respuesta contribuye al corpus al establecer criterios negativos de inclusión y a la base ontológica al proponer clases y relaciones que se marcarán como "fuera de alcance" en la versión inicial.

### 3. Plan de búsqueda documental

**Información técnica requerida:**

- Especificaciones funcionales de BioLector XT (variables medidas, actuadores).
- Especificaciones de Sartorius BIOSTAT B (5 L / 10 L) (controladores, alarmas, interfaces).
- Principios de delimitación de alcance en ingeniería ontológica.

**Tipos de documentos necesarios:**

- Manuales técnicos oficiales y fichas de fabricante.
- Guías de buenas prácticas en desarrollo de ontologías biomédicas.
- Revisiones sobre modularización ontológica.

**Repositorios y sitios oficiales sugeridos:**

- beckman.com / beckman.es (m2p-labs)
- manualslib.com (manuales Sartorius)
- PLOS Computational Biology, PMC, NIEHS

**Términos de búsqueda:**

- ES: "BioLector XT manual", "Sartorius Biostat B 5L manual", "alcance ontología bioprocesos"
- EN: "BioLector XT technical data sheet", "BIOSTAT B operating instructions", "ontology scope best practices", "modular ontology size"

**Ecuaciones de búsqueda sugeridas:**

- ("BioLector XT" OR "m2p-labs") AND ("technical data" OR manual)
- ("BIOSTAT B" AND Sartorius) AND (manual OR "operating instructions")
- ("ontology development" AND scope) OR ("Ten Simple Rules" AND bio-ontology)

**Criterios de inclusión y exclusión:** se aplican los definidos en el prompt maestro (priorizar 2021-2026, fuentes oficiales, evidencia trazable).

### 4. Documentos candidatos encontrados

| ID documento | Título                                                                                | Entidad autora             | Año                       | Tipo de fuente              | URL/DOI verificable                                                                                      | Relación con la pregunta                          | Decisión preliminar |
| ------------ | ------------------------------------------------------------------------------------- | -------------------------- | ------------------------- | --------------------------- | -------------------------------------------------------------------------------------------------------- | ------------------------------------------------- | ------------------- |
| DOC-01       | BioLector XT Technical Data Sheet                                                     | Beckman Coulter / m2p-labs | s.f. (consultado 2026)    | Ficha técnica oficial       | https://www.beckman.es/resources/reading-material/product-instructions/biolector-xt-technical-data-sheet | Define variables y límites funcionales del equipo | Include             |
| DOC-02       | BIOSTAT B-DCU Operating Instructions Manual                                           | Sartorius Stedim Biotech   | 2023 (impreso 20-09-2023) | Manual oficial              | https://www.manualslib.com/manual/3061881/Sartorius-Stedim-Biotech-Biostat-B-Dcu.html                    | Describe control, alarmas e interfaces            | Include             |
| DOC-03       | Ten Simple Rules for Selecting a Bio-ontology                                         | Malone J. et al.           | 2016                      | Artículo revisado por pares | https://doi.org/10.1371/journal.pcbi.1004743                                                             | Regla 1 sobre dominio específico                  | Include             |
| DOC-04       | Best Practices: Ontology Development and Curation                                     | Carmody L., NIEHS          | 2025                      | Guía institucional          | https://www.niehs.nih.gov/sites/default/files/2025-03/CARMODY_bestpractices_508.pdf                      | Criterio P5 Scope                                 | Include             |
| DOC-05       | Survey of modular ontology techniques and their applications in the biomedical domain | PMC                        | 2009                      | Revisión                    | https://pmc.ncbi.nlm.nih.gov/articles/PMC3113511/                                                        | Principios de tamaño y reutilización parcial      | Include             |
| DOC-06       | BIOSTAT B Operating Manual – PID controller settings                                  | Sartorius Stedim Biotech   | 2023                      | Manual oficial              | https://www.manualslib.com/manual/3343908/Sartorius-Stedim-Biotech-Biostat-B.html?page=144               | Detalla alcance de control                        | Uncertain           |

### 5. Evaluación de documentos candidatos

| ID documento | Relevancia | Autoridad | Trazabilidad | Cobertura de la pregunta                                        | Evidencia localizable                     | Justificación                                                      |
| ------------ | ---------- | --------- | ------------ | --------------------------------------------------------------- | ----------------------------------------- | ------------------------------------------------------------------ |
| DOC-01       | Alta       | Alta      | Alta         | Media                                                           | Sí – tablas de parámetros                 | Define qué mide/controla BioLector XT, permite inferir exclusiones |
| DOC-02       | Alta       | Alta      | Alta         | Media                                                           | Sí – descripción de puertos y alarmas     | Delimita alcance a sistema de control, no a procesos externos      |
| DOC-03       | Alta       | Alta      | Sí – Regla 1 | Establece que ontología debe cubrir dominio específico, no todo |
| DOC-04       | Alta       | Alta      | Alta         | Alta                                                            | Sí – P5 Scope                             | Define alcance como principio formal                               |
| DOC-05       | Alta       | Media     | Alta         | Alta                                                            | Sí – tamaño mínimo, reutilización parcial | Fundamenta exclusión para mantener módulos pequeños                |

### 6. Corpus documental seleccionado

| ID documento | Documento seleccionado            | Pregunta asociada | Fragmentos o páginas relevantes                                              | Estado   |
| ------------ | --------------------------------- | ----------------- | ---------------------------------------------------------------------------- | -------- |
| DOC-01       | BioLector XT Technical Data Sheet | ALC-08            | Temperatura 10–50°C; shaking 100–1500 rpm; optodos DO y pH; feeding profiles | Incluido |
| DOC-02       | BIOSTAT B-DCU Manual              | ALC-08            | Alarm contacts, Host Ethernet, Tower connections                             | Incluido |
| DOC-03       | Ten Simple Rules                  | ALC-08            | Rule 1: ontology should be about a specific domain                           | Incluido |
| DOC-04       | Best Practices NIEHS              | ALC-08            | P5 Scope – extent of domain                                                  | Incluido |
| DOC-05       | Survey modular ontology           | ALC-08            | Size, correctness, completeness; partial reuse                               | Incluido |

### 7. Respuesta basada en evidencia

**Evidencia explícita:**

- La guía NIEHS establece que el alcance es "extent of the domain or subject matter it intends to cover".
- Malone et al. indican que una ontología debe "provide coverage for the area it claims to describe" y no intentar cubrir áreas grandes faltantes; si reclama solo un subconjunto, debe hacerlo apropiadamente.
- El survey de ontologías modulares exige que un módulo "should be as small as possible" y que la reutilización parcial es necesaria porque OWL solo permite importar ontologías completas.
- BioLector XT documenta exclusivamente condiciones de cultivo: temperatura, velocidad de agitación, DO, pH, humidificación activa, módulos de O2/CO2, y perfiles de alimentación. No menciona purificación, analítica offline avanzada ni gestión de planta.
- BIOSTAT B-DCU documenta puertos USB, alarma, host Ethernet para MFCS SCADA, conexiones de torres de suministro. No documenta ERP, LIMS corporativo ni validación regulatoria.

**Inferencia razonable basada en evidencia:**
Dado que los manuales limitan el dominio a variables operativas y control, y que las buenas prácticas exigen dominios específicos y módulos pequeños, los conceptos que amplían el alcance más allá del biorreactor y su control inmediato deben excluirse inicialmente.

**Información no establecida en el corpus:**
No se encontró en los documentos una lista normativa de exclusiones para biorreactores; las exclusiones se derivan por contraste con el alcance documentado.

**Conceptos a excluir inicialmente:**

1. **Procesos downstream** (cromatografía, filtración tangencial, liofilización) – no aparecen en DOC-01 ni DOC-02.
2. **Gestión empresarial** (ERP, compras, finanzas, RRHH) – fuera del "host" limitado a SCADA.
3. **Sistemas LIMS/QMS corporativos completos** – solo se menciona conexión a host, no trazabilidad regulatoria integral.
4. **Biología molecular detallada** (vías metabólicas completas, genomas, ingeniería de cepas) – BioLector mide fenotipo, no diseña rutas.
5. **Infraestructura de planta** (HVAC, utilities, tratamiento de agua) – manual menciona solo aire comprimido y gases para módulos, no diseño de utilidades.
6. **Ensayos clínicos y farmacovigilancia** – dominio distinto al de cultivo.
7. **Mantenimiento predictivo avanzado basado en IA externa** – manual limita a PID y alarmas, no a modelos externos.
8. **Ontologías de dominio amplio no específicas** (p.ej., ontologías completas de enfermedades humanas) – contradice Regla 1.

### 8. Tabla de afirmaciones y evidencia

| ID evidencia | Afirmación                                                           | Tipo de evidencia | Documento      | Página/sección         | Fragmento o resumen fiel                                                                                                                            | Confianza | Validación experta |
| ------------ | -------------------------------------------------------------------- | ----------------- | -------------- | ---------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------- | --------- | ------------------ |
| E1           | El alcance debe definirse como extensión del dominio                 | Explícita         | DOC-04         | P5                     | "Scope - extent of the domain or subject matter it intends to cover"                                                                                | Alta      | No                 |
| E2           | Ontología debe ser sobre dominio específico, no cubrir todo          | Explícita         | DOC-03         | Rule 1                 | "should provide coverage for the area it claims to describe... if ontology claims to only describe a specific subset... should do so appropriately" | Alta      | No                 |
| E3           | Módulos deben ser lo más pequeños posible                            | Explícita         | DOC-05         | 2.3                    | "Size: A module... should be as small as possible"                                                                                                  | Alta      | No                 |
| E4           | BioLector XT cubre solo temperatura, agitación, DO, pH, alimentación | Explícita         | DOC-01         | Cultivation conditions | "TEMPERATURE 10 – 50 °C... SHAKING SPEED 100 – 1500 rpm... OXYGEN OPTODES 0 – 100 %... pH OPTODES pH 4 – 7.5"                                       | Alta      | No                 |
| E5           | BIOSTAT B se limita a control, alarmas y conexión host SCADA         | Explícita         | DOC-02         | Device description     | "Com Alarm... Host Ethernet port for an external host system e.g., MFCS SCADA"                                                                      | Alta      | No                 |
| E6           | Downstream no está en manuales                                       | Inferida          | DOC-01, DOC-02 | —                      | Ausencia de términos downstream                                                                                                                     | Media     | Sí                 |
| E7           | Gestión empresarial debe excluirse para mantener especificidad       | Inferida          | DOC-03, DOC-04 | —                      | Aplicación de Regla 1 y P5                                                                                                                          | Media     | Sí                 |

### 9. Conceptos ontológicos candidatos

| Concepto candidato         | Tipo sugerido     | Definición basada en evidencia                                            | Fuente asociada                        | Estado              |
| -------------------------- | ----------------- | ------------------------------------------------------------------------- | -------------------------------------- | ------------------- |
| BioreactorSystem           | Clase             | Sistema que ejecuta cultivo con control de temperatura, agitación, DO, pH | DOC-01                                 | Candidato a incluir |
| DownstreamProcessing       | Clase             | Conjunto de operaciones posteriores al cultivo (no documentado)           | DOC-01 ausencia                        | Candidato a excluir |
| EnterpriseResourcePlanning | Clase             | Sistema de gestión financiera y compras                                   | DOC-02 ausencia                        | Candidato a excluir |
| ClinicalTrial              | Clase             | Estudio en humanos                                                        | DOC-03 dominio específico              | Candidato a excluir |
| PlantUtilitySystem         | Clase             | HVAC, agua, vapor                                                         | DOC-01 mención parcial aire comprimido | Candidato a excluir |
| MetabolicPathway           | Clase             | Red bioquímica detallada                                                  | DOC-01 no incluye                      | Candidato a excluir |
| hasOperationalVariable     | Propiedad de dato | Relaciona sistema con variable medida                                     | DOC-01                                 | Candidato a incluir |

### 10. Relaciones ontológicas candidatas

| Relación candidata       | Dominio sugerido | Rango sugerido      | Significado                                            | Evidencia asociada | Estado    |
| ------------------------ | ---------------- | ------------------- | ------------------------------------------------------ | ------------------ | --------- |
| excludesFromInitialScope | OntologyModule   | Concept             | Indica que un concepto queda fuera del alcance inicial | E2, E3             | Candidato |
| hasScopeBoundary         | BioreactorSystem | OperationalVariable | Delimita variables incluidas                           | E4                 | Candidato |
| connectsTo               | BioreactorSystem | SCADAHost           | Conexión documentada                                   | E5                 | Candidato |

### 11. Triadas RDF candidatas

- **BioreactorSystem -> hasScopeBoundary -> Temperature** – Soportada – DOC-01, sección Temperature – Estado: soportada
- **BioreactorSystem -> hasScopeBoundary -> DissolvedOxygen** – Soportada – DOC-01, OXYGEN OPTODES – Estado: soportada
- **OntologyModule -> excludesFromInitialScope -> DownstreamProcessing** – Parcialmente soportada – inferida de ausencia en DOC-01/DOC-02 y E2 – Estado: requiere validación experta
- **OntologyModule -> excludesFromInitialScope -> EnterpriseResourcePlanning** – Parcialmente soportada – E2, E3 – Estado: requiere validación experta

### 12. Sinónimos y variantes terminológicas

| Término principal | Sinónimos o variantes documentadas | Idioma | Documento de soporte |
| ----------------- | ---------------------------------- | ------ | -------------------- |
| Scope             | extent of the domain               | EN     | DOC-04               |
| Bioreactor        | fermenter                          | EN     | DOC-02               |
| Dissolved oxygen  | DO, dissolved oxygen               | EN     | DOC-01               |
| pH control        | triggered pH control (closed loop) | EN     | DOC-01               |

### 13. Vacíos, riesgos y decisiones pendientes

- Información faltante: no hay lista oficial de exclusiones de Sartorius para 5 L/10 L; se requiere manual específico de Biostat B 5L.
- Ambigüedades: "host system" podría interpretarse como LIMS; DOC-02 solo menciona MFCS SCADA, necesita validación.
- Configuraciones dependientes del equipo: módulos opcionales de BioLector (O2 up/down) podrían ampliar alcance si se incluyen.
- Validación experta requerida para confirmar exclusión de mantenimiento predictivo y analítica offline.
- Documentos adicionales necesarios: SOPs internos de escalado, ontologías existentes como OBI o BFO para alineación.

### 14. Registro metodológico para el documento de investigación

Se analizó la pregunta ALC-08 mediante búsqueda dirigida en manuales oficiales de Beckman Coulter y Sartorius y en literatura de ingeniería ontológica (2016-2025). La estrategia combinó términos técnicos de equipos con principios de alcance ontológico. Se aplicaron criterios de inclusión centrados en trazabilidad y autoridad. El corpus final integró cinco documentos que evidencian que BioLector XT y BIOSTAT B se limitan a variables operativas y control, mientras que las guías NIEHS y Malone exigen dominios específicos y módulos pequeños. De esta evidencia se extrajeron afirmaciones explícitas sobre alcance y tamaño, y se infirieron exclusiones para procesos downstream, gestión empresarial y biología molecular detallada. Los conceptos y relaciones se proponen como candidatos en inglés, pendientes de validación experta.

### 15. Estado final

- **Nivel de confianza general:** Medio
- **Estado de la respuesta:** Parcialmente soportada (evidencia sólida sobre principios de alcance, inferencia necesaria para lista específica de exclusiones)
- **Estado del corpus:** Parcial (faltan manuales específicos Sartorius 5 L/10 L)
- **Próxima acción recomendada:** Obtener manual oficial Sartorius Biostat B 5L/10L y validar con experto en bioprocesos la lista de exclusiones propuesta antes de modelar en OWL.
