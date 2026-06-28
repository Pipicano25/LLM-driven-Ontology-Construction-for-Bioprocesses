## 1) ID y pregunta

**[ALC-01]:** ¿Qué se entiende por biorreactor dentro del proyecto, considerando BioLector XT, Sartorius 5 L y Sartorius 10 L?

## 2) Respuesta basada en evidencia

Trabajando exclusivamente con el corpus suministrado, no existe una definición única y explícita del término "biorreactor" para el proyecto.

Lo que sí se establece es:

- **BioLector XT:** se entiende como un _microbioreactor_ de sobremesa (_benchtop device_) para screening de alto rendimiento (_highthroughput_) de cultivos microbianos, con monitoreo en línea de biomasa, pH, oxígeno disuelto (DO) y fluorescencia. Opera en formato de microplacas MTP estándar ANSI/SLAS (SBS) de 32 o 48 pocillos, permitiendo hasta 48 experimentos simultáneos.

- **Sistemas Sartorius (referidos como "5 L" y "10 L" en la pregunta):** el corpus no utiliza esas denominaciones exactas. Lo que documenta es un sistema compuesto por:
  1. Una unidad de control **Biostat B-DCU**, usada como _control unit for various bioreactor systems_.
  2. Un recipiente de cultivo **UniVessel Glass**, descrito como _platform cultivation vessel for all Biostat benchtop bioreactors_, disponible en volúmenes de trabajo de 1 L, 2 L, **5 L y 10 L**.

  Ese conjunto se usa para _cultivate biological cultures in liquids or aqueous nutrient solutions under controlled and reproducible conditions_, para microorganismos y células, en procesos discontinuos y continuos, y a _various reactor volumes_.

Por tanto, en el corpus "biorreactor" se describe funcionalmente (cultivar bajo condiciones controladas) y mediante dos materializaciones diferentes: un microbioreactor de microplaca (BioLector XT) y un sistema de biorreactor de sobremesa con vessel de vidrio (UniVessel 5 L / 10 L + Biostat B-DCU).

## 3) Tabla de afirmaciones y evidencia

| Fragmento de evidencia                                                                                                                                                                                                                              | Fuente                                     | Concepto/Relación/Triada candidata                                                                                | Tipo                                                                                        | Confianza | Validación experta |
| --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------ | ----------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- | --------- | ------------------ |
| "The BioLector XT microbioreactor is a benchtop device for highthroughput screening of microbial cultivations in combination with onlinemonitoring of common cultivation parameters such as biomass, pH, dissolved oxygen (DO) and fluorescence..." | SRC-001, Introducción pág. 1               | BioLectorXT rdf:type Microbioreactor ; hasFormFactor BenchtopDevice                                               | explícita                                                                                   | alta      | no                 |
| "High throughput cultivations are carried out in SBS/SLAS standard format microtiter plates (MTPs) with 32 or 48 cultivation wells each, allowing up to 48 simultaneous experiments in one microbioreactor run."                                    | SRC-001, Introducción pág. 1               | BioLectorXT usesFormat MTP ; hasWellCount 32/48 ; hasCapacity 48                                                  | explícita                                                                                   | alta      | no                 |
| "High-throughput microbioreactor enables real-time evaluation of biomass, fluorescence, pH, dissolved oxygen in the liquid phase (DO), and other key cultivation parameters for aerobes and anaerobes."                                             | SRC-002, Sección ventajas                  | BioLectorXT monitors Parameter ; supports OrganismType (Aerobes, Anaerobes)                                       | explícita                                                                                   | alta      | no                 |
| "BioLector XT microbioreactor is based on a standard ANSI/SLAS (SBS) microtiter plate (MTP) format, and operates with online, pre-calibrated optical sensors."                                                                                      | SRC-002, Sección ventajas                  | BioLectorXT hasSensorType OpticalSensor ; hasCalibrationState PreCalibrated                                       | explícita                                                                                   | alta      | no                 |
| "The device is used as the control unit for various bioreactor systems in combination with the UniVessel Glass or UniVessel SU."                                                                                                                    | SRC-003, Safety Information – Intended Use | BiostatB-DCU rdf:type ControlUnit ; isComponentOf BioreactorSystem ; hasCompatibleVessel UniVesselGlass           | explícita                                                                                   | alta      | no                 |
| "This control unit is used to cultivate biological cultures in liquids or aqueous nutrient solutions under controlled and reproducible conditions."                                                                                                 | SRC-003, Device Overview                   | BioreactorSystem hasFunction Cultivation ; hasOperatingCondition Controlled                                       | explícita                                                                                   | alta      | no                 |
| "The device is designed for cultivating microorganisms and cells in discontinuous and continuous processes."                                                                                                                                        | SRC-003, Device Overview                   | BioreactorSystem supportsProcessType (Discontinuous, Continuous) ; supportsBiologicalEntity (Microorganism, Cell) | explícita                                                                                   | alta      | no                 |
| "It was designed for cultivating microorganisms and cells at various reactor volumes."                                                                                                                                                              | SRC-003, Device Overview                   | BioreactorSystem hasProperty ReactorVolume                                                                        | explícita                                                                                   | media     | sí                 |
| "The Univessel® Glass is our platform cultivation vessel for all Biostat® benchtop bioreactors. It is available in 1 L, 2 L, 5 L and 10 L working volume."                                                                                          | SRC-004, Catálogo                          | UniVesselGlass rdf:type CultivationVessel ; isPlatformFor BiostatBenchtop ; hasWorkingVolume 5L, 10L              | explícita                                                                                   | alta      | no                 |
| "Working volume 0.35–1 0.6–2 0.6–5 1.5                                                                                                                                                                                                              | 5–10"                                      | SRC-004, Catálogo                                                                                                 | UniVessel5L hasWorkingVolumeRange "0.6–5 L" ; UniVessel10L hasWorkingVolumeRange "1.5–10 L" | explícita | media              |
| "Material Borosilicate glass, stainless steel AISI 316L, EPDM"                                                                                                                                                                                      | SRC-004, Catálogo                          | UniVesselGlass hasMaterial (BorosilicateGlass, Steel316L, EPDM)                                                   | explícita                                                                                   | alta      | no                 |
| "Sartorius 5 L y Sartorius 10 L son biorreactores del proyecto"                                                                                                                                                                                     | No establecido en el corpus suministrado   | —                                                                                                                 | —                                                                                           | —         | sí                 |

## 4) Conceptos candidatos

- Biorreactor
- Microbioreactor
- BioLector XT
- Biostat B-DCU (Control Unit)
- UniVessel Glass (Cultivation Vessel)
- Sistema de Biorreactor
- Cultivo microbiano
- Parámetro de cultivo (Biomasa, pH, DO, Fluorescencia)
- Microtiter Plate (MTP)
- Sensor óptico
- Volumen de trabajo
- Proceso discontinuo / continuo

## 5) Relaciones candidatas con dominio y rango sugeridos

- **rdf:type**: Biorreactor → Clase
- **hasFormFactor**: Microbioreactor → {BenchtopDevice}
- **monitors**: BioLectorXT → ParámetroDeCultivo
- **usesFormat**: BioLectorXT → MTP
- **hasWellCount**: BioLectorXT → xsd:integer
- **isComponentOf**: ControlUnit → BioreactorSystem
- **hasCompatibleVessel**: ControlUnit → CultivationVessel
- **hasFunction**: BioreactorSystem → Cultivation
- **supportsProcessType**: BioreactorSystem → {Discontinuous, Continuous}
- **hasWorkingVolume**: CultivationVessel → xsd:decimal
- **hasMaterial**: CultivationVessel → Material

## 6) Triadas RDF candidatas

```
:BioLectorXT rdf:type :Microbioreactor.
:BioLectorXT :hasFormFactor :Benchtop.
:BioLectorXT :monitors :Biomass, :pH, :DO, :Fluorescence.
:BioLectorXT :usesFormat :MTP_SBS.
:BioLectorXT :hasWellCount 48.

:BiostatB-DCU rdf:type :ControlUnit.
:BiostatB-DCU :isComponentOf :BioreactorSystem.
:BiostatB-DCU :hasCompatibleVessel :UniVesselGlass.

:UniVesselGlass rdf:type :CultivationVessel.
:UniVesselGlass :isPlatformFor :BiostatBenchtop.
:UniVesselGlass_5L :hasWorkingVolume "5".
:UniVesselGlass_10L :hasWorkingVolume "10".
:UniVesselGlass :hasMaterial :BorosilicateGlass.

:BioreactorSystem :hasFunction :Cultivation.
:BioreactorSystem :hasOperatingCondition :ControlledReproducible.
```

## 7) Sinónimos documentados

- "microbioreactor" = "BioLector XT microbioreactor" (SRC-001, SRC-002)
- "MTPs" = "microtiter plates" (SRC-001)
- "SBS/SLAS standard format" = "ANSI/SLAS (SBS)" (SRC-001, SRC-002)
- "device" = "control unit" (en contexto Biostat B-DCU, SRC-003)
- "bioreactor systems" = combinación de control unit + UniVessel Glass/SU (SRC-003)

## 8) Vacíos del corpus

- No hay definición explícita y unificada de "biorreactor" aplicable al proyecto.
- No se mencionan literalmente los términos "Sartorius 5 L" ni "Sartorius 10 L"; solo se documentan volúmenes de UniVessel Glass.
- No se establece si "biorreactor" en el proyecto incluye solo el vessel, o el conjunto control+vessel+sensores.
- No se comparan escalas entre BioLector XT (microlitros) y UniVessel (litros).
- No se describen parámetros de control para los sistemas Sartorius (solo función general).
- No se define relación jerárquica entre Microbioreactor y Biorreactor.

## 9) Estado final

**parcialmente soportado**

La evidencia soporta qué es el BioLector XT y cuáles son los componentes y volúmenes de los sistemas Biostat/UniVessel, pero no proporciona una definición ontológica explícita de "biorreactor" dentro del proyecto ni vincula directamente las denominaciones "Sartorius 5 L" y "Sartorius 10 L".
