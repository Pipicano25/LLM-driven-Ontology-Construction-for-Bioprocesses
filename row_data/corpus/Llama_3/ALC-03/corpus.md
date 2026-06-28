## 1) ID y pregunta

**[ALC-03]:** ¿Cómo se diferencian conceptualmente BioLector XT, Sartorius 5 L y Sartorius 10 L como sistemas de bioproceso?

## 2) Respuesta basada en evidencia

Según el corpus, la diferenciación conceptual es de **escala, formato y propósito funcional**, no solo de tamaño:

- **BioLector XT** se define como _microbioreactor de alto rendimiento_ para screening: opera en formato microtiter plate desechable de 48 pocillos, volumen 800-2400 µL (1-2 mL), con sensores ópticos pre-calibrados y tecnología microfluídica para control de pH y alimentación, permitiendo 48/32 cultivos paralelos para evaluación en tiempo real de biomasa, fluorescencia, pH y DO.

- **Sartorius 5 L y Sartorius 10 L** se definen como _sistemas de bioreactor benchtop_ basados en la misma plataforma física (UniVessel® Glass) acoplada a una unidad de control BIOSTAT B-DCU. Comparten arquitectura de vessel de vidrio borosilicato/acero 316L y el mismo conjunto de sensores e instrumentación (pH, pO2, temperatura, espuma, nivel, gas mixing, alimentación gravimétrica, etc.), pero se diferencian por rango de volumen de trabajo y velocidad de agitación permitida.

- **Propósito en la cadena de escalado:** el corpus asigna explícitamente al BioLector XT el rol de "screening applications", y al 5 L el rol de "larger-scale lab production and as a starting point for scale-up". Para el 10 L no se establece propósito diferenciado en el corpus.

## 3) Tabla de afirmaciones y evidencia

| #   | Fragmento de evidencia                                                                                                                                                                                  | Fuente                       | Concepto/Relación/Triada candidata                                                        | Tipo                                       | Confianza | Validación experta |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------- | ----------------------------------------------------------------------------------------- | ------------------------------------------ | --------- | ------------------ |
| 1   | "High-throughput microbioreactor enables real-time evaluation of biomass, fluorescence, pH, dissolved oxygen in the liquid phase (DO), and other key cultivation parameters for aerobes and anaerobes." | [SRC-001] Features           | BioLectorXT rdf:type Microbioreactor ; hasCapability RealTimeEvaluation                   | explícita                                  | alta      | no                 |
| 2   | "Volume                                                                                                                                                                                                 | 800 - 2400 µL"               | [SRC-001] Specifications                                                                  | BioLectorXT hasWorkingVolume "800-2400 µL" | explícita | alta               |
| 3   | "ranging from 1 to 2 mL scale in a BioLector XT® for screening applications"                                                                                                                            | [SRC-006] Abstract           | BioLectorXT enablesApplication Screening                                                  | explícita                                  | alta      | no                 |
| 4   | "based on a standard ANSI/SLAS (SBS) microtiter plate (MTP) format, and operates with online, pre-calibrated optical sensors."                                                                          | [SRC-001] Features           | BioLectorXT hasFormat MTP ; hasSensorType OpticalPrecalibrated                            | explícita                                  | alta      | no                 |
| 5   | "Disposable 48 well MTPs enable online measurement"                                                                                                                                                     | [SRC-001] Features           | BioLectorXT hasVesselType DisposableMTP48                                                 | explícita                                  | alta      | no                 |
| 6   | "patented microfluidic technology supports simultaneous pH control and feeding."                                                                                                                        | [SRC-001] Features           | BioLectorXT hasControlMechanism MicrofluidicPHAndFeed                                     | explícita                                  | alta      | sí                 |
| 7   | "Real-time kinetics out of 48/32 parallel cultivations"                                                                                                                                                 | [SRC-001] Specifications     | BioLectorXT hasParallelization "48/32"                                                    | explícita                                  | alta      | no                 |
| 8   | "The vessel is available as 2 L, 5 L and 10 L version."                                                                                                                                                 | [SRC-002] Descripción        | Sartorius5L rdf:type UniVesselGlass ; Sartorius10L rdf:type UniVesselGlass                | explícita                                  | alta      | no                 |
| 9   | "UniVessel® Glass is our platform cultivation vessel for all Biostat® benchtop bioreactors. It is available in 1 L, 2 L, 5 L and 10 L working volume."                                                  | [SRC-004] Catalog            | UniVesselGlass isPlatformFor BiostatBenchtop                                              | explícita                                  | alta      | no                 |
| 10  | "Working volume: 2L (0.4-2L); 5L (0.6-5L); 10L (1.5-10L)"                                                                                                                                               | [SRC-005] Specifications     | Sartorius5L hasWorkingVolumeRange "0.6-5L" ; Sartorius10L hasWorkingVolumeRange "1.5-10L" | explícita                                  | alta      | no                 |
| 11  | "Permitted stirring speed: 2L (20-2000rpm); 5L (20-1500rpm); 10L (20-800rpm)"                                                                                                                           | [SRC-005] Specifications     | Sartorius5L hasMaxStirringSpeed "1500rpm" ; Sartorius10L hasMaxStirringSpeed "800rpm"     | explícita                                  | alta      | no                 |
| 12  | "Materials of major product wetted parts: Borosilicate glass, stainless steel AISI 316L, EPDM"                                                                                                          | [SRC-004] Catalog            | UniVesselGlass hasMaterial BorosilicateGlass                                              | explícita                                  | alta      | no                 |
| 13  | "The device is used as the control unit for various bioreactor systems in combination with the UniVessel Glass"                                                                                         | [SRC-003] Device Description | BIOSTAT-B-DCU controls UniVesselGlass                                                     | explícita                                  | alta      | no                 |
| 14  | "This control unit is used to cultivate biological cultures in liquids or aqueous nutrient solutions under controlled and reproducible conditions."                                                     | [SRC-003] Intended Use       | BIOSTAT-B-DCU enablesProcess ControlledCultivation                                        | explícita                                  | alta      | no                 |
| 15  | "designed for cultivating microorganisms and cells in discontinuous and continuous processes"                                                                                                           | [SRC-003] Device Description | SartoriusSystem supportsProcessType DiscontinuousAndContinuous                            | explícita                                  | alta      | no                 |
| 16  | "Sensors: pH, pO2, Temperature, Foam, Level, Substrate addition, Gas mixing, Agitation, Gravimetric Feed & Harvest Control"                                                                             | [SRC-005] Specifications     | SartoriusSystem hasSensorSuite MultiParameter                                             | explícita                                  | alta      | no                 |
| 17  | "up to a 5 L bioreactor for larger-scale lab production and as a starting point for scale-up for pilot and industry scale."                                                                             | [SRC-006] Abstract           | Sartorius5L enablesApplication LabProductionAndScaleUpStart                               | explícita                                  | alta      | no                 |
| 18  | "Bioreactor cultivations were conducted in a 5 L bioreactor (Biostat B5, Sartorius AG), equipped with two Rushton turbines."                                                                            | [SRC-006] Methods            | Sartorius5L hasImpellerType TwoRushtonTurbines                                            | explícita                                  | media     | sí                 |
| 19  | "Temperature control: 0 – 80 °C"                                                                                                                                                                        | [SRC-005] Specifications     | SartoriusSystem hasTemperatureRange "0-80C"                                               | explícita                                  | alta      | no                 |
| 20  | "Gas flow: air, O2, CO2\*, N2 (max. total flow rate 20 lpm)"                                                                                                                                            | [SRC-005] Specifications     | SartoriusSystem hasMaxGasFlow "20 lpm"                                                    | explícita                                  | alta      | no                 |

## 4) Conceptos candidatos

- BioLector XT
- Sartorius 5 L
- Sartorius 10 L
- Microbioreactor
- Bioreactor benchtop
- UniVessel Glass
- BIOSTAT B-DCU (unidad de control)
- High-throughput screening
- Lab production / Scale-up start point
- Working volume
- Microtiter plate (MTP) 48-well
- Sensor óptico pre-calibrado
- Tecnología microfluídica
- Proceso discontinuo y continuo

## 5) Relaciones candidatas con dominio y rango sugeridos

- **hasWorkingVolume** (Dominio: BioreactorSystem; Rango: VolumeRange) — diferencia cuantitativa clave
- **hasFormat** (Dominio: BioreactorSystem; Rango: VesselFormat) — MTP vs. Glass vessel
- **enablesApplication** (Dominio: BioreactorSystem; Rango: ApplicationType) — screening vs. producción lab
- **hasParallelization** (Dominio: Microbioreactor; Rango: xsd:integer)
- **isPlatformFor** (Dominio: Vessel; Rango: ControlUnit)
- **hasSensorType** (Dominio: BioreactorSystem; Rango: SensorTechnology)
- **hasMaxStirringSpeed** (Dominio: UniVesselGlass; Rango: SpeedRange)

## 6) Triadas RDF candidatas

```turtle
:BioLectorXT rdf:type :Microbioreactor ;
    :hasWorkingVolume "800-2400 µL" ;
    :hasFormat :MTP48Well ;
    :hasSensorType :OpticalPrecalibrated ;
    :enablesApplication :Screening ;
    :hasParallelization 48 .

:Sartorius5L rdf:type :BenchtopBioreactor ;
    :usesVessel :UniVesselGlass5L ;
    :hasWorkingVolumeRange "0.6-5L" ;
    :hasMaxStirringSpeed "1500rpm" ;
    :enablesApplication :LabProductionScaleUp .

:Sartorius10L rdf:type :BenchtopBioreactor ;
    :usesVessel :UniVesselGlass10L ;
    :hasWorkingVolumeRange "1.5-10L" ;
    :hasMaxStirringSpeed "800rpm" .

:UniVesselGlass :hasMaterial :BorosilicateGlass , :StainlessSteel316L .
```

## 7) Sinónimos documentados

- BioLector XT = "BioLector XT®", "BioLector XT microbioreactor" [SRC-001, SRC-006]
- Sartorius 5 L = "5 L bioreactor (Biostat B5, Sartorius AG)", "5L (0.6-5L)" [SRC-005, SRC-006]
- Sartorius 10 L = "10L version", "10L (1.5-10L)" [SRC-002, SRC-005]
- UniVessel Glass = "platform cultivation vessel for all Biostat® benchtop bioreactors" [SRC-004]

## 8) Vacíos del corpus

- No establecido en el corpus suministrado: propósito conceptual específico del Sartorius 10 L distinto del 5 L (más allá de volumen y rpm).
- No establecido: comparación directa de capacidades de control de pH/feed entre BioLector XT y Sartorius (solo se describen por separado).
- No establecido: materiales de construcción del BioLector XT.
- No establecido: si el Sartorius 10 L también usa "two Rushton turbines" (solo documentado para 5 L).
- No establecido: límites de paralelización o throughput para Sartorius.

## 9) Estado final

**Parcialmente soportado.** El corpus soporta con alta confianza la diferenciación BioLector XT (microescala, high-throughput, screening, MTP) vs. sistemas Sartorius (benchtop, UniVessel Glass, control unit, producción lab/escalado). La diferenciación entre Sartorius 5 L y 10 L está soportada solo por volumen de trabajo y velocidad de agitación máxima; el propósito conceptual diferencial no está establecido en el corpus suministrado.
