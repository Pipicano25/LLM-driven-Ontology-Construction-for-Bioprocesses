## 1) ID y pregunta

- **ID:** ALC-02
- **Pregunta:** ¿Qué características mínimas debe tener un sistema para ser considerado biorreactor y no solo un recipiente de cultivo?

## 2) Respuesta basada en evidencia

### Evidencia explícita

El corpus caracteriza a los biorreactores como “controlled systems for cultivating microorganisms and cells” (sistemas controlados para cultivar microorganismos y células) [SRC-001].

También documenta que un sistema de control puede incluir componentes externos para ajustar condiciones de cultivo, por ejemplo bombas, y software de control [SRC-004]. En ejemplos concretos, se documenta control de temperatura, pH, DO y velocidad de agitación para configuraciones Biostat B [SRC-005], y control del pH del cultivo durante el experimento para BioLector XT [SRC-006].

### Inferencia razonable

Para responder operativamente la pregunta con este corpus, un sistema candidato a biorreactor debería combinar:

1. Capacidad de cultivar microorganismos o células.
2. Carácter de sistema controlado o capacidad de ajustar al menos una condición de cultivo.

Un recipiente de cultivo sin evidencia documentada de control de condiciones no puede confirmarse como biorreactor a partir del corpus suministrado.

### Información no establecida

No establecido en el corpus suministrado:

- Una definición explícita de `CultureVessel`.
- Una comparación textual directa entre “bioreactor” y “culture vessel”.
- Que todos los biorreactores requieran sensores.
- Que todos los biorreactores requieran actuadores.
- Que todo biorreactor deba usar control automático o lazo cerrado.
- Que pH, DO, temperatura o velocidad de agitación sean requisitos universales.
- Un volumen mínimo para clasificar un sistema como biorreactor.

## 3) Tabla de afirmaciones y evidencia

| ID    | Afirmación                                                                                                                                   | Texto o fragmento de evidencia                                                                                               | Fuente y ubicación                                                                | Concepto / relación / triada candidata                                                                                              | Tipo de evidencia | Confianza | Validación experta |
| ----- | -------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------- | ----------------- | --------- | ------------------ |
| AF-01 | Un biorreactor es caracterizado como un sistema controlado para cultivar microorganismos y células.                                          | “Bioreactors, controlled systems for cultivating microorganisms and cells”                                                   | SRC-001, Resumen                                                                  | `BioreactorSystem`; `BiologicalCultivationProcess`; `BioreactorSystem -> supportsCultivation -> BiologicalCultivationProcess`       | Explícita         | Alta      | No                 |
| AF-02 | Un sistema de control puede incluir componentes externos y software de control para ajustar condiciones de cultivo.                          | “A control system comprising external components used to adjust the culturing conditions (e.g., pumps) and control software” | SRC-004, PDF p. 4 impresa                                                         | `ControlSystem`; `ExternalComponent`; `Pump`; `ControlSoftware`; `ControlSystem -> adjustsCulturingCondition -> CulturingCondition` | Explícita         | Alta      | No                 |
| AF-03 | Un manipulador automatizado conectado a una unidad de control puede formar un mecanismo de control.                                          | “An automated handler (robotic arm) is connected to a control unit and together they form a control mechanism.”              | SRC-002, PDF p. 12, Figura 3                                                      | `AutomatedHandler`; `ControlUnit`; `ControlMechanism`; `AutomatedHandler -> connectedTo -> ControlUnit`                             | Explícita         | Alta      | No                 |
| AF-04 | El control avanzado de proceso es presentado como una necesidad crítica.                                                                     | “there has been a critical need for advanced process control”                                                                | SRC-003, Resumen                                                                  | `AdvancedProcessControl`                                                                                                            | Explícita         | Media     | No                 |
| AF-05 | Una configuración Biostat B lista opciones de volumen de 1 L, 2 L, 5 L y 10 L.                                                               | “Volume: 1 L, 2 L, 5 L or 10 L”                                                                                              | SRC-005, sección “Basic Configurations for Univessel® Glass — Microbial Packages” | `BiostatB_MicrobialPackage`; `hasListedVolume`                                                                                      | Explícita         | Alta      | No                 |
| AF-06 | Una configuración Biostat B controla temperatura, pH, DO y velocidad de agitación.                                                           | “Control temperature, pH, DO, stirrer speed”                                                                                 | SRC-005, sección “Basic Configurations for Univessel® Glass — Microbial Packages” | `ProcessParameter`; `Temperature`; `pH`; `DO`; `StirrerSpeed`; `controlsProcessParameter`                                           | Explícita         | Alta      | No                 |
| AF-07 | BioLector XT puede ofrecer control del pH del cultivo durante el experimento.                                                                | “while simultaneously offering control over the culture’s pH throughout the experiment.”                                     | SRC-006, PDF p. 1, resumen                                                        | `BioLectorXT_Microbioreactor`; `CulturePH`; `controlsProcessParameter`                                                              | Explícita         | Alta      | No                 |
| AF-08 | La presencia de control de condiciones de cultivo es un criterio funcional razonable para distinguir un biorreactor de un recipiente pasivo. | Basado en SRC-001 y SRC-004: “controlled systems” y “adjust the culturing conditions”.                                       | SRC-001, Resumen; SRC-004, PDF p. 4 impresa                                       | `BioreactorSystem -> hasProcessControlCapability -> ProcessControlCapability`                                                       | Inferida          | Media     | Sí                 |
| AF-09 | Un recipiente sin evidencia de control no puede clasificarse de forma confirmada como biorreactor usando solamente este corpus.              | No hay un fragmento que defina directamente `CultureVessel` ni que establezca equivalencia con `BioreactorSystem`.           | Corpus completo                                                                   | Regla de clasificación candidata                                                                                                    | Inferida          | Media     | Sí                 |

## 4) Conceptos candidatos

| Concepto candidato             | Tipo sugerido                               | Definición basada en el corpus                                                                             | Fuente asociada  | Estado    |
| ------------------------------ | ------------------------------------------- | ---------------------------------------------------------------------------------------------------------- | ---------------- | --------- |
| `BioreactorSystem`             | Clase                                       | Sistema controlado para cultivar microorganismos y células.                                                | SRC-001          | Candidato |
| `BiologicalCultivationProcess` | Clase                                       | Cultivo de microorganismos y células.                                                                      | SRC-001          | Candidato |
| `ControlSystem`                | Clase                                       | Sistema que incluye componentes externos y software para ajustar condiciones de cultivo.                   | SRC-004          | Candidato |
| `CulturingCondition`           | Clase                                       | Condición asociada al cultivo que puede ser ajustada.                                                      | SRC-004          | Candidato |
| `ExternalComponent`            | Clase                                       | Componente externo usado para ajustar condiciones de cultivo.                                              | SRC-004          | Candidato |
| `Pump`                         | Subclase o individuo de `ExternalComponent` | Ejemplo de componente externo usado para ajustar condiciones de cultivo.                                   | SRC-004          | Candidato |
| `ControlSoftware`              | Clase                                       | Software incluido en un sistema de control.                                                                | SRC-004          | Candidato |
| `AutomatedHandler`             | Clase                                       | Manipulador automatizado o brazo robótico conectado a una unidad de control.                               | SRC-002          | Candidato |
| `ControlUnit`                  | Clase                                       | Unidad conectada a un manipulador automatizado para formar un mecanismo de control.                        | SRC-002          | Candidato |
| `ControlMechanism`             | Clase                                       | Mecanismo formado por un manipulador automatizado y una unidad de control.                                 | SRC-002          | Candidato |
| `AdvancedProcessControl`       | Concepto auxiliar                           | Control avanzado de proceso presentado como necesidad crítica.                                             | SRC-003          | Candidato |
| `ProcessParameter`             | Clase                                       | Variable de proceso que puede ser controlada.                                                              | SRC-005, SRC-006 | Candidato |
| `Temperature`                  | Clase o individuo de `ProcessParameter`     | Parámetro listado como controlado.                                                                         | SRC-005          | Candidato |
| `pH`                           | Clase o individuo de `ProcessParameter`     | Parámetro listado como controlado; se documenta control del pH del cultivo.                                | SRC-005, SRC-006 | Candidato |
| `DO`                           | Clase o individuo de `ProcessParameter`     | Parámetro listado como controlado. La expansión de la sigla no está establecida en el corpus suministrado. | SRC-005          | Candidato |
| `StirrerSpeed`                 | Clase o individuo de `ProcessParameter`     | Parámetro listado como controlado.                                                                         | SRC-005          | Candidato |
| `BiostatB_MicrobialPackage`    | Individuo o clase de configuración          | Paquete que lista opciones de volumen y variables de control.                                              | SRC-005          | Candidato |
| `BioLectorXT_Microbioreactor`  | Individuo                                   | Sistema denominado “BioLector XT Microbioreactor” que ofrece control del pH del cultivo.                   | SRC-006          | Candidato |

## 5) Relaciones candidatas con dominio y rango sugeridos

| Relación candidata            | Dominio sugerido              | Rango sugerido                 | Evidencia                                                                             | Estado                      |
| ----------------------------- | ----------------------------- | ------------------------------ | ------------------------------------------------------------------------------------- | --------------------------- |
| `supportsCultivation`         | `BioreactorSystem`            | `BiologicalCultivationProcess` | SRC-001 describe biorreactores como sistemas para cultivar microorganismos y células. | Parcialmente soportada      |
| `hasControlSystem`            | `BioreactorSystem`            | `ControlSystem`                | SRC-004 describe un sistema de control en el contexto de biorreactores.               | Parcialmente soportada      |
| `adjustsCulturingCondition`   | `ControlSystem`               | `CulturingCondition`           | SRC-004: componentes usados para ajustar condiciones de cultivo.                      | Soportada                   |
| `hasComponent`                | `ControlSystem`               | `ExternalComponent`            | SRC-004: el sistema de control comprende componentes externos.                        | Soportada                   |
| `usesControlSoftware`         | `ControlSystem`               | `ControlSoftware`              | SRC-004: el sistema de control comprende software de control.                         | Soportada                   |
| `connectedTo`                 | `AutomatedHandler`            | `ControlUnit`                  | SRC-002: el manipulador automatizado está conectado a una unidad de control.          | Soportada                   |
| `formsControlMechanismWith`   | `AutomatedHandler`            | `ControlUnit`                  | SRC-002: ambos forman un mecanismo de control.                                        | Soportada                   |
| `controlsProcessParameter`    | `BiostatB_MicrobialPackage`   | `ProcessParameter`             | SRC-005: controla temperatura, pH, DO y velocidad de agitación.                       | Soportada                   |
| `hasListedVolume`             | `BiostatB_MicrobialPackage`   | `xsd:string`                   | SRC-005: lista 1 L, 2 L, 5 L y 10 L.                                                  | Soportada                   |
| `controlsProcessParameter`    | `BioLectorXT_Microbioreactor` | `pH`                           | SRC-006: ofrece control del pH del cultivo durante el experimento.                    | Soportada                   |
| `hasProcessControlCapability` | `BioreactorSystem`            | `ProcessControlCapability`     | Derivada de SRC-001 y SRC-004.                                                        | Requiere validación experta |

## 6) Triadas RDF candidatas

| Triada RDF candidata                                                          | Fuente y ubicación                                                                | Tipo de evidencia | Estado                      |
| ----------------------------------------------------------------------------- | --------------------------------------------------------------------------------- | ----------------- | --------------------------- |
| `BioreactorSystem -> supportsCultivation -> BiologicalCultivationProcess`     | SRC-001, Resumen                                                                  | Explícita         | Parcialmente soportada      |
| `ControlSystem -> adjustsCulturingCondition -> CulturingCondition`            | SRC-004, PDF p. 4 impresa                                                         | Explícita         | Soportada                   |
| `ControlSystem -> hasComponent -> ExternalComponent`                          | SRC-004, PDF p. 4 impresa                                                         | Explícita         | Soportada                   |
| `ControlSystem -> usesControlSoftware -> ControlSoftware`                     | SRC-004, PDF p. 4 impresa                                                         | Explícita         | Soportada                   |
| `AutomatedHandler -> connectedTo -> ControlUnit`                              | SRC-002, PDF p. 12, Figura 3                                                      | Explícita         | Soportada                   |
| `AutomatedHandler -> formsControlMechanismWith -> ControlUnit`                | SRC-002, PDF p. 12, Figura 3                                                      | Explícita         | Soportada                   |
| `BiostatB_MicrobialPackage -> hasListedVolume -> "1 L"`                       | SRC-005, sección “Basic Configurations for Univessel® Glass — Microbial Packages” | Explícita         | Soportada                   |
| `BiostatB_MicrobialPackage -> hasListedVolume -> "2 L"`                       | SRC-005, sección “Basic Configurations for Univessel® Glass — Microbial Packages” | Explícita         | Soportada                   |
| `BiostatB_MicrobialPackage -> hasListedVolume -> "5 L"`                       | SRC-005, sección “Basic Configurations for Univessel® Glass — Microbial Packages” | Explícita         | Soportada                   |
| `BiostatB_MicrobialPackage -> hasListedVolume -> "10 L"`                      | SRC-005, sección “Basic Configurations for Univessel® Glass — Microbial Packages” | Explícita         | Soportada                   |
| `BiostatB_MicrobialPackage -> controlsProcessParameter -> Temperature`        | SRC-005, sección “Basic Configurations for Univessel® Glass — Microbial Packages” | Explícita         | Soportada                   |
| `BiostatB_MicrobialPackage -> controlsProcessParameter -> pH`                 | SRC-005, sección “Basic Configurations for Univessel® Glass — Microbial Packages” | Explícita         | Soportada                   |
| `BiostatB_MicrobialPackage -> controlsProcessParameter -> DO`                 | SRC-005, sección “Basic Configurations for Univessel® Glass — Microbial Packages” | Explícita         | Soportada                   |
| `BiostatB_MicrobialPackage -> controlsProcessParameter -> StirrerSpeed`       | SRC-005, sección “Basic Configurations for Univessel® Glass — Microbial Packages” | Explícita         | Soportada                   |
| `BioLectorXT_Microbioreactor -> controlsProcessParameter -> CulturePH`        | SRC-006, PDF p. 1, resumen                                                        | Explícita         | Soportada                   |
| `BioreactorSystem -> hasProcessControlCapability -> ProcessControlCapability` | SRC-001, Resumen; SRC-004, PDF p. 4 impresa                                       | Inferida          | Requiere validación experta |

## 7) Sinónimos documentados

No se documentan sinónimos estrictos y explícitos para los conceptos principales en los fragmentos suministrados.

| Término principal | Expresiones relacionadas documentadas                                                 | Idioma | Fuente                    | Observación                                                               |
| ----------------- | ------------------------------------------------------------------------------------- | ------ | ------------------------- | ------------------------------------------------------------------------- |
| `Bioreactor`      | “Bioreactors”; “BioLector XT Microbioreactor”                                         | Inglés | SRC-001, SRC-006          | No se establece sinonimia estricta entre ambos términos.                  |
| `ProcessControl`  | “control mechanism”; “control system”; “advanced process control”; “control software” | Inglés | SRC-002, SRC-003, SRC-004 | Son expresiones relacionadas; no se establece que sean sinónimos exactos. |
| `pH`              | “culture’s pH”                                                                        | Inglés | SRC-005, SRC-006          | Variante contextual, no definición formal.                                |

## 8) Vacíos del corpus

- No establecido en el corpus suministrado: definición de `CultureVessel`.
- No establecido en el corpus suministrado: comparación directa entre un biorreactor y un recipiente de cultivo.
- No establecido en el corpus suministrado: requisitos universales de sensores, actuadores, software o control automático.
- No establecido en el corpus suministrado: si el control debe ser continuo, automático, manual, abierto, cerrado o basado en realimentación.
- No establecido en el corpus suministrado: si temperatura, pH, DO y velocidad de agitación son características mínimas o solamente parámetros disponibles en ciertas configuraciones.
- No establecido en el corpus suministrado: significado expandido de la sigla `DO`.
- No establecido en el corpus suministrado: tipo semántico preciso de los valores de volumen, por ejemplo volumen nominal, máximo, útil o de trabajo.
- No establecido en el corpus suministrado: si BioLector XT y Biostat B representan clases de equipo, configuraciones o individuos en la ontología.
- No establecido en el corpus suministrado: requisitos de esterilidad, asepsia, aireación, alimentación, muestreo, alarmas, registro de datos o seguridad.

## 9) Estado final

- **Estado de la respuesta:** Parcialmente soportado.
- **Justificación:** El corpus sustenta explícitamente que los biorreactores son sistemas controlados para cultivar microorganismos y células, y documenta ejemplos de control de condiciones de cultivo. Sin embargo, no contiene una definición directa de recipiente de cultivo ni una regla universal que establezca el conjunto mínimo definitivo de características para diferenciarlo de un biorreactor.
