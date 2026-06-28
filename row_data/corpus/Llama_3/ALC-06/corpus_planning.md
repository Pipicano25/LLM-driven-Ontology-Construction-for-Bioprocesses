## 1. Identificación de la pregunta

- **ID:** ALC-06
- **Nivel metodológico:** Definición de alcance ontológico
- **Tema:** Propiedades transversales de biorreactores
- **Pregunta:** ¿Qué propiedades generales deben describir cualquier biorreactor del proyecto, independientemente de su escala o volumen?

## 2. Propósito de la pregunta

Busca establecer el conjunto mínimo de atributos que permitan comparar BioLector XT, Sartorius 5 L y 10 L en una misma ontología OWL/RDF. Aporta al corpus la base para clases comunes (equipo, vaso, sensor, actuador) y evita modelar cada escala como un dominio aislado.

## 3. Plan de búsqueda documental

**Información técnica requerida**

- Definición de vaso, volumen de trabajo y volumen total
- Rangos operativos de temperatura, agitación y aireación
- Capacidades de medida y control (pH, DO, biomasa)
- Materiales y esterilidad
- Interfaces de datos y modos de proceso

**Tipos de documentos**

- Manuales y notas técnicas oficiales de fabricante
- Folletos con especificaciones
- Application notes con parámetros operativos

**Repositorios sugeridos**

- beckman.com / media.beckman.com (m2p-labs)
- sartorius.com (descargas técnicas)
- pdf.directindustry.com (catálogos verificados)

**Términos de búsqueda**

- ES: "BioLector XT especificaciones", "Biostat B 5 L manual"
- EN: "BioLector XT microbioreactor specifications", "Biostat B-DCU operating instructions", "Univessel Glass 5L 10L datasheet"

**Criterios**

- Inclusión: autoría fabricante, fecha 2021-2026, tablas de especificaciones
- Exclusión: blogs, distribuidores sin PDF original, documentos sin trazabilidad

## 4. Documentos candidatos encontrados

| ID documento | Título                                                                  | Entidad autora                           | Año                    | Tipo de fuente  | URL/DOI verificable                                                                                    | Relación con la pregunta                                   | Decisión preliminar |
| ------------ | ----------------------------------------------------------------------- | ---------------------------------------- | ---------------------- | --------------- | ------------------------------------------------------------------------------------------------------ | ---------------------------------------------------------- | ------------------- |
| DOC-01       | Using the BioLector XT Microbioreactor Gassing Lid – Technical Note     | Beckman Coulter Life Sciences (m2p-labs) | 2021 (rev.)            | Nota técnica    | https://media.beckman.com/-/media/m2p-labs/pdfs/using-the-biolector-xt-microbioreactor-gassing-lid.pdf | Describe monitoreo online y modos de gasificación          | Include             |
| DOC-02       | BIOLECTOR XT Microbioreactor – Brochure                                 | Beckman Coulter Life Sciences            | s.f. (consultado 2024) | Folleto técnico | https://media.beckman.com/-/media/pdf-assets/brochures/biolector-xt-microbioreactor-brochure.ashx      | Especifica volúmenes, rangos pH/DO, temperatura, agitación | Include             |
| DOC-03       | Biostat® B – The Multi-Talented Bioreactor for Research and Development | Sartorius Stedim Biotech GmbH            | 2022                   | Folleto técnico | https://www.sartorius.com/download/34576/5/broch-biostat-b-sbi1513-e-1--data.pdf                       | Define vasos 1–10 L, materiales, modos de proceso          | Include             |
| DOC-04       | Biostat® B-DCU – Industry Standard Bioreactor                           | Sartorius Stedim Biotech GmbH            | 2021                   | Folleto técnico | https://www.sartorius.com/download/12080/5/broch-biostat-b-dcu-sbi1555-e-data.pdf                      | Detalla sensores, rangos, control, bombas                  | Include             |

Publicación DOC-03: SBI1513-e Status 04|14|2022. Publicación DOC-04: SBI1555-e Status 05|20|2021.

## 5. Evaluación de documentos candidatos

| ID documento | Relevancia | Autoridad | Trazabilidad                                                                                                   | Cobertura de la pregunta             | Evidencia localizable                                                                                               | Justificación                             |
| ------------ | ---------- | --------- | -------------------------------------------------------------------------------------------------------------- | ------------------------------------ | ------------------------------------------------------------------------------------------------------------------- | ----------------------------------------- |
| DOC-01       | Alta       | Alta      | Alta                                                                                                           | Media                                | Descripción de monitoreo online biomass, pH, DO; flujo gas 5–50 mL/min                                              | Fuente oficial, detalla funciones comunes |
| DOC-02       | Alta       | Alta      | Alta                                                                                                           | Alta                                 | Volumen 800–2400 µL; temperatura 8°C bajo ambiente a 50°C; agitación 100–1500 rpm; pH 5.0–7.5; DO 0–100%            | Especificaciones completas escala micro   |
| DOC-03       | Alta       | Alta      | Vasos 1,2,5,10 L; materiales vidrio borosilicato, AISI 316L, EPDM; modos batch, fed-batch, continuo, perfusión | Define familia de vasos del proyecto |
| DOC-04       | Alta       | Alta      | Alta                                                                                                           | Alta                                 | Temperatura Pt100 0–150°C (control 0–80°C); pH 2–12; DO 0–100%; velocidades agitador 5L 20–1500 rpm, 10L 20–800 rpm | Aporta rangos comparables a microescala   |

## 6. Corpus documental seleccionado

| ID documento | Documento seleccionado     | Pregunta asociada | Fragmentos o páginas relevantes              | Estado   |
| ------------ | -------------------------- | ----------------- | -------------------------------------------- | -------- |
| DOC-01       | Technical Note Gassing Lid | ALC-06            | p.1 monitoreo online; p.1 flujos             | Incluido |
| DOC-02       | Brochure BioLector XT      | ALC-06            | System Performance; Technical Specifications | Incluido |
| DOC-03       | Brochure Biostat B         | ALC-06            | Univessel Glass 5L/10L; materiales           | Incluido |
| DOC-04       | Brochure Biostat B-DCU     | ALC-06            | Process Control/Sensors; aeration            | Incluido |

## 7. Respuesta basada en evidencia

**Evidencia explícita**

Tanto el sistema micro como los benchtop comparten la necesidad de describir:

- capacidad de medida online de biomasa, pH y oxígeno disuelto. BioLector XT lo declara como "online monitoring of common cultivation parameters such as biomass, pH, dissolved oxygen (DO)". Sartorius lista sensores reutilizables pH 2–12 y DO 0–100%.
- rangos de volumen de trabajo definidos por el vaso. BioLector: 800–2400 µL. Sartorius 5 L: 0.6–5 L, 10 L: 1.5–10 L, volúmenes totales 6.6 L y 13 L.
- control de temperatura. BioLector: 8°C bajo ambiente hasta 50°C. Sartorius: control 0–80°C.
- sistema de agitación. BioLector: shaking 100–1500 rpm. Sartorius: 5L 20–1500 rpm, 10L 20–800 rpm.
- aireación con gases definidos. BioLector: atmósfera controlada CO2, O2. Sartorius: líneas para Air, O2, N2, CO2.
- control de pH por ácido/base. BioLector: "pH control By acid or/and alkali". Sartorius: "automatic acid and base addition or by CO₂ aeration".
- modos de proceso. Sartorius: batch, fed-batch, continuous, perfusion. BioLector soporta batch y fed-batch con alimentación flexible.
- materiales en contacto. Sartorius: vidrio borosilicato, acero AISI 316L, EPDM. BioLector: tecnología desechable con placas precalibradas.
- interfaz de datos. BioLector: Ethernet. Sartorius: conectividad a BioPAT MFCS o SCADA.

**Inferencia razonable basada en evidencia**
Aunque las escalas difieren en órdenes de magnitud, ambas arquitecturas requieren describir: identificación del equipo, geometría del vaso, límites operativos, conjunto de sensores/actuadores, estrategia de control y trazabilidad de datos. La coincidencia en parámetros medidos (pH, DO, temperatura) sugiere que son propiedades generales, no específicas de escala.

**Información no establecida en el corpus**

- Definición formal de alarmas y fallas para BioLector XT
- Límites de presión y validación de esterilidad para Sartorius 10 L
- Equivalencias exactas de kLa entre micro y benchtop (BioLector menciona 30–600 h⁻¹, sin contraparte Sartorius en los documentos)

## 8. Tabla de afirmaciones y evidencia

| ID evidencia | Afirmación                                                                     | Tipo de evidencia | Documento      | Página/sección   | Fragmento o resumen fiel                                                                        | Confianza | Validación experta       |
| ------------ | ------------------------------------------------------------------------------ | ----------------- | -------------- | ---------------- | ----------------------------------------------------------------------------------------------- | --------- | ------------------------ |
| E01          | Todo biorreactor debe describir capacidad de medida online de biomasa, pH y DO | Explícita         | DOC-01         | Introducción     | "online monitoring of common cultivation parameters such as biomass, pH, dissolved oxygen (DO)" | Alta      | No requerida             |
| E02          | Rango de volumen de trabajo es propiedad esencial                              | Explícita         | DOC-02, DOC-03 | Especificaciones | BioLector 800–2400 µL; Sartorius 5L 0.6–5 L                                                     | Alta      | No requerida             |
| E03          | Control de temperatura con límites definidos                                   | Explícita         | DOC-02, DOC-04 | Technical data   | BioLector hasta 50°C; Sartorius 0–80°C                                                          | Alta      | No requerida             |
| E04          | Sistema de agitación con rango de velocidad                                    | Explícita         | DOC-02, DOC-04 | Especificaciones | 100–1500 rpm vs 20–1500 rpm                                                                     | Alta      | No requerida             |
| E05          | Aireación con gases específicos controlables                                   | Explícita         | DOC-02, DOC-03 | Aeration         | O2/CO2 y Air/O2/N2/CO2                                                                          | Media     | Requiere mapeo de gases  |
| E06          | Materiales en contacto con cultivo deben documentarse                          | Explícita         | DOC-03         | Materiales       | Vidrio borosilicato, AISI 316L, EPDM                                                            | Alta      | Validar para desechables |
| E07          | Modos de proceso soportados son propiedad general                              | Explícita         | DOC-03         | Aplicaciones     | batch, fed-batch, continuous, perfusion                                                         | Media     | Confirmar para BioLector |
| E08          | Interfaz digital para adquisición de datos                                     | Explícita         | DOC-02, DOC-04 | Conectividad     | Ethernet; conexión a MFCS                                                                       | Alta      | No requerida             |

## 9. Conceptos ontológicos candidatos

| Concepto candidato      | Tipo sugerido       | Definición basada en evidencia                        | Fuente asociada | Estado    |
| ----------------------- | ------------------- | ----------------------------------------------------- | --------------- | --------- |
| Bioreactor              | Clase               | Sistema que alberga cultivo con control de parámetros | DOC-01, DOC-03  | Candidato |
| CultureVessel           | Clase               | Recipiente con volumen total y de trabajo definidos   | DOC-02, DOC-03  | Candidato |
| WorkingVolumeRange      | Propiedad de dato   | Intervalo operativo de volumen                        | E02             | Candidato |
| MaterialOfConstruction  | Propiedad de dato   | Materiales en contacto (vidrio, acero, polímero)      | E06             | Candidato |
| TemperatureControlRange | Propiedad de dato   | Límites de control térmico                            | E03             | Candidato |
| AgitationSystem         | Clase               | Mecanismo de mezcla (shaker o stirrer)                | E04             | Candidato |
| AgitationSpeedRange     | Propiedad de dato   | rpm mínimo y máximo                                   | E04             | Candidato |
| AerationSystem          | Clase               | Conjunto de líneas de gas y controladores             | E05             | Candidato |
| GasType                 | Individuo           | Air, O2, N2, CO2                                      | E05             | Candidato |
| Sensor                  | Clase               | Dispositivo de medida (pH, DO, temperatura, biomasa)  | E01             | Candidato |
| Actuator                | Clase               | Bomba, válvula, controlador de gas                    | DOC-04          | Candidato |
| ProcessMode             | Concepto auxiliar   | batch, fed-batch, continuous, perfusion               | E07             | Candidato |
| DataInterface           | Propiedad de objeto | Conexión Ethernet/SCADA                               | E08             | Candidato |

## 10. Relaciones ontológicas candidatas

| Relación candidata    | Dominio sugerido | Rango sugerido         | Significado                | Evidencia asociada | Estado    |
| --------------------- | ---------------- | ---------------------- | -------------------------- | ------------------ | --------- |
| hasVessel             | Bioreactor       | CultureVessel          | Asocia equipo con su vaso  | DOC-03             | Candidato |
| hasWorkingVolumeRange | CultureVessel    | WorkingVolumeRange     | Define capacidad operativa | E02                | Candidato |
| hasMaterial           | CultureVessel    | MaterialOfConstruction | Material en contacto       | E06                | Candidato |
| measuresParameter     | Sensor           | Parameter              | Capacidad de medida        | E01                | Candidato |
| controlsParameter     | Bioreactor       | Parameter              | Capacidad de control       | E03, E04           | Candidato |
| hasAgitationSystem    | Bioreactor       | AgitationSystem        | Sistema de mezcla          | E04                | Candidato |
| hasAerationSystem     | Bioreactor       | AerationSystem         | Sistema de gases           | E05                | Candidato |
| supportsProcessMode   | Bioreactor       | ProcessMode            | Modos operativos           | E07                | Candidato |

## 11. Triadas RDF candidatas

- Bioreactor -> hasWorkingVolumeRange -> WorkingVolumeRange — Soporte: DOC-02 800–2400 µL; DOC-03 0.6–5 L — Estado: soportada
- Bioreactor -> measuresParameter -> DissolvedOxygen — Soporte: DOC-01 "DO" — Estado: soportada
- Bioreactor -> controlsParameter -> Temperature — Soporte: DOC-02 hasta 50°C; DOC-04 0–80°C — Estado: soportada
- CultureVessel -> hasMaterial -> "BorosilicateGlass" — Soporte: DOC-03 materiales — Estado: soportada
- Bioreactor -> hasDataInterface -> Ethernet — Soporte: DOC-02 — Estado: requiere validación experta para Sartorius

## 12. Sinónimos y variantes terminológicas

| Término principal | Sinónimos o variantes documentadas    | Idioma | Documento de soporte |
| ----------------- | ------------------------------------- | ------ | -------------------- |
| Dissolved Oxygen  | DO, oxígeno disuelto                  | EN/ES  | DOC-01, DOC-04       |
| Working volume    | volumen de trabajo, volumen operativo | EN/ES  | DOC-02, DOC-03       |
| Agitation speed   | shaking frequency, stirrer speed, rpm | EN     | DOC-02, DOC-04       |
| pH control        | control de pH por ácido/base          | EN/ES  | DOC-02, DOC-03       |

## 13. Vacíos, riesgos y decisiones pendientes

- Falta manual de operación completo de BioLector XT para confirmar alarmas y fallas
- No se encontró especificación de presión máxima para Sartorius 10 L en los folletos
- Equivalencia funcional de kLa entre escalas solo parcialmente documentada
- Material exacto de placas desechables BioLector no declarado en corpus
- Necesidad de validar si "DataInterface" debe ser clase o propiedad

## 14. Registro metodológico para el documento de investigación

Se analizó la pregunta ALC-06 mediante búsqueda dirigida en documentación oficial de Beckman Coulter y Sartorius entre 2021-2022. Se recuperaron cuatro documentos verificables que describen tanto el microbioreactor BioLector XT como los sistemas Biostat B/B-DCU con vasos de 5 L y 10 L. La evaluación priorizó tablas de especificaciones y descripciones de sensores. La evidencia extraída permitió identificar propiedades comunes independientes de escala: volumen de trabajo, materiales, rangos de temperatura y agitación, capacidades de medida/control de pH y DO, sistemas de aireación, modos de proceso e interfaces digitales. A partir de ello se propusieron clases y propiedades candidatas en inglés para la ontología preliminar. Las limitaciones incluyen ausencia de manuales completos y de datos de validación de esterilidad, por lo que se requiere validación experta antes de formalizar axiomas.

## 15. Estado final

- **Nivel de confianza general:** Medio
- **Estado de la respuesta:** Parcialmente soportada
- **Estado del corpus:** Parcial
- **Próxima acción recomendada:** Obtener manuales de usuario completos de BioLector XT y BIOSTAT B-DCU Operating Instructions, y extraer secciones sobre alarmas, fallas y validación de materiales para completar las propiedades generales.
