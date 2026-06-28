## 1) ID y pregunta

- **ID:** ALC-05
- **Pregunta:** ¿Cómo se separan ontológicamente el equipo físico, el proceso biológico, el sistema de control, las variables medidas y los datos generados?

## 2) Respuesta basada en evidencia

La evidencia permite una separación preliminar en capas:

- **Equipo físico:** puede representarse como `sosa:System` cuando se trata de instrumento, equipo, software o agente que implementa un procedimiento. El corpus identifica un `ControlTower`, módulos de control de aireación, bombas y temperatura, y un `CultureVessel` disponible en versiones de 2 L, 5 L y 10 L.

- **Proceso biológico:** el corpus menciona parámetros de cultivo y define una actividad como algo que ocurre en el tiempo y actúa sobre o con entidades. Por ello, `CultivationActivity` o `CultivationRun` puede proponerse como candidato alineable con `prov:Activity`, pero esta asignación es una inferencia razonable, no una afirmación explícita.

- **Sistema de control:** el corpus documenta `TRIGGERED pH CONTROL (CLOSED LOOP CONTROLLER)`, control activo de pH según señales en línea y alimentación continua de hasta dos soluciones. Esto permite distinguir un sistema o procedimiento de control de la variable controlada.

- **Variables medidas o controladas:** biomasa, fluorescencia, pH y oxígeno disuelto se mencionan explícitamente como parámetros evaluados en tiempo real. Según SOSA, una `sosa:Property` es una cualidad identificable que puede observarse o sobre la cual se puede actuar. Por tanto, estas variables pueden proponerse como instancias o especializaciones de `sosa:Property`.

- **Datos generados:** no establecido en el corpus suministrado para archivos, series temporales, resultados numéricos, formatos de exportación, frecuencia de muestreo o conjuntos de datos concretos. PROV-O permite representar genéricamente que una actividad produce una nueva entidad, pero el corpus no identifica una entidad de datos específica producida por BioLector XT o Biostat B.

## 3) Tabla de afirmaciones y evidencia

| ID  | Afirmación                                                                                   | Texto o fragmento de evidencia                                                                                                    | Fuente y ubicación                         | Concepto, relación o triada candidata                                                                             | Tipo      | Confianza | Validación experta |
| --- | -------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------ | ----------------------------------------------------------------------------------------------------------------- | --------- | --------- | ------------------ |
| A01 | BioLector XT permite evaluación en tiempo real de parámetros de cultivo.                     | “The high-throughput microbioreactor enables real-time evaluation…”                                                               | SRC-001, descripción principal             | `BioLectorXT -> evaluatesCultivationParameter -> CultivationParameter`                                            | Explícita | Alta      | No                 |
| A02 | Biomasa, fluorescencia, pH y DO son parámetros evaluados por BioLector XT.                   | “…biomass, fluorescence, pH, dissolved oxygen in the liquid phase (DO)…”                                                          | SRC-001, descripción principal             | `Biomass`, `Fluorescence`, `pH`, `DissolvedOxygen` como candidatos a `sosa:Property`                              | Explícita | Alta      | No                 |
| A03 | Una propiedad puede observarse o ser objeto de una acción.                                   | “Property — identifiable quality of features of interest that can be observed or acted upon.”                                     | SRC-005, sección 5.3.2.2.2                 | `sosa:Property`                                                                                                   | Explícita | Alta      | No                 |
| A04 | Un sistema puede ser instrumento, equipo, software o agente que implementa un procedimiento. | “A sosa:System is an instrument or equipment, including software systems and agents where relevant, that implements a procedure…” | SRC-005, sección 5.3.5.1                   | `sosa:System`; `implementsProcedure`                                                                              | Explícita | Alta      | No                 |
| A05 | Existe control de pH activado y de lazo cerrado.                                             | “TRIGGERED pH CONTROL (CLOSED LOOP CONTROLLER)”                                                                                   | SRC-002, “Microfluidic Bioprocess Control” | `TriggeredPHControl`; `ControlSystem`                                                                             | Explícita | Alta      | No                 |
| A06 | El control de pH usa señales en línea y puede alimentar hasta dos soluciones.                | “Active control of pH according to online signals and continuous feeding of up to two solutions”                                  | SRC-002, “Microfluidic features”           | `controlsProperty`; `isGuidedBySignal`; `continuouslyFeedsSolution`                                               | Explícita | Alta      | Sí                 |
| A07 | La torre de control contiene módulos de control de aireación, bombas y temperatura.          | “The control tower contains both the aeration, pump and temperature control modules…”                                             | SRC-003, p. 6                              | `ControlTower`; `AerationControlModule`; `PumpControlModule`; `TemperatureControlModule`; `containsControlModule` | Explícita | Alta      | No                 |
| A08 | El recipiente está disponible en versiones de 2 L, 5 L y 10 L.                               | “The vessel is available as 2 L, 5 L and 10 L version.”                                                                           | SRC-004, párrafo previo a “Downloads”      | `CultureVessel`; `VesselVersion`; `hasAvailableVersion`                                                           | Explícita | Alta      | No                 |
| A09 | Una actividad ocurre durante un período de tiempo y actúa sobre o con entidades.             | “An activity is something that occurs over a period of time and acts upon or with entities.”                                      | SRC-006, sección 3.1                       | `prov:Activity`                                                                                                   | Explícita | Alta      | No                 |
| A10 | Una nueva entidad puede ser producida por una actividad.                                     | “Generation is the completion of production of a new entity by an activity.”                                                      | SRC-006, sección 4                         | `prov:Entity -> prov:wasGeneratedBy -> prov:Activity`                                                             | Explícita | Alta      | No                 |
| A11 | Una corrida de cultivo puede modelarse como actividad.                                       | Combinación de “cultivation parameters” y definición de actividad.                                                                | SRC-001; SRC-006, sección 3.1              | `CultivationRun -> rdf:type -> prov:Activity`                                                                     | Inferida  | Media     | Sí                 |
| A12 | El pH puede representarse como propiedad observada o controlada.                             | pH aparece como parámetro evaluado y como objetivo de control; una propiedad puede observarse o ser objeto de acción.             | SRC-001; SRC-002; SRC-005                  | `pH -> rdf:type -> sosa:Property`                                                                                 | Inferida  | Alta      | Sí                 |

## 4) Conceptos candidatos

| Concepto candidato         | Tipo sugerido                           | Evidencia asociada                                                                                  | Estado                      |
| -------------------------- | --------------------------------------- | --------------------------------------------------------------------------------------------------- | --------------------------- |
| `sosa:System`              | Clase                                   | SRC-005 define sistema como instrumento, equipo, software o agente que implementa un procedimiento. | Soportado                   |
| `BioreactorSystem`         | Subclase candidata de `sosa:System`     | SRC-001 describe BioLector XT como microbioreactor.                                                 | Parcialmente soportado      |
| `ControlTower`             | Clase                                   | SRC-003 identifica una torre de control.                                                            | Soportado                   |
| `ControlModule`            | Clase                                   | SRC-003 identifica módulos de aireación, bombas y temperatura.                                      | Soportado                   |
| `AerationControlModule`    | Subclase                                | SRC-003.                                                                                            | Soportado                   |
| `PumpControlModule`        | Subclase                                | SRC-003.                                                                                            | Soportado                   |
| `TemperatureControlModule` | Subclase                                | SRC-003.                                                                                            | Soportado                   |
| `CultureVessel`            | Clase                                   | SRC-004 menciona el recipiente en versiones de volumen.                                             | Soportado                   |
| `VesselVersion`            | Clase auxiliar                          | SRC-004 menciona versiones de 2 L, 5 L y 10 L.                                                      | Parcialmente soportado      |
| `TriggeredPHControl`       | Clase o individuo candidato             | SRC-002 identifica control de pH activado y de lazo cerrado.                                        | Soportado                   |
| `CultivationParameter`     | Clase candidata                         | SRC-001 menciona parámetros clave de cultivo.                                                       | Parcialmente soportado      |
| `Biomass`                  | Individuo o subclase de `sosa:Property` | SRC-001.                                                                                            | Parcialmente soportado      |
| `Fluorescence`             | Individuo o subclase de `sosa:Property` | SRC-001.                                                                                            | Parcialmente soportado      |
| `pH`                       | Individuo o subclase de `sosa:Property` | SRC-001, SRC-002, SRC-005.                                                                          | Parcialmente soportado      |
| `DissolvedOxygen`          | Individuo o subclase de `sosa:Property` | SRC-001.                                                                                            | Parcialmente soportado      |
| `OnlineSignal`             | Concepto auxiliar                       | SRC-002 menciona señales en línea.                                                                  | Parcialmente soportado      |
| `CultivationRun`           | Clase candidata                         | Alineamiento inferido entre cultivo y actividad.                                                    | Requiere validación experta |
| `prov:Activity`            | Clase                                   | SRC-006 define actividad.                                                                           | Soportado                   |
| `prov:Entity`              | Clase                                   | SRC-006 describe producción de una nueva entidad por una actividad.                                 | Soportado                   |
| `ProcessDataSet`           | Clase                                   | No establecido en el corpus suministrado.                                                           | No proponer como soportado  |

## 5) Relaciones candidatas con dominio y rango sugeridos

| Relación candidata              | Dominio sugerido   | Rango sugerido         | Evidencia                                                                                        | Estado                 |
| ------------------------------- | ------------------ | ---------------------- | ------------------------------------------------------------------------------------------------ | ---------------------- |
| `implementsProcedure`           | `sosa:System`      | `Procedure`            | SRC-005 indica que un sistema implementa un procedimiento.                                       | Soportada              |
| `containsControlModule`         | `ControlTower`     | `ControlModule`        | SRC-003 indica que la torre contiene módulos de aireación, bombas y temperatura.                 | Soportada              |
| `evaluatesCultivationParameter` | `BioreactorSystem` | `CultivationParameter` | SRC-001 describe evaluación en tiempo real de parámetros.                                        | Soportada              |
| `controlsProperty`              | `ControlSystem`    | `sosa:Property`        | SRC-002 describe control activo de pH; SRC-005 define propiedades sobre las que se puede actuar. | Inferida               |
| `isGuidedBySignal`              | `ControlSystem`    | `OnlineSignal`         | SRC-002 indica control de pH según señales en línea.                                             | Parcialmente soportada |
| `continuouslyFeedsSolution`     | `ControlSystem`    | `Solution`             | SRC-002 menciona alimentación continua de hasta dos soluciones.                                  | Soportada              |
| `hasAvailableVersion`           | `CultureVessel`    | `VesselVersion`        | SRC-004 identifica versiones de 2 L, 5 L y 10 L.                                                 | Parcialmente soportada |
| `prov:wasGeneratedBy`           | `prov:Entity`      | `prov:Activity`        | SRC-006 describe producción de una entidad por una actividad.                                    | Soportada              |

## 6) Triadas RDF candidatas

| ID  | Triada RDF candidata                                                | Fuente y ubicación                         | Tipo      | Confianza | Validación experta |
| --- | ------------------------------------------------------------------- | ------------------------------------------ | --------- | --------- | ------------------ |
| T01 | `BioLectorXT -> evaluatesCultivationParameter -> Biomass`           | SRC-001, descripción principal             | Explícita | Alta      | No                 |
| T02 | `BioLectorXT -> evaluatesCultivationParameter -> Fluorescence`      | SRC-001, descripción principal             | Explícita | Alta      | No                 |
| T03 | `BioLectorXT -> evaluatesCultivationParameter -> pH`                | SRC-001, descripción principal             | Explícita | Alta      | No                 |
| T04 | `BioLectorXT -> evaluatesCultivationParameter -> DissolvedOxygen`   | SRC-001, descripción principal             | Explícita | Alta      | No                 |
| T05 | `TriggeredPHControl -> controlsProperty -> pH`                      | SRC-002, “Microfluidic Bioprocess Control” | Inferida  | Alta      | Sí                 |
| T06 | `TriggeredPHControl -> isGuidedBySignal -> OnlineSignal`            | SRC-002, “Microfluidic features”           | Explícita | Alta      | Sí                 |
| T07 | `TriggeredPHControl -> continuouslyFeedsSolution -> Solution`       | SRC-002, “Microfluidic features”           | Explícita | Alta      | Sí                 |
| T08 | `ControlTower -> containsControlModule -> AerationControlModule`    | SRC-003, p. 6                              | Explícita | Alta      | No                 |
| T09 | `ControlTower -> containsControlModule -> PumpControlModule`        | SRC-003, p. 6                              | Explícita | Alta      | No                 |
| T10 | `ControlTower -> containsControlModule -> TemperatureControlModule` | SRC-003, p. 6                              | Explícita | Alta      | No                 |
| T11 | `UnivesselGlass -> hasAvailableVersion -> VesselVersion_2L`         | SRC-004, ubicación indicada                | Explícita | Alta      | No                 |
| T12 | `UnivesselGlass -> hasAvailableVersion -> VesselVersion_5L`         | SRC-004, ubicación indicada                | Explícita | Alta      | No                 |
| T13 | `UnivesselGlass -> hasAvailableVersion -> VesselVersion_10L`        | SRC-004, ubicación indicada                | Explícita | Alta      | No                 |
| T14 | `CultivationRun -> rdf:type -> prov:Activity`                       | SRC-001; SRC-006, sección 3.1              | Inferida  | Media     | Sí                 |
| T15 | `prov:Entity -> prov:wasGeneratedBy -> prov:Activity`               | SRC-006, sección 4                         | Explícita | Alta      | No                 |

## 7) Sinónimos documentados

| Término principal | Sinónimo o variante documentada             | Fuente  |
| ----------------- | ------------------------------------------- | ------- |
| `DissolvedOxygen` | “dissolved oxygen in the liquid phase (DO)” | SRC-001 |
| `DO`              | “dissolved oxygen in the liquid phase”      | SRC-001 |

No se establecen otros sinónimos documentados en el corpus suministrado.

## 8) Vacíos del corpus

- No se identifican sensores concretos, sus tipos, fabricantes, posiciones ni asociación directa con las variables medidas.
- No se establece qué unidad específica de BioLector XT, Biostat o recipiente está instalada en el laboratorio.
- No se establece que el recipiente de 5 L o 10 L esté conectado a una torre de control determinada.
- No se establecen organismo, medio de cultivo, biomasa objetivo, fases biológicas ni estados de proceso.
- No se establecen setpoints, límites, algoritmos PID, reglas de alarma o decisiones operativas.
- No se establecen resultados numéricos, archivos, series temporales, formatos de datos, frecuencia de muestreo ni procedimientos de exportación.
- No se establece una entidad de datos concreta generada por una corrida de cultivo.
- No se establecen relaciones directas entre sensores, observaciones, resultados y datos de proceso.

## 9) Estado final

**Parcialmente soportado.**

El corpus respalda la separación preliminar entre equipo físico, módulos de control, variables de cultivo, propiedades observables o actuables y actividades genéricas. La representación del proceso biológico como actividad es inferida. La capa de datos generados solo cuenta con soporte genérico de procedencia y no permite afirmar estructuras, archivos o resultados específicos.
