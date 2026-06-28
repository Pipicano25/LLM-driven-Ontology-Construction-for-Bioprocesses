## 1. Identificación de la pregunta

- **ID:** ALC-02
- **Nivel metodológico:** Conceptual-ontológico / delimitación de clase
- **Tema:** Definición mínima de biorreactor en el contexto BioLector XT, Sartorius 5 L y Sartorius 10 L
- **Pregunta:** ¿Qué características mínimas debe tener un sistema para ser considerado biorreactor y no solo un recipiente de cultivo?

## 2. Propósito de la pregunta

La pregunta busca establecer el límite ontológico entre **Bioreactor** y **CultureVessel**. No es trivial porque tanto el BioLector XT (microescala) como los Sartorius 5 L/10 L (banco) se describen como "vessels", pero la literatura y los manuales les atribuyen funciones de control que un matraz o placa no tiene.

Para la ontología OWL/RDF necesitamos:

- criterios verificables para instanciar `Bioreactor` vs `SimpleCultureContainer`
- propiedades de dato y de objeto que capturen "control", "monitorización" y "entorno regulado"
- base para equivalencias funcionales entre escalas

## 3. Plan de búsqueda documental

**Información técnica requerida:**

- definiciones normativas de biorreactor
- funciones esenciales y requisitos de diseño
- componentes mínimos (sensores, controladores, actuadores)
- distinción explícita frente a recipientes pasivos

**Tipos de documentos:**

- glosarios normativos (IUPAC)
- revisiones académicas 2021-2026
- manuales técnicos oficiales de Beckman Coulter (BioLector XT) y Sartorius (Biostat B-DCU)
- artículos peer-reviewed sobre sistemas de cultivo escalables

**Fuentes consultadas:**

- IUPAC Gold Book, ScienceDirect Topics, Eppendorf Academy, Beckman Coulter, ManualsLib (Sartorius), PMC/Frontiers

**Términos de búsqueda (es/en):**

- "bioreactor definition controlled environment"
- "bioreactor vs culture vessel monitoring control"
- "BioLector XT technical data sheet"
- "Sartorius Biostat B-DCU operating instructions"
- "bioreactor essential functions pH DO temperature control"

**Criterios de inclusión:** documentos con autoría, fecha o versión trazable, que describan funciones mínimas.
**Criterios de exclusión:** blogs sin referencia, material comercial sin especificaciones.

## 4. Documentos candidatos encontrados

| ID documento | Título                                                                   | Entidad autora                                                | Año                         | Tipo de fuente         | URL/DOI verificable                                                         | Relación con la pregunta                                                                       | Decisión preliminar |
| ------------ | ------------------------------------------------------------------------ | ------------------------------------------------------------- | --------------------------- | ---------------------- | --------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------- | ------------------- |
| DOC-01       | bioreactor (B00662)                                                      | IUPAC                                                         | 1992 (versión online 2025)  | Glosario normativo     | https://doi.org/10.1351/goldbook.B00662                                     | Definición base                                                                                | Include             |
| DOC-02       | Bioreactor – overview                                                    | ScienceDirect Topics (Delavar & Wang 2022; Wang & Zhong 2007) | 2022                        | Revisión terciaria     | https://www.sciencedirect.com/topics/immunology-and-microbiology/bioreactor | Funciones esenciales y requisitos                                                              | Include             |
| DOC-03       | What is a Bioreactor?                                                    | Eppendorf SE                                                  | s.f. (contenido vigente)    | Fabricante – educativo | https://www.eppendorf.com/ch-fr/lab-academy/.../what-is-a-bioreactor/       | Distingue biorreactor de shaker/incubadora, lista componentes                                  | Include             |
| DOC-04       | BioLector XT Microbioreactor – Technical Data Sheet                      | Beckman Coulter / m2p-labs                                    | s.f.                        | Ficha técnica oficial  | https://www.beckman.es/.../biolector-xt-technical-data-sheet                | Evidencia de monitorización y control en microescala                                           | Include             |
| DOC-05       | BIOSTAT B-DCU Operating Instructions Manual                              | Sartorius Stedim Biotech                                      | s.f. (versión 85037-549-98) | Manual oficial         | https://www.manualslib.com/manual/3061881/...                               | Uso previsto: cultivo bajo condiciones controladas y reproducibles                             | Include             |
| DOC-06       | Scalable Production... in a Microcarrier-Based Bioreactor Culture System | de Almeida Fuzeta et al., Frontiers                           | 2020                        | Artículo peer-reviewed | https://doi.org/10.3389/fcell.2020.553444                                   | Afirma que biorreactores permiten monitorización y control, a diferencia de sistemas estáticos | Include             |

## 5. Evaluación de documentos candidatos

| ID documento | Relevancia | Autoridad | Trazabilidad                                      | Cobertura de la pregunta       | Evidencia localizable                    | Justificación                            |
| ------------ | ---------- | --------- | ------------------------------------------------- | ------------------------------ | ---------------------------------------- | ---------------------------------------- |
| DOC-01       | Media      | Alta      | Alta                                              | Baja                           | Definición breve                         | Base normativa pero no detalla mínimos   |
| DOC-02       | Alta       | Alta      | Alta                                              | Alta                           | Funciones, requisitos de control         | Describe entorno controlado y parámetros |
| DOC-03       | Alta       | Media     | Media                                             | Alta                           | Componentes, comparación con recipientes | Útil para distinción práctica            |
| DOC-04       | Alta       | Alta      | Alta                                              | Media                          | Optodos, control pH en lazo cerrado      | Evidencia técnica microescala            |
| DOC-05       | Alta       | Alta      | Alta                                              | Media                          | Uso previsto y arquitectura de control   | Evidencia técnica banco                  |
| DOC-06       | Alta       | Alta      | Afirmación explícita sobre monitorización/control | Puente entre teoría y práctica |

## 6. Corpus documental seleccionado

| ID documento | Documento seleccionado  | Pregunta asociada | Fragmentos o páginas relevantes                  | Estado   |
| ------------ | ----------------------- | ----------------- | ------------------------------------------------ | -------- |
| DOC-01       | IUPAC Gold Book         | ALC-02            | definición                                       | Incluido |
| DOC-02       | ScienceDirect Topics    | ALC-02            | secciones 7.1.1, 7.1.2, Introducción             | Incluido |
| DOC-03       | Eppendorf               | ALC-02            | definición, componentes                          | Incluido |
| DOC-04       | BioLector XT datasheet  | ALC-02            | OXYGEN OPTODES, pH OPTODES, TRIGGERED pH CONTROL | Incluido |
| DOC-05       | Sartorius BIOSTAT B-DCU | ALC-02            | Intended Use, Device Description                 | Incluido |
| DOC-06       | Frontiers 2020          | ALC-02            | discusión sobre monitorización/control           | Incluido |

## 7. Respuesta basada en evidencia

La evidencia muestra que un biorreactor no se define solo por contener células, sino por **proporcionar y mantener activamente un entorno regulado**.

**Evidencia explícita:**

- IUPAC lo define como "aparato usado para llevar a cabo cualquier tipo de bioproceso", sin detallar control, lo que explica por qué históricamente el término es amplio.
- ScienceDirect precisa que es "un dispositivo, recipiente o sistema para cultivar... que proporciona un entorno controlado para crecimiento óptimo" y que su propósito principal es "proporcionar un entorno adecuado y regulado".
- El mismo texto exige que sea "fácil de monitorizar y/o controlar parámetros de reacción (como oxígeno disuelto, pH, temperatura, agitación, redox) para crear un entorno aséptico controlado" y que "es necesario controlar parámetros operativos... DO, pH, temperatura, mezcla y suplementación de nutrientes".
- Eppendorf refuerza: "vasos usados para cultivar células bajo condiciones estrechamente controladas", y lista como partes esenciales sensores, software de control y actuadores.
- Frente a un simple recipiente, Eppendorf señala que los biorreactores disminuyen variabilidad lote a lote, algo que shakers/incubadoras no logran.

**Evidencia en equipos del alcance:**

- BioLector XT incorpora optodos de oxígeno (0-100% DO) y pH (4-7.5), y control de pH disparado en lazo cerrado con controlador PI editable.
- Sartorius BIOSTAT B-DCU está destinado "a cultivar cultivos biológicos en líquidos bajo condiciones controladas y reproducibles", y su unidad de suministro forma la interfaz con el sistema de medición y control.
- El artículo de Frontiers afirma que las plataformas de cultivo requieren "escalabilidad así como la capacidad de monitorizar y controlar parámetros de cultivo, lo que no puede lograrse en sistemas estáticos tradicionales", y que "los biorreactores también permiten la implementación de sistemas de monitorización y control de cultivo".

**Inferencia razonable basada en evidencia:**
Un sistema mínimo debe integrar tres capas inseparables: (1) contención física, (2) sensado en tiempo real de al menos una variable crítica, y (3) capacidad de actuación regulada (lazo abierto o cerrado) para mantener setpoints. Sin estas, permanece como recipiente de cultivo.

**Información no establecida en el corpus:**

- No hay consenso normativo sobre número mínimo de parámetros (¿basta pH o se requiere también DO y temperatura?).
- IUPAC no exige control activo, lo que genera ambigüedad histórica.
- Los manuales no definen umbral entre "monitorización" y "control".

## 8. Tabla de afirmaciones y evidencia

| ID evidencia | Afirmación                                                                          | Tipo de evidencia | Documento                   | Página/sección        | Fragmento o resumen fiel                                                                 | Confianza | Validación experta  |
| ------------ | ----------------------------------------------------------------------------------- | ----------------- | --------------------------- | --------------------- | ---------------------------------------------------------------------------------------- | --------- | ------------------- |
| E1           | Biorreactor = aparato para bioproceso                                               | Explícita         | DOC-01                      | definición            | "An apparatus used to carry out any kind of bioprocess"                                  | Alta      | No requerida        |
| E2           | Proporciona entorno controlado para crecimiento óptimo                              | Explícita         | DOC-02                      | 7.1.1                 | "provide a controlled environment for optimal cell growth"                               | Alta      | No requerida        |
| E3           | Debe ser fácil de monitorizar/controlar DO, pH, temperatura, agitación              | Explícita         | DOC-02                      | 7.1.2                 | "Easy to monitor and/or control reaction parameters..."                                  | Alta      | No requerida        |
| E4           | Requiere control de DO, pH, temperatura, mezcla, nutrientes                         | Explícita         | DOC-02                      | Introducción          | "need to be controlled and optimized"                                                    | Alta      | No requerida        |
| E5           | Biorreactores usan condiciones estrechamente controladas                            | Explícita         | DOC-03                      | definición            | "under tightly controlled conditions"                                                    | Alta      | No requerida        |
| E6           | Componentes esenciales: sensores, software de control, actuadores                   | Explícita         | DOC-03                      | componentes           | lista de sensores, software, actuadores                                                  | Alta      | No requerida        |
| E7           | BioLector XT mide DO y pH con optodos                                               | Explícita         | DOC-04                      | specs                 | OXYGEN OPTODES 0-100%, pH OPTODES 4-7.5                                                  | Alta      | No requerida        |
| E8           | BioLector XT tiene control pH en lazo cerrado                                       | Explícita         | DOC-04                      | microfluidic features | TRIGGERED pH CONTROL (CLOSED LOOP)                                                       | Alta      | No requerida        |
| E9           | Sartorius cultiva bajo condiciones controladas y reproducibles                      | Explícita         | DOC-05                      | Intended Use          | "under controlled and reproducible conditions"                                           | Alta      | No requerida        |
| E10          | Biorreactores permiten monitorización y control, a diferencia de sistemas estáticos | Explícita         | DOC-06                      | discusión             | "ability to monitor and control... cannot be accomplished in traditional static culture" | Alta      | No requerida        |
| E11          | Mínimo = contención + sensado + actuación regulada                                  | Inferida          | Síntesis DOC-02/03/04/05/06 | —                     | Integración de requisitos                                                                | Media     | Requiere validación |

## 9. Conceptos ontológicos candidatos

| Concepto candidato    | Tipo sugerido     | Definición basada en evidencia                                                                   | Fuente asociada    | Estado    |
| --------------------- | ----------------- | ------------------------------------------------------------------------------------------------ | ------------------ | --------- |
| Bioreactor            | Clase             | Apparatus that carries out a bioprocess and provides a controlled environment for optimal growth | DOC-01, DOC-02     | candidato |
| CultureVessel         | Clase             | Physical container for cells without active monitoring/control                                   | DOC-03 (contraste) | candidato |
| ControlledEnvironment | Concepto auxiliar | Condition maintained by monitoring and regulating process parameters                             | DOC-02, DOC-05     | candidato |
| MonitoringSystem      | Clase             | System enabling measurement of pH, DO, temperature, etc.                                         | DOC-03, DOC-04     | candidato |
| ControlSystem         | Clase             | System that calculates adjustments to maintain setpoints                                         | DOC-03             | candidato |
| Sensor                | Clase             | Device for continuous real-time parameter measurement                                            | DOC-03, DOC-04     | candidato |
| Actuator              | Clase             | Pump, valve or motor regulated by control software                                               | DOC-03             | candidato |
| ProcessParameter      | Clase             | DO, pH, Temperature, AgitationRate, etc.                                                         | DOC-02             | candidato |

## 10. Relaciones ontológicas candidatas

| Relación candidata | Dominio sugerido | Rango sugerido        | Significado                   | Evidencia asociada | Estado    |
| ------------------ | ---------------- | --------------------- | ----------------------------- | ------------------ | --------- |
| provides           | Bioreactor       | ControlledEnvironment | suministra entorno regulado   | DOC-02, DOC-05     | candidato |
| monitors           | MonitoringSystem | ProcessParameter      | mide parámetro                | DOC-03, DOC-04     | candidato |
| controls           | ControlSystem    | ProcessParameter      | mantiene setpoint             | DOC-03, DOC-04     | candidato |
| hasComponent       | Bioreactor       | Sensor                | posee sensor                  | DOC-03             | candidato |
| hasComponent       | Bioreactor       | Actuator              | posee actuador                | DOC-03             | candidato |
| distinguishesFrom  | Bioreactor       | CultureVessel         | diferencia por control activo | DOC-03, DOC-06     | candidato |

## 11. Triadas RDF candidatas

- **Bioreactor -> provides -> ControlledEnvironment** — Soportada — DOC-02 sección 7.1.1; DOC-05 Intended Use — Estado: soportada
- **Bioreactor -> hasComponent -> Sensor** — Soportada — DOC-03 "Sensors monitor pH, dissolved oxygen and temperature" — Estado: soportada
- **Bioreactor -> hasComponent -> ControlSystem** — Soportada — DOC-03 "control software calculates adjustments" — Estado: soportada
- **Bioreactor -> hasComponent -> Actuator** — Soportada — DOC-03 "actuators can be pumps, valves, or motors" — Estado: soportada
- **Bioreactor -> monitors -> ProcessParameter** — Parcialmente soportada — DOC-02 lista parámetros — Estado: requiere validación experta para lista mínima
- **CultureVessel -> lacks -> ControlSystem** — Inferida — DOC-06 contraste con sistemas estáticos — Estado: requiere validación

## 12. Sinónimos y variantes terminológicas

| Término principal      | Sinónimos o variantes documentadas                     | Idioma | Documento de soporte |
| ---------------------- | ------------------------------------------------------ | ------ | -------------------- |
| Bioreactor             | fermenter, fermentor                                   | en     | DOC-01, DOC-03       |
| Controlled environment | regulated environment, tightly controlled conditions   | en     | DOC-02, DOC-03       |
| Monitoring and control | monitor and/or control, measurement and control system | en     | DOC-02, DOC-05       |
| Culture vessel         | flask, plate, shaker, incubator (uso comparativo)      | en     | DOC-03               |

## 13. Vacíos, riesgos y decisiones pendientes

- IUPAC no exige control, lo que choca con definiciones modernas; riesgo de incluir recipientes pasivos como biorreactores si se usa solo DOC-01.
- No se establece número mínimo de sensores: ¿un solo optodo de pH basta? BioLector XT sugiere al menos DO y pH, Sartorius incluye temperatura, pH, DO, agitación.
- Ambigüedad entre "monitorizar" y "controlar": DOC-02 dice "monitor and/or control", DOC-03 exige ambos (sensor + software + actuador).
- Falta manual completo de Sartorius 5 L/10 L con lista de sensores obligatorios; solo se dispone de extracto del B-DCU.
- Necesario validar con expertos si "lazo cerrado" es requisito mínimo o si "lazo abierto con ajuste manual" califica.

## 14. Registro metodológico para el documento de investigación

Se analizó la pregunta ALC-02 mediante búsqueda dirigida en glosarios normativos, revisiones académicas y documentación oficial de fabricantes. Se priorizaron fuentes 2021-2026, admitiendo manuales vigentes sin fecha explícita. El corpus final integró seis documentos verificables: IUPAC Gold Book, ScienceDirect Topics (2022), Eppendorf, ficha técnica BioLector XT, manual Sartorius B-DCU y artículo Frontiers 2020. La evidencia convergente indica que la característica distintiva no es el volumen ni el material, sino la capacidad de proporcionar un entorno controlado mediante sensado continuo y actuación regulada. A partir de ello se propusieron clases candidatas (Bioreactor, CultureVessel, MonitoringSystem, ControlSystem) y relaciones (provides, monitors, controls). Las limitaciones incluyen la ausencia de un umbral normativo mínimo y la necesidad de validación experta para decidir si el control en lazo cerrado es obligatorio.

## 15. Estado final

- **Nivel de confianza general:** Medio
- **Estado de la respuesta:** Parcialmente soportada (evidencia sólida para entorno controlado, pero falta consenso sobre mínimos cuantitativos)
- **Estado del corpus:** Parcial (cubre definición y funciones, pero carece de norma ISO específica y de manuales completos Sartorius 5 L/10 L)
- **Próxima acción recomendada:** Solicitar a Sartorius y Beckman Coulter los manuales completos con especificaciones de sensores obligatorios, y validar con expertos de bioprocesos si "monitorización + capacidad de actuación" es suficiente o se requiere control automático en lazo cerrado para la ontología.
