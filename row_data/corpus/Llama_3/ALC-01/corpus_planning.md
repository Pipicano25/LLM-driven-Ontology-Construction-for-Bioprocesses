## 1. Identificación de la pregunta

- **ID:** ALC-01
- **Nivel metodológico:** conceptual-ontológico
- **Tema:** Definición de biorreactor en el contexto del proyecto
- **Pregunta:** ¿Qué se entiende por biorreactor dentro del proyecto, considerando BioLector XT, Sartorius 5 L y Sartorius 10 L?

## 2. Propósito de la pregunta

Busca establecer una definición operativa común de "biorreactor" que sea válida para tres escalas heterogéneas del proyecto. Esta definición es el anclaje para la ontología OWL/RDF: permitirá crear la clase base **Bioreactor** y sus especializaciones, alinear variables operativas, y definir equivalencias funcionales entre microescala (BioLector XT) y banco (5 L / 10 L). Contribuye al corpus al exigir evidencia explícita de fabricante sobre propósito, componentes y volúmenes.

## 3. Plan de búsqueda documental

**Información técnica requerida:**

- Definición funcional de biorreactor/microbiorreactor
- Descripción de sistema BioLector XT (formato, volúmenes, monitoreo)
- Descripción de sistema Sartorius BIOSTAT B-DCU con vasos UniVessel Glass 5 L y 10 L
- Volúmenes de trabajo y totales

**Tipos de documentos necesarios:**

- Manuales técnicos oficiales, notas técnicas, páginas de producto, brochures

**Repositorios y sitios oficiales sugeridos:**

- media.beckman.com, beckman.com (m2p-labs)
- sartorius.com, manuals.lib

**Términos de búsqueda (es/en):**

- "BioLector XT microbioreactor" / "microbiorreactor BioLector XT"
- "BIOSTAT B-DCU operating instructions"
- "Univessel Glass 5 L 10 L working volume"

**Ecuaciones de búsqueda:**

- "BioLector XT" AND "microbioreactor" AND "high-throughput"
- "BIOSTAT B-DCU" AND "bioreactor" AND "cultivate"
- "Univessel Glass" AND ("5 L" OR "10 L") AND "working volume"

**Criterios de inclusión/exclusión:** aplican los definidos en el prompt maestro; priorizar 2021-2026, aceptar manuales anteriores si vigentes.

## 4. Documentos candidatos encontrados

| ID documento | Título                                                              | Entidad autora                           | Año                   | Tipo de fuente     | URL/DOI verificable                                                                                    | Relación con la pregunta                                                                                  | Decisión preliminar |
| ------------ | ------------------------------------------------------------------- | ---------------------------------------- | --------------------- | ------------------ | ------------------------------------------------------------------------------------------------------ | --------------------------------------------------------------------------------------------------------- | ------------------- |
| DOC-01       | Using the BioLector XT Microbioreactor Gassing Lid (Technical Note) | Beckman Coulter Life Sciences / m2p-labs | s.f. (no verificable) | Nota técnica       | https://media.beckman.com/-/media/m2p-labs/pdfs/using-the-biolector-xt-microbioreactor-gassing-lid.pdf | Define BioLector XT como dispositivo de sobremesa para screening con monitoreo en línea                   | Include             |
| DOC-02       | Advantages & Applications of the BioLector XT Microbioreactor       | Beckman Coulter Life Sciences            | s.f.                  | Página de producto | https://media.beckman.com/microbioreactor/biolector-xt/advantages-and-applications                     | Describe formato MTP, sensores ópticos precalibrados, microfluídica                                       | Include             |
| DOC-03       | BIOSTAT B-DCU Operating Instructions Manual (85037-549-98)          | Sartorius Stedim Biotech                 | s.f. (manual vigente) | Manual técnico     | https://www.manualslib.com/manual/3061881/Sartorius-Stedim-Biotech-Biostat-B-Dcu.html                  | Define uso previsto como unidad de control para cultivar cultivos biológicos bajo condiciones controladas | Include             |
| DOC-04       | Univessel® Glass – Reliability and Continuity (brochure)            | Sartorius AG                             | 2022-06-28            | Brochure técnico   | https://www.sartorius.com (referenciado)                                                               | Especifica vasos 1 L, 2 L, 5 L, 10 L, volúmenes totales y de trabajo                                      | Include             |

Fuentes verificadas en búsqueda: DOC-01, DOC-02, DOC-03, DOC-04 fecha confirmada.

## 5. Evaluación de documentos candidatos

| ID documento | Relevancia | Autoridad | Trazabilidad | Cobertura de la pregunta                            | Evidencia localizable        | Justificación                                                |
| ------------ | ---------- | --------- | ------------ | --------------------------------------------------- | ---------------------------- | ------------------------------------------------------------ |
| DOC-01       | Alta       | Alta      | Alta         | Define BioLector XT y operación en MTP              | Sí – párrafos introductorios | Fuente oficial fabricante, describe propósito y formato      |
| DOC-02       | Alta       | Alta      | Media        | Complementa definición con sensores y microfluídica | Sí – secciones ventajas      | Página oficial, sin fecha pero contenido técnico consistente |
| DOC-03       | Alta       | Alta      | Alta         | Define bioreactor/fermenter y uso previsto          | Sí – sección Intended Use    | Manual oficial Sartorius, aplicable a 5 L/10 L               |
| DOC-04       | Alta       | Alta      | Alta         | Especifica escalas 5 L y 10 L, volúmenes            | Sí – extractos catálogo      | Brochure 2022, datos numéricos verificables                  |

## 6. Corpus documental seleccionado

| ID documento | Documento seleccionado                             | Pregunta asociada | Fragmentos o páginas relevantes                                       | Estado       |
| ------------ | -------------------------------------------------- | ----------------- | --------------------------------------------------------------------- | ------------ |
| DOC-01       | Using the BioLector XT Microbioreactor Gassing Lid | ALC-01            | Introducción: definición de microbioreactor; págs. 1-2                | Seleccionado |
| DOC-02       | Advantages & Applications BioLector XT             | ALC-01            | "High-throughput microbioreactor enables..."; formato MTP             | Seleccionado |
| DOC-03       | BIOSTAT B-DCU Operating Instructions               | ALC-01            | Intended Use; Device Overview págs. 11, 17                            | Seleccionado |
| DOC-04       | Univessel Glass brochure                           | ALC-01            | "available in 1 L, 2 L, 5 L and 10 L working volume"; tabla volúmenes | Seleccionado |

## 7. Respuesta basada en evidencia

**Evidencia explícita:**

- BioLector XT es definido por el fabricante como "a benchtop device for highthroughput screening of microbial cultivations in combination with onlinemonitoring of common cultivation parameters such as biomass, pH, dissolved oxygen (DO) and fluorescence". Las cultivaciones se realizan en placas microtiter formato SBS/SLAS con 32 o 48 pozos, "allowing up to 48 simultaneous experiments in one microbioreactor run".
- La página de ventajas añade que es "based on a standard ANSI/SLAS (SBS) microtiter plate (MTP) format, and operates with online, pre-calibrated optical sensors", y que es un "High-throughput microbioreactor enables real-time evaluation of biomass, fluorescence, pH, dissolved oxygen in the liquid phase (DO)".
- Para Sartorius, el BIOSTAT B-DCU se describe como "used as the control unit for various bioreactor systems in combination with the UniVessel Glass or UniVessel SU. This control unit is used to cultivate biological cultures in liquids or aqueous nutrient solutions under controlled and reproducible conditions".
- Además, "The device is designed for cultivating microorganisms and cells in discontinuous and continuous processes. It was designed for cultivating microorganisms and cells at various reactor volumes".
- El vaso UniVessel Glass es "our platform cultivation vessel for all Biostat® benchtop bioreactors. It is available in 1 L, 2 L, 5 L and 10 L working volume". La ficha técnica detalla: Total volume 1.6, 3, 6.6, 13; Working volume 0.35–1, 0.6–2, 0.6–5, 1.5–10. La versión 5 L tiene 6.6 L totales y 0.6–5 L de trabajo; la 10 L tiene 13 L totales y 1.5–10 L de trabajo.[L]
- Sartorius confirma que el vaso está disponible como "2 L, 5 L and 10 L version".

**Inferencia razonable basada en evidencia:**

- Dentro del proyecto, "biorreactor" debe entenderse no como un único tipo de equipo, sino como una familia funcional: sistema que permite cultivar microorganismos o células en medio líquido bajo condiciones controladas y reproducibles, con monitoreo en línea, y que existe en tres realizaciones:
  1. **Microbiorreactor de alto rendimiento** (BioLector XT): escala mililitros por pozo, formato MTP, sensores ópticos precalibrados.
  2. **Biorreactor de banco** (Sartorius BIOSTAT B-DCU + UniVessel Glass 5 L)
  3. **Biorreactor de banco** (Sartorius BIOSTAT B-DCU + UniVessel Glass 10 L)

**Información no establecida en el corpus:**

- No se encontró en los documentos una definición explícita del término "biorreactor" que integre simultáneamente las tres plataformas; la definición unificada es construcción del proyecto.
- Volúmenes exactos por pozo del BioLector XT (ej. 800-1000 µL) no están en los fragmentos recuperados; se requeriría manual completo.
- Año de publicación de DOC-01, DOC-02 y DOC-03 no verificable en las fuentes consultadas.

## 8. Tabla de afirmaciones y evidencia

| ID evidencia | Afirmación                                                                                                                               | Tipo de evidencia | Documento                | Página/sección         | Fragmento o resumen fiel                                                                                                    | Confianza | Validación experta                      |
| ------------ | ---------------------------------------------------------------------------------------------------------------------------------------- | ----------------- | ------------------------ | ---------------------- | --------------------------------------------------------------------------------------------------------------------------- | --------- | --------------------------------------- |
| EV-01        | BioLector XT es un dispositivo de sobremesa para screening de alto rendimiento con monitoreo en línea de biomasa, pH, DO y fluorescencia | Explícita         | DOC-01                   | Introducción           | "benchtop device for highthroughput screening... with onlinemonitoring"                                                     | Alta      | No requerida                            |
| EV-02        | BioLector XT opera en placas MTP de 32 o 48 pozos, hasta 48 experimentos simultáneos                                                     | Explícita         | DOC-01                   | Introducción           | "up to 48 simultaneous experiments in one microbioreactor run"                                                              | Alta      | No requerida                            |
| EV-03        | BioLector XT usa formato ANSI/SLAS y sensores ópticos precalibrados                                                                      | Explícita         | DOC-02                   | Ventajas               | "based on a standard ANSI/SLAS... operates with online, pre-calibrated optical sensors"                                     | Alta      | No requerida                            |
| EV-04        | BIOSTAT B-DCU se usa para cultivar cultivos biológicos en líquidos bajo condiciones controladas y reproducibles                          | Explícita         | DOC-03                   | Intended Use           | "used to cultivate biological cultures in liquids... under controlled and reproducible conditions"                          | Alta      | No requerida                            |
| EV-05        | BIOSTAT está diseñado para microorganismos y células en procesos discontinuos y continuos a varios volúmenes                             | Explícita         | DOC-03                   | Device Overview        | "designed for cultivating microorganisms and cells in discontinuous and continuous processes... at various reactor volumes" | Alta      | No requerida                            |
| EV-06        | UniVessel Glass disponible en 5 L y 10 L volumen de trabajo                                                                              | Explícita         | DOC-04                   | Catálogo               | "available in 1 L, 2 L, 5 L and 10 L working volume"                                                                        | Alta      | No requerida                            |
| EV-07        | Volumen total 5 L = 6.6 L, trabajo 0.6–5 L; 10 L = 13 L total, trabajo 1.5–10 L                                                          | Explícita         | DOC-04                   | Tabla especificaciones | "Total volume... 6.6 13... Working volume... 0.6–5 1.5–10"                                                                  | Alta      | Requiere validación con manual completo |
| EV-08        | Biorreactor en proyecto integra tres realizaciones escalables con función común de cultivo controlado                                    | Inferida          | Síntesis DOC-01 a DOC-04 | –                      | Integración conceptual para ontología                                                                                       | Media     | Requiere validación experta             |

[L]

## 9. Conceptos ontológicos candidatos

| Concepto candidato | Tipo sugerido          | Definición basada en evidencia                                                                     | Fuente asociada | Estado    |
| ------------------ | ---------------------- | -------------------------------------------------------------------------------------------------- | --------------- | --------- |
| Bioreactor         | Clase                  | Sistema para cultivar cultivos biológicos en líquidos bajo condiciones controladas y reproducibles | DOC-03          | Candidato |
| Microbioreactor    | Subclase de Bioreactor | Biorreactor de sobremesa de alto rendimiento en formato MTP con monitoreo óptico en línea          | DOC-01, DOC-02  | Candidato |
| BenchtopBioreactor | Subclase de Bioreactor | Biorreactor de banco con vaso de vidrio autoclavable y unidad de control                           | DOC-03          | Candidato |
| BioLectorXT        | Individuo              | Instancia de Microbioreactor de Beckman Coulter                                                    | DOC-01          | Candidato |
| BiostatB_DCU       | Individuo              | Unidad de control Sartorius para sistemas de biorreactor                                           | DOC-03          | Candidato |
| UniVesselGlass_5L  | Individuo              | Vaso de cultivo 5 L, volumen trabajo 0.6–5 L                                                       | DOC-04          | Candidato |
| UniVesselGlass_10L | Individuo              | Vaso de cultivo 10 L, volumen trabajo 1.5–10 L                                                     | DOC-04          | Candidato |
| CultivationVessel  | Clase                  | Recipiente donde ocurre el cultivo (MTP, vaso de vidrio)                                           | DOC-01, DOC-04  | Candidato |
| hasWorkingVolume   | Propiedad de dato      | Rango de volumen operativo en litros                                                               | DOC-04          | Candidato |

## 10. Relaciones ontológicas candidatas

| Relación candidata     | Dominio sugerido | Rango sugerido    | Significado                                  | Evidencia asociada | Estado              |
| ---------------------- | ---------------- | ----------------- | -------------------------------------------- | ------------------ | ------------------- |
| cultivates             | Bioreactor       | BiologicalCulture | El sistema cultiva microorganismos o células | DOC-03             | Candidato           |
| hasMonitoringParameter | Bioreactor       | Parameter         | Monitorea biomasa, pH, DO, fluorescencia     | DOC-01, DOC-02     | Candidato           |
| hasCultivationVessel   | Bioreactor       | CultivationVessel | Usa MTP o vaso de vidrio                     | DOC-01, DOC-04     | Candidato           |
| operatesInFormat       | Microbioreactor  | PlateFormat       | Formato ANSI/SLAS MTP                        | DOC-02             | Candidato           |
| hasScale               | Bioreactor       | OperationalScale  | microescala vs banco                         | Inferida           | Requiere validación |

## 11. Triadas RDF candidatas

- BioLectorXT -> rdf:type -> Microbioreactor — Documento: DOC-01, sección Introducción — Estado: soportada
- BioLectorXT -> hasMonitoringParameter -> DissolvedOxygen — DOC-01 — soportada
- BioLectorXT -> operatesInFormat -> SBS_MTP_48 — DOC-02 — soportada
- BiostatB_DCU -> rdf:type -> BenchtopBioreactor — DOC-03 — soportada
- BiostatB_DCU -> cultivates -> MicroorganismOrCellCulture — DOC-03 — soportada
- UniVesselGlass_5L -> hasWorkingVolume -> "0.6-5 L"^^xsd:string — DOC-04 — soportada
- UniVesselGlass_10L -> hasWorkingVolume -> "1.5-10 L"^^xsd:string — DOC-04 — soportada
- Bioreactor -> hasSubclass -> Microbioreactor — inferida del proyecto — requiere validación experta

## 12. Sinónimos y variantes terminológicas

| Término principal  | Sinónimos o variantes documentadas                                 | Idioma | Documento de soporte |
| ------------------ | ------------------------------------------------------------------ | ------ | -------------------- |
| Bioreactor         | Fermenter, bioreactor system                                       | en     | DOC-03               |
| Microbioreactor    | high-throughput microbioreactor, microtiter plate based bioreactor | en     | DOC-01, DOC-02       |
| Cultivation vessel | process vessel, UniVessel Glass                                    | en     | DOC-04               |
| Working volume     | volumen de trabajo                                                 | en/es  | DOC-04               |

## 13. Vacíos, riesgos y decisiones pendientes

- Información faltante: definición normativa ISO o ASTM de biorreactor no incluida; volúmenes por pozo exactos del BioLector XT; año de publicación de manuales.
- Ambigüedades: "bioreactor" vs "fermenter" usados indistintamente en DOC-03; necesidad de decidir si son sinónimos en ontología.
- Configuraciones dependientes: BioLector XT con/sin módulo microfluídico cambia capacidades de alimentación; Sartorius 5 L/10 L con pared simple o doble.
- Validación experta requerida para la triada de integración funcional y para rangos de volumen.
- Documentos adicionales necesarios: manual completo BioLector XT (User Manual), datasheet oficial UniVessel Glass 2022 PDF completo, SOP interno del proyecto.

## 14. Registro metodológico para el documento de investigación

Se analizó la pregunta ALC-01 mediante búsqueda dirigida en fuentes oficiales de Beckman Coulter y Sartorius. La estrategia combinó términos en inglés para captar documentación técnica ("BioLector XT microbioreactor", "BIOSTAT B-DCU", "Univessel Glass 5 L 10 L"). Se recuperaron cuatro documentos verificables: dos notas/páginas de Beckman que definen el BioLector XT como microbiorreactor de alto rendimiento en formato MTP con sensores ópticos, el manual de operación del BIOSTAT B-DCU que establece el uso previsto para cultivo controlado de microorganismos y células, y el brochure de UniVessel Glass de 2022 que especifica volúmenes de trabajo para 5 L (0.6–5 L) y 10 L (1.5–10 L). Los criterios de inclusión priorizaron autoría de fabricante y trazabilidad. La evidencia extraída permitió proponer una definición unificada de biorreactor como sistema de cultivo controlado, con tres realizaciones escalables. Se identificaron conceptos candidatos (Bioreactor, Microbioreactor, BenchtopBioreactor) y relaciones (cultivates, hasMonitoringParameter). Las limitaciones incluyen ausencia de fechas en tres documentos y falta de especificación detallada por pozo.

## 15. Estado final

- **Nivel de confianza general:** Medio (evidencia sólida de fabricantes, pero falta integración normativa y fechas)
- **Estado de la respuesta:** Parcialmente soportada (definición funcional soportada, unificación es inferencia)
- **Estado del corpus:** Parcial (suficiente para definición inicial, insuficiente para ontología detallada)
- **Próxima acción recomendada:** Obtener manuales completos de BioLector XT y BIOSTAT B-DCU con fechas, y validar con experto de bioprocesos la definición unificada y las equivalencias funcionales entre escalas.
