## 1. Identificación de la pregunta

- **ID:** ALC-04
- **Nivel metodológico:** conceptualización ontológica preliminar
- **Tema:** componentes comunes para modelado OWL/RDF
- **Pregunta:** ¿Qué componentes comunes permiten describir estos tres biorreactores en una misma ontología?

## 2. Propósito de la pregunta

Busca identificar los elementos estructurales y funcionales compartidos entre BioLector XT, Sartorius Biostat B 5 L y Biostat B 10 L, para definir clases, propiedades y relaciones reutilizables. El resultado alimenta el corpus documental y la base ontológica preliminar, evitando modelar cada equipo como silo independiente y facilitando equivalencias funcionales entre escalas.

## 3. Plan de búsqueda documental

**Información técnica requerida:**

- arquitectura del sistema, recipiente de cultivo, volumen operativo
- sistemas de agitación, control térmico, sensado pH/DO, aireación, alimentación
- software de control y adquisición

**Tipos de documentos necesarios:**

- fichas técnicas y manuales oficiales de fabricante
- artículos científicos revisados por pares que usen los tres sistemas en cadena de escalado

**Repositorios sugeridos:**

- beckman.com, m2p-labs.com, sartorius.com
- PMC, MDPI Bioengineering, Nature Scientific Reports

**Términos de búsqueda:**

- ES: "BioLector XT ficha técnica", "Biostat B-DCU 5 L 10 L especificaciones"
- EN: "BioLector XT technical data sheet", "Biostat B-DCU brochure 5L 10L", "BioLector XT Biostat scale-down"

**Criterios de inclusión y exclusión:** ver sección del prompt maestro; priorizar 2021-2026 y manuales vigentes.

## 4. Documentos candidatos encontrados

| ID documento | Título                                                                                             | Entidad autora                           | Año                                       | Tipo de fuente              | URL/DOI verificable                                                                                      | Relación con la pregunta                                                        | Decisión preliminar                                                   |
| ------------ | -------------------------------------------------------------------------------------------------- | ---------------------------------------- | ----------------------------------------- | --------------------------- | -------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- | --------------------------------------------------------------------- |
| DOC-01       | BioLector XT Technical Data Sheet                                                                  | Beckman Coulter Life Sciences / m2p-labs | n.d. (documento vigente, consultado 2026) | ficha técnica oficial       | https://www.beckman.es/resources/reading-material/product-instructions/biolector-xt-technical-data-sheet | especifica temperatura, agitación, pH, DO, gases, alimentación, volúmenes       | Include                                                               |
| DOC-02       | Biostat® B-DCU Brochure                                                                            | Sartorius Stedim Biotech GmbH            | 2025 (©2025, last modified 06 2025)		| brochure técnico oficial   | https://www.sartorius.com/download/82806/broch-biostat-b-dcu-sbi1555-e-data.pdf | describe Biostat B-DCU, vasos 1–10 L, sensores, bombas, controladores | Include |
| DOC-03       | Optimizing Yeast Surface-Displayed Unspecific Peroxygenase Production for Sustainable Biocatalysis | MDPI Bioengineering / PMC                | 2025                                      | artículo revisado por pares | https://pmc.ncbi.nlm.nih.gov/articles/PMC12383419/                                                       | usa BioLector XT (1–2 mL) y Biostat B5 (5 L) en misma cadena de escalado        | Include                                                               |

## 5. Evaluación de documentos candidatos

| ID documento | Relevancia | Autoridad | Trazabilidad | Cobertura de la pregunta | Evidencia localizable                           | Justificación                                                      |
| ------------ | ---------- | --------- | ------------ | ------------------------ | ----------------------------------------------- | ------------------------------------------------------------------ |
| DOC-01       | Alta       | Alta      | Alta         | Media                    | especificaciones tabuladas de componentes       | fabricante directo, detalla sistemas comunes                       |
| DOC-02       | Alta       | Alta      | Alta         | Alta                     | tablas de sensores, velocidades, vasos 5 L/10 L | brochure oficial 2025 con datos verificables                       |
| DOC-03       | Media      | Alta      | Alta         | Media                    | descripción de uso paralelo de escalas          | peer-reviewed, confirma equivalencia funcional en flujo de trabajo |

## 6. Corpus documental seleccionado

| ID documento | Documento seleccionado            | Pregunta asociada | Fragmentos o páginas relevantes                                                                                       | Estado   |
| ------------ | --------------------------------- | ----------------- | --------------------------------------------------------------------------------------------------------------------- | -------- |
| DOC-01       | BioLector XT Technical Data Sheet | ALC-04            | temperatura 10–50°C; agitación 100–1500 rpm; pH 4–7.5; DO 0–100%; módulos O2/CO2                                      | Incluido |
| DOC-02       | Biostat B-DCU Brochure            | ALC-04            | vasos 5 L y 10 L; velocidades 5 L 20–1500 rpm, 10 L 20–800 rpm; sensores pH 2–12, DO 0–100%; bombas hasta 4 variables | Incluido |
| DOC-03       | Artículo MDPI 2025                | ALC-04            | uso BioLector XT y Biostat B5 en misma investigación; Biostat B5 con dos turbinas Rushton                             | Incluido |

## 7. Respuesta basada en evidencia

**Evidencia explícita:**
Los tres sistemas comparten una arquitectura funcional descrita en documentos oficiales. Ambos fabricantes definen un recipiente de cultivo con volumen nominal: BioLector XT trabaja con placas de 48 pocillos (800–1900 µL FlowerPlate, 1000–2400 µL Round Well); Biostat B-DCU acepta Univessel® Glass de 5 L y 10 L. El control térmico está presente en ambos: 10–50 °C en BioLector y Pt100 con rango 0–150 °C (control 0–80 °C) en Sartorius, con potencias específicas para 5 L (400 W) y 10 L (780 W).

La agitación es un componente común: BioLector 100–1500 rpm; Sartorius 5 L 20–1500 rpm y 10 L 20–800 rpm. El sensado de pH y oxígeno disuelto aparece en ambos con rangos solapados: pH 4–7.5 (optodos) frente a 2–12 (electrodo); DO 0–100 % en ambos y.

El manejo de gases es explícito: BioLector ofrece módulos de O2 (1–100 %) y CO2 (0–12 %) con módulos de up/down regulation; Sartorius integra controladores de flujo másico 1:200 y flujo máximo 20 lpm por línea, con mezcla de 2 gases para microbial y 4 gases para cultivo celular.

La alimentación controlada también es compartida: BioLector dispone de dos líneas de alimentación, control PI y perfiles dV/dt = A + B·t + C·e^{D·t}, con bomba hasta 665 strokes/h; Sartorius permite hasta cuatro bombas de velocidad variable Watson-Marlow 114.

El software de supervisión aparece en ambos contextos: el artículo de 2025 describe el uso paralelo de BioLector XT con módulo microfluídico y Biostat B5 dentro del mismo flujo de escalado, mientras el brochure de Sartorius menciona integración con Biobrain® Supervise.

**Inferencia razonable basada en evidencia:**
Estos elementos permiten abstraer clases comunes: sistema de contención, sistema de agitación, sistema de control térmico, sensores de pH y DO, sistema de gas, sistema de alimentación y controlador de proceso. La coincidencia de rangos operativos (temperatura, DO, agitación) sugiere que una ontología puede modelar propiedades de dato compartidas y especializar rangos por escala.

**Información no establecida en el corpus:**
No hay evidencia explícita en DOC-01 sobre sensores de espuma, nivel o presión presentes en DOC-02. Tampoco se documenta en el corpus la equivalencia exacta de estrategias de control de alarmas entre BioLector y Biostat, ni la geometría detallada de impulsores más allá de "dos turbinas Rushton" en Biostat B5.

## 8. Tabla de afirmaciones y evidencia

| ID evidencia | Afirmación                                   | Tipo de evidencia | Documento      | Página/sección   | Fragmento o resumen fiel                                  | Confianza | Validación experta |
| ------------ | -------------------------------------------- | ----------------- | -------------- | ---------------- | --------------------------------------------------------- | --------- | ------------------ |
| E01          | Ambos sistemas tienen control de temperatura | Explícita         | DOC-01, DOC-02 | ficha técnica    | BioLector 10–50°C; Sartorius Pt100 0–150°C control 0–80°C | Alta      | No                 |
| E02          | Ambos miden pH y DO en rango 0–100% DO       | Explícita         | DOC-01, DOC-02 | sensores         | pH 4–7.5 vs 2–12; DO 0–100% ambos                         | Alta      | No                 |
| E03          | Ambos poseen agitación regulable             | Explícita         | DOC-01, DOC-02 | especificaciones | 100–1500 rpm vs 20–1500 rpm (5L) / 20–800 rpm (10L)       | Alta      | No                 |
| E04          | Ambos integran control de gases con MFC      | Explícita         | DOC-01, DOC-02 | módulos          | O2/CO2 modules vs MFC 1:200, 20 lpm                       | Alta      | No                 |
| E05          | Ambos permiten alimentación programada       | Explícita         | DOC-01, DOC-02 | feeding          | perfiles dV/dt y 2 líneas vs 4 bombas variables           | Alta      | No                 |
| E06          | Se usan conjuntamente en escalado            | Explícita         | DOC-03         | métodos          | BioLector 1–2 mL y Biostat B5 5 L en mismo estudio        | Alta      | No                 |

## 9. Conceptos ontológicos candidatos

| Concepto candidato       | Tipo sugerido | Definición basada en evidencia                                                                   | Fuente asociada        | Estado    |
| ------------------------ | ------------- | ------------------------------------------------------------------------------------------------ | ---------------------- | --------- |
| BioreactorSystem         | Clase         | sistema que integra recipiente, agitación, control térmico, sensores y alimentación para cultivo | DOC-01, DOC-02         | candidato |
| Microbioreactor          | Subclase      | BioreactorSystem de volúmenes microlitro con placas de 48 pocillos                               | DOC-01                 | candidato |
| StirredTankBioreactor    | Subclase      | BioreactorSystem con vaso agitado de 5–10 L                                                      | DOC-02                 | candidato |
| CultureVessel            | Clase         | contenedor donde ocurre el cultivo                                                               | DOC-01, DOC-02         | candidato |
| TemperatureControlSystem | Clase         | sistema que regula temperatura del cultivo                                                       | DOC-01, DOC-02         | candidato |
| AgitationSystem          | Clase         | mecanismo que imparte movimiento al cultivo                                                      | DOC-01, DOC-02         | candidato |
| pHSensor                 | Clase         | sensor óptico o electroquímico para pH                                                           | DOC-01, DOC-02         | candidato |
| DissolvedOxygenSensor    | Clase         | sensor para DO 0–100%                                                                            | DOC-01, DOC-02         | candidato |
| GasSupplySystem          | Clase         | módulos y MFC para O2, CO2, N2, aire                                                             | DOC-01, DOC-02         | candidato |
| FeedSystem               | Clase         | bombas y líneas para alimentación y control pH                                                   | DOC-01, DOC-02         | candidato |
| ProcessController        | Clase         | controlador PI/PID y software de supervisión                                                     | DOC-01, DOC-02, DOC-03 | candidato |

## 10. Relaciones ontológicas candidatas

| Relación candidata    | Dominio sugerido | Rango sugerido           | Significado                       | Evidencia asociada | Estado    |
| --------------------- | ---------------- | ------------------------ | --------------------------------- | ------------------ | --------- |
| hasVessel             | BioreactorSystem | CultureVessel            | el sistema contiene un recipiente | DOC-01, DOC-02     | candidato |
| hasAgitationSystem    | BioreactorSystem | AgitationSystem          | equipa sistema de agitación       | E03                | candidato |
| hasTemperatureControl | BioreactorSystem | TemperatureControlSystem | regula temperatura                | E01                | candidato |
| measuresWith          | BioreactorSystem | pHSensor                 | mide pH                           | E02                | candidato |
| measuresWith          | BioreactorSystem | DissolvedOxygenSensor    | mide DO                           | E02                | candidato |
| hasGasSupply          | BioreactorSystem | GasSupplySystem          | suministra gases                  | E04                | candidato |
| hasFeedSystem         | BioreactorSystem | FeedSystem               | permite alimentación              | E05                | candidato |
| isScaleDownOf         | Microbioreactor  | StirredTankBioreactor    | relación de escalado funcional    | DOC-03             | candidato |

## 11. Triadas RDF candidatas

- BioLectorXT -> hasVessel -> MicrotiterPlate48 – soportada – DOC-01, sección placas
- BiostatB5L -> hasVessel -> UnivesselGlass5L – soportada – DOC-02
- BiostatB10L -> hasVessel -> UnivesselGlass10L – soportada – DOC-02
- BioLectorXT -> hasAgitationSystem -> ShakingSystem100-1500rpm – soportada – DOC-01
- BiostatB5L -> hasAgitationSystem -> Stirrer20-1500rpm – soportada – DOC-02
- Ambos -> measuresWith -> DissolvedOxygenSensor – parcialmente soportada – requiere validación de equivalencia de tecnología óptica vs polarográfica

## 12. Sinónimos y variantes terminológicas

| Término principal | Sinónimos o variantes documentadas   | Idioma | Documento de soporte |
| ----------------- | ------------------------------------ | ------ | -------------------- |
| Microbioreactor   | microbioreactor, BioLector XT        | EN     | DOC-01, DOC-03       |
| Bioreactor        | fermenter, bioreactor, BIOSTAT B-DCU | EN     | DOC-02               |
| FeedSystem        | feeding options, pump module         | EN     | DOC-01, DOC-02       |
| GasSupplySystem   | gassing lid, aeration module, MFC    | EN     | DOC-01, DOC-02       |

## 13. Vacíos, riesgos y decisiones pendientes

- Falta evidencia en DOC-01 sobre sensores de espuma, nivel, presión y biomasa capacitiva presentes en DOC-02; no asumir equivalencia.
- Ambigüedad terminológica: "microfluidic module" en BioLector vs "pump module" en Sartorius; requiere mapeo funcional.
- Configuraciones dependientes del equipo: rangos de pH difieren (4–7.5 vs 2–12); modelar como restricciones de individuo, no de clase.
- Necesidad de manuales completos de BioLector XT para confirmar alarmas y eventos.
- Validación experta requerida para definir si "triggered pH control" equivale a lazo PID del Biostat.

## 14. Registro metodológico para el documento de investigación

Se analizó la pregunta ALC-04 mediante búsqueda dirigida en fuentes oficiales de Beckman Coulter y Sartorius, complementada con un artículo peer-reviewed de 2025 que emplea ambos equipos en escalado. Se seleccionaron tres documentos verificables que describen componentes técnicos explícitos. La evaluación mostró alta autoridad y trazabilidad. La extracción identificó siete componentes comunes (recipiente, control térmico, agitación, sensores pH/DO, suministro de gas, alimentación y controlador) que sustentan clases y relaciones candidatas en inglés. Las limitaciones incluyen ausencia de datos sobre sensores auxiliares en BioLector y necesidad de validación de equivalencias funcionales.

## 15. Estado final

- Nivel de confianza general: Medio
- Estado de la respuesta: Parcialmente soportada
- Estado del corpus: Parcial
- Próxima acción recomendada: suministrar manuales completos de BioLector XT (Operating Manual) y de Biostat B 5 L/10 L (Operating Instructions) para completar evidencia sobre alarmas, eventos y sensores auxiliares, y validar triadas RDF con expertos de proceso.
