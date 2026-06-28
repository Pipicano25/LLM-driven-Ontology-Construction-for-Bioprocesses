## 1) ID y pregunta

- **ID:** ALC-04
- **Pregunta:** ¿Qué componentes comunes permiten describir estos tres biorreactores en una misma ontología?

## 2) Respuesta basada en evidencia

La evidencia explícita muestra que el BioLector XT registra o emplea parámetros asociados con `ShakingSpeed`, `DissolvedOxygen` y `pH`, mediante velocidad de agitación y optodos de oxígeno y pH. El Biostat B documenta control de `Temperature`, `pH`, `DissolvedOxygen` y `StirrerSpeed`, además de dos bombas integradas para control de pH.

Como inferencia razonable, ambos tipos de sistema pueden describirse mediante categorías funcionales comunes relacionadas con parámetros de proceso: `pH`, `DissolvedOxygen` y velocidad de mezcla o agitación. También puede proponerse una categoría candidata de sistema de control de proceso, aunque el fragmento del BioLector XT no declara explícitamente una función de control para todas esas variables.

No está establecido en el corpus suministrado que los tres equipos tengan sensores físicamente equivalentes, recipientes equivalentes, sistemas de aireación equivalentes, control de temperatura equivalente o bombas de adición equivalentes.

## 3) Tabla de afirmaciones y evidencia

| ID evidencia | Afirmación                                                                            | Texto o fragmento de evidencia                                                 | Fuente y ubicación                                                                | Concepto / relación / triada candidata                                                               | Tipo de evidencia                                                    | Confianza | Validación experta |
| ------------ | ------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------ | --------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------- | --------- | ------------------ | 
| E-ALC04-01   | BioLector XT incluye una especificación de velocidad de agitación.                    | “SHAKING SPEED 100 – 1500 rpm (3 mm diameter)”                                 | SRC-001, “Cultivation conditions”                                                 | `ShakingSpeed`; `BioLectorXT -> hasProcessParameter -> ShakingSpeed`                                 | Explícita                                                            | Alta      | No                 |
| E-ALC04-02   | BioLector XT incluye optodos de oxígeno para oxígeno disuelto.                        | “OXYGEN OPTODES 0 – 100 % dissolved oxygen”                                    | SRC-001, “Cultivation conditions”                                                 | `OxygenOptode`; `DissolvedOxygen`; `OxygenOptode -> observesParameter -> DissolvedOxygen`            | Explícita                                                            | Alta      | No                 |
| E-ALC04-03   | BioLector XT incluye optodos de pH.                                                   | “pH OPTODES pH 4 – 7.5 (depending on plate)”                                   | SRC-001, “Cultivation conditions”                                                 | `pHOptode`; `pH`; `pHOptode -> observesParameter -> pH`                                              | Explícita                                                            | Alta      | No                 |
| E-ALC04-04   | Biostat B documenta configuraciones de volumen de 5 L y 10 L.                         | “Volume: 1 L, 2 L, 5 L or 10 L”                                                | SRC-002, p. 22, “Basic Configurations for Univessel® Glass”, “Microbial Packages” | `VolumeSpecification`; `BiostatB -> hasVolumeSpecification -> FiveLiterVolume`                       | Explícita                                                            | Alta      | No                 |
| E-ALC04-05   | Biostat B controla temperatura, pH, DO y velocidad del agitador.                      | “Control temperature, pH, DO, stirrer speed”                                   | SRC-002, p. 22, “Basic Configurations for Univessel® Glass”, “Microbial Packages” | `ProcessControlSystem`; `regulatesParameter`; `Temperature`; `pH`; `DissolvedOxygen`; `StirrerSpeed` | Explícita                                                            | Alta      | No                 |
| E-ALC04-06   | Biostat B tiene dos bombas integradas para control de pH.                             | “2 integrated pumps for pH control (acidbase)”                                                                            | SRC-002, p. 22, “Basic Configurations for Univessel® Glass”, “Microbial Packages”                    | `Pump`; `pHControlPump`; `BiostatB -> hasComponent -> pHControlPump` | Explícita | Alta               | No  |
| E-ALC04-07   | Los sistemas comparten parámetros funcionales relacionados con pH y oxígeno disuelto. | SRC-001 documenta pH y oxígeno disuelto; SRC-002 documenta control de pH y DO. | SRC-001, “Cultivation conditions”; SRC-002, p. 22                                 | `ProcessParameter`; `pH`; `DissolvedOxygen`                                                          | Inferida                                                             | Media     | Sí                 |
| E-ALC04-08   | Los sistemas comparten una función asociada a velocidad de mezcla o agitación.        | SRC-001 documenta “SHAKING SPEED”; SRC-002 documenta “stirrer speed”.          | SRC-001, “Cultivation conditions”; SRC-002, p. 22                                 | `MixingSpeed`; `MixingSubsystem`                                                                     | Inferida                                                             | Media     | Sí                 |

## 4) Conceptos candidatos

| Concepto candidato     | Tipo sugerido                            | Evidencia asociada                                                                | Tipo de evidencia | Confianza | Validación experta |
| ---------------------- | ---------------------------------------- | --------------------------------------------------------------------------------- | ----------------- | --------- | ------------------ |
| `BioLectorXT`          | Individuo                                | Título de SRC-001.                                                                | Explícita         | Alta      | No                 |
| `BiostatB`             | Individuo                                | Título de SRC-002.                                                                | Explícita         | Alta      | No                 |
| `ShakingSpeed`         | Propiedad de dato / parámetro de proceso | “SHAKING SPEED 100 – 1500 rpm”.                                                   | Explícita         | Alta      | No                 |
| `StirrerSpeed`         | Propiedad de dato / parámetro de proceso | “Control ... stirrer speed”.                                                      | Explícita         | Alta      | No                 |
| `DissolvedOxygen`      | Concepto auxiliar / parámetro de proceso | “dissolved oxygen”; “DO”.                                                         | Explícita         | Alta      | No                 |
| `pH`                   | Concepto auxiliar / parámetro de proceso | “pH OPTODES”; “Control ... pH”.                                                   | Explícita         | Alta      | No                 |
| `Temperature`          | Concepto auxiliar / parámetro de proceso | “Control temperature”.                                                            | Explícita         | Alta      | No                 |
| `OxygenOptode`         | Clase                                    | “OXYGEN OPTODES”.                                                                 | Explícita         | Alta      | No                 |
| `pHOptode`             | Clase                                    | “pH OPTODES”.                                                                     | Explícita         | Alta      | No                 |
| `Pump`                 | Clase                                    | “2 integrated pumps”.                                                             | Explícita         | Alta      | No                 |
| `pHControlPump`        | Subclase / concepto auxiliar             | “pumps for pH control”.                                                           | Explícita         | Alta      | No                 |
| `VolumeSpecification`  | Concepto auxiliar                        | “Volume: ... 5 L or 10 L”.                                                        | Explícita         | Alta      | No                 |
| `ProcessControlSystem` | Clase                                    | Biostat B documenta control de temperatura, pH, DO y velocidad del agitador.      | Inferida          | Media     | Sí                 |
| `MixingSubsystem`      | Clase                                    | Velocidad de agitación y velocidad de agitador documentadas en fuentes distintas. | Inferida          | Media     | Sí                 |
| `ProcessParameter`     | Clase                                    | pH, DO, temperatura y velocidades documentados como variables técnicas.           | Inferida          | Media     | Sí                 |

## 5) Relaciones candidatas con dominio y rango sugeridos

| Relación candidata       | Dominio sugerido       | Rango sugerido                  | Evidencia asociada                                                    | Tipo de evidencia | Confianza | Validación experta |
| ------------------------ | ---------------------- | ------------------------------- | --------------------------------------------------------------------- | ----------------- | --------- | ------------------ |
| `hasProcessParameter`    | `BioreactorSystem`     | `ProcessParameter`              | Velocidad de agitación, pH, DO, temperatura y velocidad del agitador. | Inferida          | Media     | Sí                 |
| `observesParameter`      | `OxygenOptode`         | `DissolvedOxygen`               | “OXYGEN OPTODES 0 – 100 % dissolved oxygen”.                          | Explícita         | Alta      | No                 |
| `observesParameter`      | `pHOptode`             | `pH`                            | “pH OPTODES pH 4 – 7.5”.                                              | Explícita         | Alta      | No                 |
| `regulatesParameter`     | `ProcessControlSystem` | `ProcessParameter`              | “Control temperature, pH, DO, stirrer speed”.                         | Explícita         | Alta      | No                 |
| `hasComponent`           | `BioreactorSystem`     | `Pump`                          | “2 integrated pumps for pH control”.                                  | Explícita         | Alta      | No                 |
| `hasVolumeSpecification` | `BioreactorSystem`     | `VolumeSpecification`           | “Volume: ... 5 L or 10 L”.                                            | Explícita         | Alta      | No                 |
| `hasMixingSpeed`         | `BioreactorSystem`     | `ShakingSpeed` o `StirrerSpeed` | “SHAKING SPEED”; “stirrer speed”.                                     | Inferida          | Media     | Sí                 |

## 6) Triadas RDF candidatas

| Triada RDF candidata                                    | Evidencia                                                                | Fuente y ubicación                | Tipo de evidencia | Confianza | Validación experta |
| ------------------------------------------------------- | ------------------------------------------------------------------------ | --------------------------------- | ----------------- | --------- | ------------------ |
| `BioLectorXT -> hasProcessParameter -> ShakingSpeed`    | “SHAKING SPEED 100 – 1500 rpm”                                           | SRC-001, “Cultivation conditions” | Explícita         | Alta      | No                 |
| `OxygenOptode -> observesParameter -> DissolvedOxygen`  | “OXYGEN OPTODES 0 – 100 % dissolved oxygen”                              | SRC-001, “Cultivation conditions” | Explícita         | Alta      | No                 |
| `pHOptode -> observesParameter -> pH`                   | “pH OPTODES pH 4 – 7.5”                                                  | SRC-001, “Cultivation conditions” | Explícita         | Alta      | No                 |
| `BiostatB -> hasVolumeSpecification -> FiveLiterVolume` | “Volume: 1 L, 2 L, 5 L or 10 L”                                          | SRC-002, p. 22                    | Explícita         | Alta      | No                 |
| `BiostatB -> hasVolumeSpecification -> TenLiterVolume`  | “Volume: 1 L, 2 L, 5 L or 10 L”                                          | SRC-002, p. 22                    | Explícita         | Alta      | No                 |
| `BiostatB -> regulatesParameter -> Temperature`         | “Control temperature”                                                    | SRC-002, p. 22                    | Explícita         | Alta      | No                 |
| `BiostatB -> regulatesParameter -> pH`                  | “Control ... pH”                                                         | SRC-002, p. 22                    | Explícita         | Alta      | No                 |
| `BiostatB -> regulatesParameter -> DissolvedOxygen`     | “Control ... DO”                                                         | SRC-002, p. 22                    | Explícita         | Alta      | No                 |
| `BiostatB -> regulatesParameter -> StirrerSpeed`        | “Control ... stirrer speed”                                              | SRC-002, p. 22                    | Explícita         | Alta      | No                 |
| `BiostatB -> hasComponent -> pHControlPump`             | “2 integrated pumps for pH control”                                      | SRC-002, p. 22                    | Explícita         | Alta      | No                 |
| `BioLectorXT -> hasProcessParameter -> DissolvedOxygen` | La fuente documenta optodos de oxígeno y porcentaje de oxígeno disuelto. | SRC-001, “Cultivation conditions” | Inferida          | Media     | Sí                 |
| `BioLectorXT -> hasProcessParameter -> pH`              | La fuente documenta optodos y rango de pH.                               | SRC-001, “Cultivation conditions” | Inferida          | Media     | Sí                 |
| `BioLectorXT -> hasMixingSpeed -> ShakingSpeed`         | La fuente documenta velocidad de agitación.                              | SRC-001, “Cultivation conditions” | Inferida          | Media     | Sí                 |

## 7) Sinónimos documentados

| Término principal     | Sinónimos o variantes documentadas | Fuente           |
| --------------------- | ---------------------------------- | ---------------- |
| `DissolvedOxygen`     | “dissolved oxygen”; “DO”           | SRC-001; SRC-002 |
| `ShakingSpeed`        | “SHAKING SPEED”                    | SRC-001          |
| `StirrerSpeed`        | “stirrer speed”                    | SRC-002          |
| `pHControlPump`       | “integrated pumps for pH control”  | SRC-002          |
| `VolumeSpecification` | “Volume”                           | SRC-002          |

## 8) Vacíos del corpus

- No establecido en el corpus suministrado cuál es el modelo específico de los sistemas Sartorius de 5 L y 10 L del laboratorio.
- No establecido en el corpus suministrado que cada volumen corresponda a un biorreactor individual distinto.
- No establecido en el corpus suministrado el tipo de recipiente de cultivo del BioLector XT.
- No establecido en el corpus suministrado la existencia de sensores de temperatura, pH o DO en Biostat B; solo se establece el control de estas variables.
- No establecido en el corpus suministrado que el BioLector XT controle pH, oxígeno disuelto o velocidad de agitación.
- No establecido en el corpus suministrado que Biostat B utilice optodos.
- No establecido en el corpus suministrado el método de aireación, gasificación o transferencia de masa.
- No establecido en el corpus suministrado la arquitectura de datos, alarmas, fallas, eventos, muestras, calibraciones o calidad de datos.
- No establecido en el corpus suministrado que `ShakingSpeed` y `StirrerSpeed` sean físicamente equivalentes.
- No establecido en el corpus suministrado que `OxygenOptode` y cualquier posible sensor Biostat B sean equivalentes.

## 9) Estado final

**Parcialmente soportado.**

El corpus sustenta explícitamente parámetros y componentes técnicos del BioLector XT y del Biostat B. La identificación de componentes funcionales comunes entre los tres sistemas requiere inferencias limitadas y validación experta, especialmente para la equivalencia entre configuraciones Sartorius de 5 L y 10 L y el BioLector XT.
