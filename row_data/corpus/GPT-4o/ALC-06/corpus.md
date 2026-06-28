## 1) ID y pregunta

**ID:** ALC-06
**Pregunta:** ¿Qué propiedades generales deben describir cualquier biorreactor del proyecto, independientemente de su escala o volumen?

## 2) Respuesta basada en evidencia

El corpus no establece una lista universal, obligatoria y definitiva de propiedades para todos los biorreactores. Sin embargo, sí permite proponer una capa descriptiva mínima candidata.

La evidencia explícita identifica como dimensiones de clasificación: `ConstructionMaterial`, `MixingMechanism`, `WorkingVolume` y `OverallPurpose` (SRC-006). También aparecen aspectos operativos como `Agitation`, `Aeration`, `Temperature`, `pH`, `NutrientSupply` y `ProductRemoval` (SRC-007); variables de medición como `Biomass`, `Fluorescence`, `pH` y `DissolvedOxygen` en BioLector XT (SRC-001); y elementos de control, automatización y comparabilidad multiescala, incluidos `ControlStrategy`, `Automation`, `Substrate`, `DissolvedCO2` y `MixingTime` (SRC-008, SRC-009).

**Inferencia razonable:** para describir cualquier biorreactor del proyecto, la ontología preliminar debería considerar, como candidatos: identidad o propósito, arquitectura física, mecanismo de mezcla, capacidad o volumen de trabajo, condiciones y aspectos de operación, variables medidas, estrategia de control o automatización y descriptores relevantes para comparación entre escalas.

No queda establecido en el corpus suministrado que todas estas propiedades sean obligatorias para cada tipo de sistema ni que alarmas, fallas, eventos, muestreo o calidad de datos tengan cobertura documental suficiente.

## 3) Tabla de afirmaciones y evidencia

| ID   | Afirmación                                                                                                                                                           | Texto o fragmento de evidencia                                                                                                                                          | Fuente y ubicación                | Concepto / relación / triada candidata                                                                | Tipo      | Confianza | Validación experta |
| ---- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------- | ----------------------------------------------------------------------------------------------------- | --------- | --------- | ------------------ |
| A-01 | Los biorreactores pueden describirse por material de construcción, mecanismo de mezcla, volumen de trabajo y propósito general.                                      | “material of construction”, “mechanism of mixing”, “working volume” y “overall purpose”.                                                                                | SRC-006; L239-L246.               | `ConstructionMaterial`; `MixingMechanism`; `WorkingVolume`; `OverallPurpose`.                         | Explícita | Alta      | Sí                 |
| A-02 | La comparabilidad entre escalas puede considerar estrategias de control armonizadas.                                                                                 | “scalable and interchangeable” y “harmonized control strategies”.                                                                                                       | SRC-006; L153-L166.               | `ScaleCompatibility`; `ControlStrategy`; `hasScaleCompatibility`.                                     | Explícita | Alta      | Sí                 |
| A-03 | BioLector XT permite evaluación en tiempo real de biomasa, fluorescencia, pH y oxígeno disuelto.                                                                     | “The high-throughput microbioreactor enables real-time evaluation of biomass, fluorescence, pH, dissolved oxygen in the liquid phase (DO)”.                             | SRC-001; L436-L438.               | `MeasuredVariable`; `Biomass`; `Fluorescence`; `pH`; `DissolvedOxygen`; `measures`.                   | Explícita | Alta      | No                 |
| A-04 | Las condiciones de cultivo, dimensiones del sistema, dimensiones de la tapa de gaseado y características microfluídicas son aspectos documentados para BioLector XT. | “Microfluidic Bioprocess Control. Cultivation conditions, system dimensions, Gassing lid dimensions, Microfluidic features and more”.                                   | SRC-002; L413-L473 y L517-L557.   | `CultivationCondition`; `SystemDimension`; `GassingLidDimension`; `MicrofluidicFeature`.              | Explícita | Alta      | Sí                 |
| A-05 | Biostat B se describe como controlador de sobremesa aplicable a fermentación microbiana y cultivo celular.                                                           | “El Sartorius Biostat® B es un controlador de sobremesa universal flexible y satisface diferentes demandas, desde la fermentación microbiana hasta el cultivo celular”. | SRC-003; L155-L163 y L226-L257.   | `BenchtopBioreactorController`; `MicrobialFermentation`; `CellCulture`; `supportsApplication`.        | Explícita | Alta      | No                 |
| A-06 | Un recipiente de cultivo de vidrio borosilicato autoclavable está disponible en volúmenes de 1 L, 2 L, 5 L y 10 L.                                                   | “Our proven autoclavable borosilicate glass culture vessel is available in four different volumes: 1 L, 2 L, 5 L and 10 L”.                                             | SRC-004; P2-P3, P7-P10 y P16-P22. | `CultureVessel`; `BorosilicateGlassCultureVessel`; `availableInVolume`.                               | Explícita | Alta      | No                 |
| A-07 | Univessel Glass está disponible con volúmenes de trabajo de 1 L, 2 L, 5 L y 10 L.                                                                                    | “The Univessel® Glass is our platform cultivation vessel for all Biostat® benchtop bioreactors. It is available in 1 L, 2 L, 5 L and 10 L working volume”.              | SRC-005; L2-L13.                  | `UnivesselGlass`; `WorkingVolume`; `hasWorkingVolume`.                                                | Explícita | Alta      | No                 |
| A-08 | La operación de biorreactores incluye agitación, aireación, temperatura, pH, suministro de nutrientes y retiro de producto.                                          | “agitation, aeration, temperature, pH, nutrient supply, product removal”.                                                                                               | SRC-007; L175-L176 y L287-L292.   | `ProcessOperationAspect`; `Agitation`; `Aeration`; `Temperature`; `NutrientSupply`; `ProductRemoval`. | Explícita | Alta      | Sí                 |
| A-09 | Para la comparación multiescala son candidatos relevantes sustrato, DO, pH, temperatura, CO₂ disuelto y tiempo de mezcla.                                            | “substrate, DO, pH, temperature and dissolved CO₂”; “mixing time”.                                                                                                      | SRC-008; L97-L112 y L131-L133.    | `ScaleRelevantDescriptor`; `Substrate`; `DissolvedCO2`; `MixingTime`; `hasScaleRelevantDescriptor`.   | Inferida  | Media     | Sí                 |
| A-10 | Control y automatización deben representarse como dimensiones candidatas de descripción del sistema.                                                                 | “industrial aspects of a process and automation along with various commercial control strategies”.                                                                      | SRC-009; Abstract, L48-L52.       | `Automation`; `ControlStrategy`; `usesControlStrategy`; `hasAutomationCapability`.                    | Inferida  | Media     | Sí                 |
| A-11 | El volumen no debe ser el único descriptor ontológico de un biorreactor.                                                                                             | Convergencia de SRC-006 sobre material, mezcla, volumen y propósito; SRC-007 sobre operación; SRC-001 sobre variables medidas.                                          | SRC-001, SRC-006 y SRC-007.       | `BioreactorSystem`; `hasWorkingVolume`; `usesMixingMechanism`; `hasOverallPurpose`; `measures`.       | Inferida  | Media     | Sí                 |

## 4) Conceptos candidatos

| Concepto candidato             | Tipo sugerido             | Base documental                                                   | Estado               |
| ------------------------------ | ------------------------- | ----------------------------------------------------------------- | -------------------- |
| `BioreactorSystem`             | Clase                     | Síntesis de SRC-001, SRC-006 y SRC-007.                           | Candidato; inferido  |
| `BenchtopBioreactorController` | Clase                     | Biostat B es descrito como controlador de sobremesa.              | Candidato; explícito |
| `CultureVessel`                | Clase                     | SRC-004 y SRC-005 mencionan culture vessel y cultivation vessel.  | Candidato; explícito |
| `ConstructionMaterial`         | Concepto auxiliar         | SRC-006 menciona material of construction.                        | Candidato; explícito |
| `MixingMechanism`              | Concepto auxiliar         | SRC-006 menciona mechanism of mixing.                             | Candidato; explícito |
| `WorkingVolume`                | Propiedad de dato         | SRC-005 indica working volume.                                    | Candidato; explícito |
| `OverallPurpose`               | Concepto auxiliar         | SRC-006 menciona overall purpose.                                 | Candidato; explícito |
| `CultivationCondition`         | Clase o concepto auxiliar | SRC-002 menciona cultivation conditions.                          | Candidato; explícito |
| `SystemDimension`              | Propiedad de dato         | SRC-002 menciona system dimensions.                               | Candidato; explícito |
| `MicrofluidicFeature`          | Clase o concepto auxiliar | SRC-002 menciona microfluidic features.                           | Candidato; explícito |
| `MeasuredVariable`             | Clase                     | SRC-001 enumera biomass, fluorescence, pH y DO.                   | Candidato; inferido  |
| `ProcessOperationAspect`       | Clase                     | SRC-007 enumera aspectos operativos.                              | Candidato; inferido  |
| `ControlStrategy`              | Clase                     | SRC-006 y SRC-009 mencionan control strategies.                   | Candidato; inferido  |
| `Automation`                   | Clase o concepto auxiliar | SRC-009 menciona automation.                                      | Candidato; explícito |
| `ScaleRelevantDescriptor`      | Clase o concepto auxiliar | SRC-008 contiene variables y mixing time en contexto multiescala. | Candidato; inferido  |
| `MixingTime`                   | Propiedad de dato         | SRC-008 menciona mixing time.                                     | Candidato; explícito |

## 5) Relaciones candidatas

| Relación candidata           | Dominio sugerido                     | Rango sugerido            | Significado                                                  | Evidencia          | Estado                            |
| ---------------------------- | ------------------------------------ | ------------------------- | ------------------------------------------------------------ | ------------------ | --------------------------------- |
| `hasConstructionMaterial`    | `BioreactorSystem`                   | `ConstructionMaterial`    | Asocia un sistema con su material de construcción.           | SRC-006.           | Candidata; requiere validación    |
| `usesMixingMechanism`        | `BioreactorSystem`                   | `MixingMechanism`         | Indica el mecanismo de mezcla.                               | SRC-006.           | Candidata; requiere validación    |
| `hasWorkingVolume`           | `BioreactorSystem` o `CultureVessel` | Literal con unidad        | Registra el volumen de trabajo.                              | SRC-005 y SRC-006. | Candidata; requiere validación    |
| `hasOverallPurpose`          | `BioreactorSystem`                   | `OverallPurpose`          | Registra el propósito general del sistema.                   | SRC-006.           | Candidata; requiere validación    |
| `measures`                   | `BioreactorSystem`                   | `MeasuredVariable`        | Vincula un sistema con una variable medida.                  | SRC-001.           | Candidata; parcialmente soportada |
| `hasCultivationCondition`    | `BioreactorSystem`                   | `CultivationCondition`    | Asocia condiciones documentadas de cultivo.                  | SRC-002.           | Candidata; requiere validación    |
| `supportsApplication`        | `BenchtopBioreactorController`       | `CultureApplication`      | Indica aplicaciones de cultivo o fermentación soportadas.    | SRC-003.           | Candidata; parcialmente soportada |
| `usesControlStrategy`        | `BioreactorSystem`                   | `ControlStrategy`         | Vincula un sistema con una estrategia de control.            | SRC-006 y SRC-009. | Candidata; requiere validación    |
| `hasScaleRelevantDescriptor` | `BioreactorSystem`                   | `ScaleRelevantDescriptor` | Registra descriptores útiles para comparación entre escalas. | SRC-008.           | Candidata; requiere validación    |

## 6) Triadas RDF candidatas

| Triada RDF candidata                                                  | Fuente y ubicación                   | Tipo de evidencia | Confianza | Validación experta |
| --------------------------------------------------------------------- | ------------------------------------ | ----------------- | --------- | ------------------ |
| `BioreactorSystem -> hasConstructionMaterial -> ConstructionMaterial` | SRC-006; L239-L246.                  | Inferida          | Media     | Sí                 |
| `BioreactorSystem -> usesMixingMechanism -> MixingMechanism`          | SRC-006; L239-L246.                  | Inferida          | Media     | Sí                 |
| `BioreactorSystem -> hasWorkingVolume -> WorkingVolume`               | SRC-005; L2-L13; SRC-006; L239-L246. | Inferida          | Media     | Sí                 |
| `BioreactorSystem -> hasOverallPurpose -> OverallPurpose`             | SRC-006; L239-L246.                  | Inferida          | Media     | Sí                 |
| `BioLectorXT -> measures -> Biomass`                                  | SRC-001; L436-L438.                  | Explícita         | Alta      | No                 |
| `BioLectorXT -> measures -> Fluorescence`                             | SRC-001; L436-L438.                  | Explícita         | Alta      | No                 |
| `BioLectorXT -> measures -> pH`                                       | SRC-001; L436-L438.                  | Explícita         | Alta      | No                 |
| `BioLectorXT -> measures -> DissolvedOxygen`                          | SRC-001; L436-L438.                  | Explícita         | Alta      | No                 |
| `BioLectorXT -> hasCultivationCondition -> CultivationCondition`      | SRC-002; L413-L473 y L517-L557.      | Inferida          | Media     | Sí                 |
| `BioLectorXT -> hasSystemDimension -> SystemDimension`                | SRC-002; L413-L473 y L517-L557.      | Inferida          | Media     | Sí                 |
| `BiostatB -> rdf:type -> BenchtopBioreactorController`                | SRC-003; L155-L163 y L226-L257.      | Explícita         | Alta      | No                 |
| `BiostatB -> supportsApplication -> MicrobialFermentation`            | SRC-003; L155-L163 y L226-L257.      | Explícita         | Alta      | No                 |
| `BiostatB -> supportsApplication -> CellCulture`                      | SRC-003; L155-L163 y L226-L257.      | Explícita         | Alta      | No                 |
| `UnivesselGlass -> hasWorkingVolume -> "1 L"`                         | SRC-005; L2-L13.                     | Explícita         | Alta      | No                 |
| `UnivesselGlass -> hasWorkingVolume -> "2 L"`                         | SRC-005; L2-L13.                     | Explícita         | Alta      | No                 |
| `UnivesselGlass -> hasWorkingVolume -> "5 L"`                         | SRC-005; L2-L13.                     | Explícita         | Alta      | No                 |
| `UnivesselGlass -> hasWorkingVolume -> "10 L"`                        | SRC-005; L2-L13.                     | Explícita         | Alta      | No                 |
| `BioreactorSystem -> hasScaleRelevantDescriptor -> MixingTime`        | SRC-008; L97-L112 y L131-L133.       | Inferida          | Media     | Sí                 |
| `BioreactorSystem -> usesControlStrategy -> ControlStrategy`          | SRC-009; Abstract, L48-L52.          | Inferida          | Media     | Sí                 |

## 7) Sinónimos documentados

| Término principal | Sinónimo o variante documentada | Idioma | Fuente              |
| ----------------- | ------------------------------- | ------ | ------------------- |
| `DissolvedOxygen` | `DO`                            | Inglés | SRC-001; L436-L438. |

No se establecen otros sinónimos de manera explícita en el corpus suministrado.

## 8) Vacíos del corpus

- No establecido en el corpus suministrado que exista una lista universal y obligatoria de propiedades para todo biorreactor.
- No establecido en el corpus suministrado qué propiedades deben ser obligatorias en OWL, cuáles opcionales y cuáles dependientes del tipo de equipo.
- No establecido en el corpus suministrado el detalle de sensores, actuadores, alarmas, fallas, eventos, decisiones, muestreo o calidad de datos.
- No establecido en el corpus suministrado un modelo común de interfaces físicas entre BioLector XT y los recipientes Sartorius.
- No establecido en el corpus suministrado el rango operativo, la unidad y la semántica precisa de todas las condiciones de cultivo mencionadas en SRC-002.
- No establecido en el corpus suministrado que `Substrate`, `DissolvedCO2` o `MixingTime` deban representarse para cada ejecución experimental; solo son candidatos relevantes para comparación multiescala.
- La separación ontológica entre `BioreactorSystem`, `BioreactorController` y `CultureVessel` requiere validación experta.

## 9) Estado final

**Estado:** Parcialmente soportado.

El corpus sustenta propiedades candidatas de clasificación, volumen, mezcla, propósito, operación, medición, automatización y comparabilidad multiescala. No sustenta todavía un conjunto definitivo de axiomas o requisitos universales para todos los equipos.
