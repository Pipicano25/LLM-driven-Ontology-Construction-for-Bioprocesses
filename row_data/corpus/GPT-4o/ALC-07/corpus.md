## 1) ID y pregunta

**ID:** ALC-07
**Pregunta:** ¿Qué relaciones básicas debe tener cada biorreactor con sensores, actuadores, variables operativas, fases del proceso y eventos?

---

## 2) Respuesta basada en evidencia

El corpus suministrado respalda parcialmente que los sistemas de biorreactor deben poder relacionarse con:

- componentes de actuación, como `PeristalticPump`, `SolenoidValve` y `MassFlowController`;
- variables operativas tales como temperatura, pH, DO, espuma, nivel, turbidez, redox, biomasa, fluorescencia y presión;
- modos de proceso como `Batch`, `FedBatch`, `Continuous` y `Perfusion`;
- capacidades de alarma, incluyendo `PotentialFreeAlarmContact` y `RemoteAlarming`;
- estrategias de alimentación como `ContinuousFeeding` y `SignalTriggeredFeeding`;
- señales o programaciones, como `PredefinedSchedule` y `OnlineProcessSignal`.

Para BioLector XT, está explícitamente documentado el monitoreo en línea de biomasa, pH, DO y fluorescencia, así como modos de gasificación, agentes de alimentación y agentes de pH. También se documentan estrategias de alimentación continua y disparada por señal.

No está establecido en el corpus suministrado que los modos de proceso deban modelarse como fases biológicas. El corpus usa los términos `batch`, `fed-batch`, `continuous` y `perfusion`, por lo que `ProcessMode` está mejor soportado que `ProcessPhase`.

Tampoco está establecida una taxonomía completa de eventos, alarmas, severidades, errores, fallas, recuperación o bitácoras de ejecución.

---

## 3) Tabla de afirmaciones y evidencia

| ID    | Afirmación                                                                                                      | Texto o fragmento de evidencia                                                                           | Fuente y ubicación                                                                                                | Concepto / relación / triada candidata                                                              | Tipo                                                   | Confianza | Validación experta |
| ----- | --------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- | ------------------------------------------------------ | --------- | ------------------ |
| AF-01 | Se documentan componentes de actuación en un sistema Sartorius.                                                 | “Peristaltic pumps”; “solenoid valves”; “mass flow controllers”.                                         | SRC-001. Páginas 6–7, 10, 16 y secciones de alarmas; la correspondencia exacta por fragmento no fue suministrada. | `Actuator`; `hasActuationComponent`; `BioreactorSystem -> hasActuationComponent -> PeristalticPump` | explícita                                              | alta      | no                 |
| AF-02 | Se documentan variables asociadas a un sistema Sartorius.                                                       | “Temperature, pH, DO, foam, level, turbidity, redox”.                                                    | SRC-001. Ubicación general suministrada.                                                                          | `OperatingVariable`; `hasOperatingVariable`                                                         | explícita                                              | alta      | no                 |
| AF-03 | Se documentan modos de proceso.                                                                                 | “batch, fed-batch, continuous and perfusion”.                                                            | SRC-001. Ubicación general suministrada.                                                                          | `ProcessMode`; `supportsProcessMode`                                                                | explícita                                              | alta      | no                 |
| AF-04 | Se documentan capacidades relacionadas con alarmas.                                                             | “potential-free alarm contact”; “remote alarming”.                                                       | SRC-001. Secciones de alarmas.                                                                                    | `AlarmCapability`; `supportsAlarmCapability`                                                        | explícita                                              | alta      | sí                 |
| AF-05 | Univessel Glass se documenta con volúmenes de trabajo de 5 L y 10 L.                                            | “5 L and 10 L working volume”.                                                                           | SRC-002. Páginas 23–27 y 31–35.                                                                                   | `CultureVessel`; `hasWorkingVolume`                                                                 | explícita                                              | alta      | no                 |
| AF-06 | Se documentan variables para los sistemas Univessel Glass.                                                      | “pH, DO, biomass, temperature, level, foam and pressure”.                                                | SRC-002. Páginas 23–27 y 31–35.                                                                                   | `OperatingVariable`; `hasOperatingVariable`                                                         | explícita                                              | alta      | no                 |
| AF-07 | BioLector XT realiza monitoreo en línea de biomasa, pH, DO y fluorescencia.                                     | “online-monitoring of biomass, pH, DO and fluorescence”.                                                 | SRC-003. Páginas 1–3.                                                                                             | `OnlineMonitoring`; `monitorsVariable`                                                              | explícita                                              | alta      | no                 |
| AF-08 | BioLector XT dispone de varios modos de gasificación.                                                           | “five different gassing modes”.                                                                          | SRC-003. Páginas 1–3.                                                                                             | `GassingMode`; `supportsGassingMode`                                                                | explícita                                              | alta      | no                 |
| AF-09 | BioLector XT incluye agentes de alimentación y de pH.                                                           | “feed agents and pH agents”.                                                                             | SRC-003. Páginas 1–3.                                                                                             | `FeedAgent`; `PHAgent`; `usesProcessAgent`                                                          | explícita                                              | media     | sí                 |
| AF-10 | BioLector XT incluye programación y señales en línea.                                                           | “predefined schedule”; “online process signals”.                                                         | SRC-003. Páginas 1–3.                                                                                             | `PredefinedSchedule`; `OnlineProcessSignal`; `triggeredBy`                                          | explícita para los términos; inferida para la relación | media     | sí                 |
| AF-11 | BioLector XT soporta cultivo batch y fed-batch, con estrategias de alimentación continua y disparada por señal. | “batch and fed-batch”; “continuous feeding”; “signal-triggered feeding”.                                 | SRC-004. Páginas 3–6.                                                                                             | `Batch`; `FedBatch`; `FeedingStrategy`; `supportsFeedingStrategy`                                   | explícita                                              | alta      | no                 |
| AF-12 | Se documenta un umbral de DO mayor de 6 %.                                                                      | “DO > 6%”.                                                                                               | SRC-004. Páginas 3–6.                                                                                             | `DOLimit`; `hasThreshold`                                                                           | explícita                                              | alta      | sí                 |
| AF-13 | El corpus clasifica parámetros en físicos, biológicos y químicos.                                               | “physical, biological and chemical parameters”.                                                          | SRC-005. Secciones sobre sensores y variables de proceso.                                                         | `OperatingVariable`; `PhysicalParameter`; `BiologicalParameter`; `ChemicalParameter`                | explícita                                              | alta      | no                 |
| AF-14 | El corpus menciona control de lazo cerrado.                                                                     | “closed-loop control”.                                                                                   | SRC-005. Secciones sobre control.                                                                                 | `ControlLoop`; `controlsVariable`                                                                   | explícita                                              | media     | sí                 |
| AF-15 | Conviene separar lo monitorizado de lo actuado o controlado.                                                    | Monitoreo en línea en SRC-003, componentes de actuación en SRC-001 y control de lazo cerrado en SRC-005. | SRC-001, SRC-003 y SRC-005.                                                                                       | `monitorsVariable` y `controlsVariable` como relaciones separadas.                                  | inferida                                               | media     | sí                 |

---

## 4) Conceptos candidatos

| Concepto candidato    | Tipo sugerido     | Base documental                                                          | Fuente                    | Estado                         |
| --------------------- | ----------------- | ------------------------------------------------------------------------ | ------------------------- | ------------------------------ |
| `BioreactorSystem`    | Clase             | Sistema asociado a monitoreo, componentes, modos y alarmas.              | SRC-001, SRC-003          | candidato                      |
| `CultureVessel`       | Clase             | Se documentan recipientes con volumen de trabajo de 5 L y 10 L.          | SRC-002                   | candidato                      |
| `OperatingVariable`   | Clase             | Temperatura, pH, DO, biomasa, nivel, espuma, presión y otras variables.  | SRC-001, SRC-002, SRC-003 | candidato                      |
| `PhysicalParameter`   | Subclase          | Categoría documentada de parámetros.                                     | SRC-005                   | candidato                      |
| `BiologicalParameter` | Subclase          | Categoría documentada de parámetros.                                     | SRC-005                   | candidato                      |
| `ChemicalParameter`   | Subclase          | Categoría documentada de parámetros.                                     | SRC-005                   | candidato                      |
| `Sensor`              | Clase             | Inferido a partir de monitoreo en línea de variables.                    | SRC-003                   | candidato; requiere validación |
| `Actuator`            | Clase             | Inferido a partir de bombas, válvulas y controladores de flujo.          | SRC-001                   | candidato; requiere validación |
| `PeristalticPump`     | Subclase          | “Peristaltic pumps”.                                                     | SRC-001                   | candidato                      |
| `SolenoidValve`       | Subclase          | “solenoid valves”.                                                       | SRC-001                   | candidato                      |
| `MassFlowController`  | Subclase          | “mass flow controllers”.                                                 | SRC-001                   | candidato                      |
| `ProcessMode`         | Clase             | Batch, fed-batch, continuous y perfusion.                                | SRC-001, SRC-004, SRC-005 | candidato                      |
| `ProcessPhase`        | Clase             | No establecida directamente; el corpus habla de modos, no de fases.      | —                         | requiere validación            |
| `GassingMode`         | Clase             | “five different gassing modes”.                                          | SRC-003                   | candidato                      |
| `FeedingStrategy`     | Clase             | Continuous feeding y signal-triggered feeding.                           | SRC-004                   | candidato                      |
| `ControlLoop`         | Clase             | “closed-loop control”.                                                   | SRC-005                   | candidato                      |
| `AlarmCapability`     | Concepto auxiliar | Alarm contact y remote alarming.                                         | SRC-001                   | candidato                      |
| `ProcessEvent`        | Clase             | Inferido desde programación, señales y alimentación disparada por señal. | SRC-003, SRC-004          | requiere validación            |
| `OnlineProcessSignal` | Concepto auxiliar | “online process signals”.                                                | SRC-003                   | candidato                      |
| `PredefinedSchedule`  | Concepto auxiliar | “predefined schedule”.                                                   | SRC-003                   | candidato                      |

---

## 5) Relaciones candidatas con dominio y rango sugeridos

| Relación candidata        | Dominio sugerido   | Rango sugerido                               | Evidencia                                                             | Tipo      | Estado              |
| ------------------------- | ------------------ | -------------------------------------------- | --------------------------------------------------------------------- | --------- | ------------------- |
| `hasWorkingVolume`        | `CultureVessel`    | literal numérico con unidad                  | 5 L y 10 L.                                                           | explícita | candidata           |
| `hasOperatingVariable`    | `BioreactorSystem` | `OperatingVariable`                          | Variables documentadas en SRC-001 y SRC-002.                          | inferida  | candidata           |
| `monitorsVariable`        | `BioreactorSystem` | `OperatingVariable`                          | Monitoreo en línea de biomasa, pH, DO y fluorescencia.                | explícita | candidata           |
| `hasActuationComponent`   | `BioreactorSystem` | `Actuator`                                   | Bombas, válvulas y controladores de flujo.                            | inferida  | candidata           |
| `supportsProcessMode`     | `BioreactorSystem` | `ProcessMode`                                | Batch, fed-batch, continuous y perfusion.                             | explícita | candidata           |
| `supportsGassingMode`     | `BioreactorSystem` | `GassingMode`                                | Cinco modos de gasificación.                                          | explícita | candidata           |
| `supportsFeedingStrategy` | `BioreactorSystem` | `FeedingStrategy`                            | Alimentación continua y disparada por señal.                          | explícita | candidata           |
| `usesProcessAgent`        | `BioreactorSystem` | `FeedAgent` o `PHAgent`                      | Feed agents y pH agents.                                              | inferida  | requiere validación |
| `supportsAlarmCapability` | `BioreactorSystem` | `AlarmCapability`                            | Alarm contact y remote alarming.                                      | inferida  | requiere validación |
| `controlsVariable`        | `ControlLoop`      | `OperatingVariable`                          | Closed-loop control.                                                  | inferida  | requiere validación |
| `triggeredBy`             | `ProcessEvent`     | `OnlineProcessSignal` o `PredefinedSchedule` | Señales en línea, programación y signal-triggered feeding.            | inferida  | requiere validación |
| `hasProcessPhase`         | `BioreactorRun`    | `ProcessPhase`                               | No establecido directamente; las fuentes documentan modos de proceso. | inferida  | requiere validación |

---

## 6) Triadas RDF candidatas

| Triada RDF candidata                                                       | Documento y ubicación                     | Estado                      |
| -------------------------------------------------------------------------- | ----------------------------------------- | --------------------------- |
| `UnivesselGlass -> hasWorkingVolume -> "5 L"`                              | SRC-002, páginas 23–27 y 31–35.           | soportada                   |
| `UnivesselGlass -> hasWorkingVolume -> "10 L"`                             | SRC-002, páginas 23–27 y 31–35.           | soportada                   |
| `BioLectorXT -> monitorsVariable -> Biomass`                               | SRC-003, páginas 1–3.                     | soportada                   |
| `BioLectorXT -> monitorsVariable -> PH`                                    | SRC-003, páginas 1–3.                     | soportada                   |
| `BioLectorXT -> monitorsVariable -> DO`                                    | SRC-003, páginas 1–3.                     | soportada                   |
| `BioLectorXT -> monitorsVariable -> Fluorescence`                          | SRC-003, páginas 1–3.                     | soportada                   |
| `BioLectorXT -> supportsGassingMode -> GassingMode`                        | SRC-003, páginas 1–3.                     | soportada                   |
| `BioLectorXT -> supportsFeedingStrategy -> ContinuousFeeding`              | SRC-004, páginas 3–6.                     | soportada                   |
| `BioLectorXT -> supportsFeedingStrategy -> SignalTriggeredFeeding`         | SRC-004, páginas 3–6.                     | soportada                   |
| `SartoriusBioreactorSystem -> hasActuationComponent -> PeristalticPump`    | SRC-001, ubicación general suministrada.  | parcialmente soportada      |
| `SartoriusBioreactorSystem -> hasActuationComponent -> SolenoidValve`      | SRC-001, ubicación general suministrada.  | parcialmente soportada      |
| `SartoriusBioreactorSystem -> hasActuationComponent -> MassFlowController` | SRC-001, ubicación general suministrada.  | parcialmente soportada      |
| `SartoriusBioreactorSystem -> supportsProcessMode -> Batch`                | SRC-001, ubicación general suministrada.  | soportada                   |
| `SartoriusBioreactorSystem -> supportsProcessMode -> FedBatch`             | SRC-001, ubicación general suministrada.  | soportada                   |
| `SartoriusBioreactorSystem -> supportsProcessMode -> Continuous`           | SRC-001, ubicación general suministrada.  | soportada                   |
| `SartoriusBioreactorSystem -> supportsProcessMode -> Perfusion`            | SRC-001, ubicación general suministrada.  | soportada                   |
| `BioreactorSystem -> supportsAlarmCapability -> RemoteAlarming`            | SRC-001, secciones de alarmas.            | parcialmente soportada      |
| `ProcessEvent -> triggeredBy -> OnlineProcessSignal`                       | SRC-003 y SRC-004.                        | requiere validación experta |
| `BioreactorRun -> hasProcessPhase -> ProcessPhase`                         | No establecido en el corpus suministrado. | requiere validación experta |

---

## 7) Sinónimos documentados

| Término principal     | Sinónimos o variantes documentadas                   | Idioma | Documento                          |
| --------------------- | ---------------------------------------------------- | ------ | ---------------------------------- |
| `DO`                  | No se suministró una expansión o sinónimo explícito. | EN     | SRC-001, SRC-002, SRC-003, SRC-004 |
| `Batch`               | No se suministraron sinónimos explícitos.            | EN     | SRC-001, SRC-004, SRC-005          |
| `FedBatch`            | “fed-batch”                                          | EN     | SRC-001, SRC-004, SRC-005          |
| `OnlineMonitoring`    | “online-monitoring”                                  | EN     | SRC-003                            |
| `OnlineProcessSignal` | “online process signals”                             | EN     | SRC-003                            |

---

## 8) Vacíos del corpus

- No se identifican sensores físicos específicos para cada variable documentada.
- No se establece qué variables están únicamente monitorizadas, cuáles son controladas o cuáles cumplen ambas funciones.
- No se suministra una relación explícita entre cada actuador y la variable que modifica.
- No se establece que `DO > 6%` sea el umbral exacto que dispara una acción específica; solo se proporcionan ambos fragmentos en SRC-004.
- No se documentan tipos, códigos, severidades ni causas de alarmas.
- No se documentan fallas, errores, recuperación, paradas, pausas o abortos.
- No se documenta una estructura de registro histórico o bitácora de eventos.
- No se documentan fases biológicas del cultivo, tales como lag, exponential o stationary phase.
- No se establecen unidades para las variables, excepto los volúmenes de trabajo de 5 L y 10 L.
- No está establecido en el corpus suministrado si Sartorius 5 L y Sartorius 10 L deben modelarse como individuos, configuraciones o subclases.

---

## 9) Estado final

**Estado de la respuesta:** parcialmente soportado.

El corpus permite proponer relaciones candidatas entre sistemas de biorreactor, variables, modos de proceso, componentes de actuación, estrategias de alimentación, señales, programación y capacidades de alarma. La modelación detallada de sensores, control, fases y eventos requiere validación experta y documentación operativa adicional.
