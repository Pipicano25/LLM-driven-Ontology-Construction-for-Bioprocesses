# 1) ID y pregunta

**ID:** ALC-08
**Pregunta:** ¿Qué conceptos deben quedar fuera del alcance inicial para evitar que la ontología sea demasiado amplia?

# 2) Respuesta basada en evidencia

El corpus suministrado (SRC-001 a SRC-009) no contiene ninguna declaración explícita sobre qué conceptos deben excluirse del alcance de una ontología. Ningún fragmento menciona "scope", "alcance ontológico", "exclusión" ni nada equivalente referido a un modelo conceptual.

Sin embargo, los fragmentos sí delimitan, de forma explícita, **qué cubre funcionalmente cada sistema** (variables medidas/controladas, módulos, recipientes, rangos de operación). A partir de esa delimitación funcional explícita puede inferirse razonablemente qué tipos de conceptos quedarían fuera de un modelo centrado en estos tres sistemas, pero esto es **inferencia**, no evidencia explícita del corpus, y no debe tomarse como respuesta definitiva.

**No establecido en el corpus suministrado:** cualquier afirmación directa sobre exclusiones de alcance ontológico.

# 3) Tabla de afirmaciones y evidencia

| ID    | Texto/fragmento de evidencia                                                                                                                                                                                                                                                                                   | Fuente / sección                                 | Concepto/relación/triada candidata                                                                                                 | Tipo de evidencia | Confianza | Validación experta                                 |
| ----- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------ | ---------------------------------------------------------------------------------------------------------------------------------- | ----------------- | --------- | -------------------------------------------------- |
| AF-01 | "Cultivation conditions, system dimensions, Gassing lid dimensions, Microfluidic features and more for the Bioreactor XT microbioreactor"                                                                                                                                                                      | SRC-001, sección general                         | BioLectorXT -> hasScopeOfMeasurement -> CultivationConditions                                                                      | Explícita         | Media     | Sí                                                 |
| AF-02 | "the BioLector XT microbioreactor is based on a standard ANSI/SLAS (SBS) microtiter plate (MTP) format, and operates with online, pre-calibrated optical sensors... supports simultaneous pH control and feeding"                                                                                              | SRC-002, descripción general                     | BioLectorXT -> controlsVariable -> pH                                                                                              | Explícita         | Alta      | No                                                 |
| AF-03 | "The BioLector XT microbioreactor measures biomass, pH, DO, and fluorescence online... The system controls the shaking speed and the temperature"                                                                                                                                                              | SRC-003, descripción del sistema                 | BioLectorXT -> measuresVariable -> {Biomass, pH, DO, Fluorescence}; BioLectorXT -> controlsVariable -> {ShakingSpeed, Temperature} | Explícita         | Alta      | No                                                 |
| AF-04 | "online-monitoring of common cultivation parameters such as biomass, pH, dissolved oxygen (DO) and fluorescence of various fluorescing molecules or proteins"                                                                                                                                                  | SRC-004, descripción general                     | BioLectorXT -> hasMonitoredParameter -> {Biomass, pH, DO, Fluorescence}                                                            | Explícita         | Alta      | No                                                 |
| AF-05 | "These operating instructions apply to the BIOSTAT® B-MO (microbial), BIOSTAT® B-CC (cell culture)... in combination with the following culture vessels (operating volume): 1L, 2L, 5L, 10L [...] UniVessel® SU: 2L"                                                                                           | SRC-005, sección 1.1 "Validity"                  | BiostatB -> hasValidVesselVolume -> {1L, 2L, 5L, 10L}                                                                              | Explícita         | Alta      | No                                                 |
| AF-06 | "Biostat® B-DCU The Industry Standard Bioreactor for Advanced Process Optimization and Characterization"                                                                                                                                                                                                       | SRC-006, introducción                            | BiostatBDCU -> usedFor -> ProcessOptimizationAndCharacterization                                                                   | Explícita         | Media     | Sí                                                 |
| AF-07 | "the advanced DO controller supports parallel adjustment of all DO affecting parameter settings like stirrer speed and gas flow rates of air and pure oxygen, automatically and simultaneously to control the DO set point"                                                                                    | SRC-007, sección de control de gases y DO        | BiostatB -> controlsVariable -> DO; BiostatB -> hasControlStrategy -> AdvancedDOController                                         | Explícita         | Alta      | No                                                 |
| AF-08 | "Gas supply comprises the following gases (depending on the integrated aeration module): ... AIR (air), Oxygen (O..."                                                                                                                                                                                          | SRC-008, sección 6.4.4 "Gas Supply"              | BiostatB -> usesGas -> {Air, Oxygen, ...}                                                                                          | Explícita         | Media     | Sí (fragmento truncado, lista de gases incompleta) |
| AF-09 | "Working volume: 2L (0.4-2L); 5L (0.6-5L); 10L (1.5-10L) - Permitted stirring speed... - Sensors: pH, pO2, Temperature, Foam, Level, Substrate"                                                                                                                                                                | SRC-009, "Technical features and specifications" | BiostatB10L -> hasSensor -> {pH, pO2, Temperature, Foam, Level, Substrate}                                                         | Explícita         | Alta      | No                                                 |
| AF-10 | Inferencia: dado que ningún fragmento del corpus menciona variables de biología molecular/genómica, regulación GMP, aspectos comerciales, ni escalas de recipiente distintas a las explícitamente listadas (1L, 2L, 5L, 10L), estos no estarían cubiertos por el alcance funcional documentado de los sistemas | SRC-001 a SRC-009 (ausencia conjunta)            | (sin triada formal; es nota de alcance, no relación afirmativa)                                                                    | Inferida          | Baja      | Sí                                                 |

# 4) Conceptos candidatos

| Concepto candidato                                    | Tipo sugerido              | Fuente asociada                    | Estado    |
| ----------------------------------------------------- | -------------------------- | ---------------------------------- | --------- |
| CultivationCondition                                  | Clase                      | SRC-001                            | Candidato |
| MicrotiterPlate (MTP)                                 | Clase                      | SRC-002                            | Candidato |
| Biomass                                               | Clase / variable           | SRC-002, SRC-003, SRC-004          | Candidato |
| pH                                                    | Clase / variable           | SRC-002, SRC-003, SRC-004, SRC-007 | Candidato |
| DissolvedOxygen (DO)                                  | Clase / variable           | SRC-003, SRC-004, SRC-007          | Candidato |
| Fluorescence                                          | Clase / variable           | SRC-003, SRC-004                   | Candidato |
| ShakingSpeed                                          | Propiedad de dato          | SRC-003                            | Candidato |
| Temperature                                           | Clase / variable           | SRC-003, SRC-009                   | Candidato |
| CultureVessel                                         | Clase                      | SRC-005                            | Candidato |
| OperatingVolume                                       | Propiedad de dato          | SRC-005, SRC-009                   | Candidato |
| AdvancedDOController                                  | Individuo / Clase auxiliar | SRC-007                            | Candidato |
| AerationModule                                        | Clase                      | SRC-008                            | Candidato |
| Sensor (pH, pO2, Temperature, Foam, Level, Substrate) | Subclase / individuo       | SRC-009                            | Candidato |
| StirringSpeed                                         | Propiedad de dato          | SRC-009                            | Candidato |

No establecido en el corpus suministrado: ningún concepto explícito de exclusión de alcance (p. ej. "biología molecular", "regulación GMP") aparece mencionado textualmente en las fuentes; estos solo podrían proponerse por ausencia, no por afirmación.

# 5) Relaciones candidatas con dominio y rango sugeridos

| Relación candidata   | Dominio sugerido | Rango sugerido  | Evidencia                 | Estado    |
| -------------------- | ---------------- | --------------- | ------------------------- | --------- |
| measuresVariable     | BioreactorSystem | ProcessVariable | SRC-003, SRC-004          | Candidato |
| controlsVariable     | BioreactorSystem | ProcessVariable | SRC-002, SRC-003, SRC-007 | Candidato |
| hasValidVesselVolume | BioreactorSystem | OperatingVolume | SRC-005, SRC-009          | Candidato |
| hasSensor            | BioreactorSystem | Sensor          | SRC-009                   | Candidato |
| usesGas              | BioreactorSystem | Gas             | SRC-008                   | Candidato |
| hasControlStrategy   | BioreactorSystem | ControlStrategy | SRC-007                   | Candidato |
| usedFor              | BioreactorSystem | ProcessPurpose  | SRC-006                   | Candidato |

# 6) Triadas RDF candidatas

```
BioLectorXT -> measuresVariable -> Biomass
```

Soporte: SRC-003 / SRC-004. Estado: soportada.

```
BioLectorXT -> measuresVariable -> pH
```

Soporte: SRC-002 / SRC-003 / SRC-004. Estado: soportada.

```
BioLectorXT -> measuresVariable -> DissolvedOxygen
```

Soporte: SRC-003 / SRC-004. Estado: soportada.

```
BioLectorXT -> measuresVariable -> Fluorescence
```

Soporte: SRC-003 / SRC-004. Estado: soportada.

```
BioLectorXT -> controlsVariable -> ShakingSpeed
```

Soporte: SRC-003. Estado: soportada.

```
BioLectorXT -> controlsVariable -> Temperature
```

Soporte: SRC-003. Estado: soportada.

```
BiostatB -> hasValidVesselVolume -> "1L, 2L, 5L, 10L"
```

Soporte: SRC-005, sección 1.1 "Validity". Estado: soportada.

```
BiostatB -> controlsVariable -> DissolvedOxygen
```

Soporte: SRC-007. Estado: soportada.

```
BiostatB10L -> hasSensor -> "pH, pO2, Temperature, Foam, Level, Substrate"
```

Soporte: SRC-009. Estado: soportada.

```
BiostatB -> usesGas -> "Air, Oxygen"
```

Soporte: SRC-008 (fragmento truncado: lista de gases incompleta en el texto disponible). Estado: parcialmente soportada — requiere validación experta para completar la lista de gases.

No se generan triadas sobre "exclusión de alcance" porque ningún fragmento del corpus lo afirma; cualquier triada de ese tipo sería inferencia sin soporte textual directo y se omite por instrucción de no convertir inferencias en axiomas.

# 7) Sinónimos documentados

No establecido en el corpus suministrado. Ninguno de los fragmentos entregados contiene variantes terminológicas explícitas (sinónimos en español/inglés) para los conceptos identificados; solo se dispone del término en inglés tal como aparece en las fuentes originales (p. ej. "DO" como abreviatura de "dissolved oxygen" en SRC-003/SRC-004/SRC-007).

# 8) Vacíos del corpus

- No hay en el corpus ningún fragmento que aborde directamente la pregunta de alcance ontológico (qué excluir).
- El fragmento SRC-008 está truncado ("Oxygen (O...") y no permite confirmar la lista completa de gases soportados por BIOSTAT B.
- No hay fechas verificables de publicación/vigencia para SRC-001, SRC-002, SRC-003, SRC-004, SRC-006, SRC-007 y SRC-009.
- No hay fragmentos sobre fases de proceso, eventos, alarmas, fallas, decisiones, observaciones, muestras o calidad de datos — dimensiones mencionadas en el alcance general del proyecto pero no cubiertas por las fuentes de este paquete.
- No hay evidencia comparativa entre BioLector XT y BIOSTAT B sobre equivalencia funcional entre escalas.

# 9) Estado final

**Parcialmente soportado.** El corpus permite responder con evidencia explícita qué variables y módulos cubren funcionalmente BioLector XT y BIOSTAT B (5L/10L), lo cual ofrece una base indirecta para razonar sobre el alcance. Pero la pregunta específica sobre qué excluir **no está establecida en el corpus suministrado**: no hay ninguna fuente que declare exclusiones de alcance ontológico de forma explícita. Cualquier conclusión sobre exclusiones requiere inferencia adicional fuera de este corpus y validación experta antes de incorporarse a la ontología.
