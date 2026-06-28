## 1. Identificación de la pregunta

**ID:** ALC-03

**Nivel metodológico:** Conceptual / comparativo multiescala

**Tema:** Sistemas de bioproceso BioLector XT, Sartorius 5 L y Sartorius 10 L

**Pregunta:** ¿Cómo se diferencian conceptualmente BioLector XT, Sartorius 5 L y Sartorius 10 L como sistemas de bioproceso?

## 2. Propósito de la pregunta

Busca establecer las diferencias de principio entre un sistema de microbioreactor de alto rendimiento y dos biorreactores agitados de banco, para fundamentar la ontología de escalas, volúmenes, instrumentación y funciones. Contribuye al corpus definiendo clases base (microscale vs benchtop stirred-tank), propiedades de escala y equivalencias funcionales necesarias para representar screening, optimización y producción a escala laboratorio.

## 3. Plan de búsqueda documental

**Información técnica requerida:**

- Principio de operación, volumen de trabajo, paralelización
- Sensores y actuadores, control de pH/DO, alimentación
- Materiales, esterilización, compatibilidad con controladores
- Rangos operativos (temperatura, agitación, gases)

**Tipos de documentos necesarios:** manuales técnicos oficiales, fichas de fabricante, brochure técnico, artículo revisado por pares con uso comparativo.

**Repositorios sugeridos:** beckman.com, sartorius.com, ManualsLib, PMC, A\*STAR equipment database

**Términos de búsqueda:**

- ES: "BioLector XT microbioreactor", "Sartorius Biostat B 5 L", "Univessel 10 L especificaciones"
- EN: "BioLector XT specifications", "Biostat B-DCU operating instructions", "Univessel Glass 5L 10L working volume"

**Ecuaciones de búsqueda:** ("BioLector XT" AND specifications) OR ("Biostat B" AND "5 L" AND "10 L") OR ("Univessel Glass" AND "working volume")

**Criterios inclusión/exclusión:** ver sección del prompt; priorizar 2021-2026.

## 4. Documentos candidatos encontrados

| ID documento | Título                                                                | Entidad autora                      | Año                         | Tipo de fuente              | URL/DOI verificable                               | Relación con la pregunta                                                | Decisión preliminar |
| ------------ | --------------------------------------------------------------------- | ----------------------------------- | --------------------------- | --------------------------- | ------------------------------------------------- | ----------------------------------------------------------------------- | ------------------- |
| DOC-01       | BioLector XT Microbioreactor – Features and Specifications            | Beckman Coulter Life Sciences       | s.f. (vigente 2024-2025)    | Ficha técnica oficial       | https://media.beckman.com                         | Define principio, volumen 800-2400 µL, sensores ópticos, paralelización | Include             |
| DOC-02       | Univessel® Glass – Autoclavable Cultivation Vessel                    | Sartorius AG                        | s.f.                        | Página producto oficial     | https://sartorius.com                             | Confirma disponibilidad 2 L, 5 L, 10 L                                  | Include             |
| DOC-03       | BIOSTAT B-DCU Operating Instructions Manual                           | Sartorius Stedim Biotech            | s.f. (versión 85037-549-98) | Manual técnico              | https://manualslib.com                            | Define uso con UniVessel Glass/SU, control multiescala                  | Include             |
| DOC-04       | Univessel Glass Reliability and Continuity (brochure)                 | Sartorius AG                        | 2022                        | Brochure técnico            | https://pdf.directindustry.com                    | Especifica volúmenes de trabajo 1-10 L, materiales                      | Include             |
| DOC-05       | Bioreactor: Sartorius 10 (w/MFCS) – BIOSTAT B specifications          | A\*STAR Scientific Equipment Finder | s.f.                        | Base datos institucional    | https://asef.a-star.edu.sg                        | Rangos volumen, agitación, gases para 5 L y 10 L                        | Include             |
| DOC-06       | Optimizing Yeast Surface-Displayed Unspecific Peroxygenase Production | MDPI Bioengineering / PMC           | 2025                        | Artículo revisado por pares | https://pmc.ncbi.nlm.nih.gov/articles/PMC12383419 | Uso comparativo BioLector XT (1-2 mL) vs Biostat B5 (5 L)               | Include             |

## 5. Evaluación de documentos candidatos

**DOC-01**

- Relevancia: Alta
- Autoridad: Alta – fabricante
- Trazabilidad: Alta
- Cobertura: Volumen, sensores ópticos, gassing, microfluídica
- Justificación: Include

**DOC-02**

- Relevancia: Media
- Autoridad: Alta
- Trazabilidad: Alta
- Cobertura: disponibilidad 2 L, 5 L, 10 L
- Justificación: Include

**DOC-03**

- Relevancia: Alta
- Autoridad: Alta
- Trazabilidad: Alta
- Cobertura: uso con UniVessel para cultivo en condiciones controladas y reproducibles; diseño para varios volúmenes
- Justificación: Include

**DOC-04**

- Relevancia: Alta
- Autoridad: Alta
- Trazabilidad: Alta
- Cobertura: "available in 1 L, 2 L, 5 L and 10 L working volume"; materiales borosilicato, AISI 316L
- Justificación: Include

**DOC-05**

- Relevancia: Alta
- Autoridad: Media (institucional)
- Trazabilidad: Alta
- Cobertura: working volume 5L (0.6-5L); 10L (1.5-10L); stirring 5L 20-1500rpm; 10L 20-800rpm; gas flow max 20 lpm; temperatura 0-80°C
- Justificación: Include

**DOC-06**

- Relevancia: Alta
- Autoridad: Alta – peer-review
- Trazabilidad: Alta
- Cobertura: "ranging from 1 to 2 mL scale in a BioLector XT® for screening... up to a 5 L bioreactor"; Biostat B5 con dos turbinas Rushton
- Justificación: Include

## 6. Corpus documental seleccionado

| ID     | Documento seleccionado       | Pregunta asociada | Fragmentos relevantes                                                   | Estado     |
| ------ | ---------------------------- | ----------------- | ----------------------------------------------------------------------- | ---------- |
| DOC-01 | BioLector XT Microbioreactor | ALC-03            | volumen 800-2400 µL, sensores ópticos pre-calibrados, placa 48 pocillos | Verificado |
| DOC-03 | BIOSTAT B-DCU Manual         | ALC-03            | Uso con UniVessel Glass/SU; cultivo en condiciones controladas          | Verificado |
| DOC-04 | Univessel Glass brochure     | ALC-03            | Volúmenes 1-10 L working; materiales                                    | Verificado |
| DOC-05 | A\*STAR Biostat B specs      | ALC-03            | Working volume y agitación 5L/10L; gases                                | Verificado |
| DOC-06 | PMC 2025 artículo            | ALC-03            | Comparación escala screening vs 5L                                      | Verificado |

## 7. Respuesta basada en evidencia

**Evidencia explícita:**

- BioLector XT es un microbioreactor de alto rendimiento basado en formato microtiter ANSI/SLAS, con sensores ópticos pre-calibrados en línea. Permite evaluación en tiempo real de biomasa, fluorescencia, pH y oxígeno disuelto para aerobios y anaerobios【8009893174837283377†L2-L4】.
- Su volumen de trabajo es 800 – 2400 µL, con 48/32 cultivos paralelos【8009893174837283377†L106-L107】.
- El sistema Sartorius utiliza UniVessel Glass como vaso plataforma para biorreactores de banco Biostat, disponible en 1 L, 2 L, 5 L y 10 L de volumen de trabajo【7994170111834507682†L34-L36】, con versiones 2 L, 5 L y 10 L confirmadas【2950214818290998553†L19-L21】.
- BIOSTAT B-DCU se usa con UniVessel Glass o SU para cultivar en condiciones controladas y reproducibles【2441582828990923054†L78-L81】, diseñado para varios volúmenes【2441582828990923054†L112-L115】.
- Para Biostat B, volumen de trabajo 5 L (0.6–5 L) y 10 L (1.5–10 L)【724095730734625047†L15-L17】, agitación 5L 20–1500 rpm y 10L 20–800 rpm【724095730734625047†L15-L17】, flujo gas máximo 20 lpm【724095730734625047†L17-L18】, temperatura 0–80 °C【724095730734625047†L19-L21】.
- En literatura, BioLector XT se emplea para screening a 1–2 mL, mientras el biorreactor de 5 L se usa para producción a escala laboratorio【2598993920621889847†L55-L58】.

**Inferencia razonable:**

- BioLector XT es sistema de screening paralelizado sin esterilización in situ; Sartorius 5 L/10 L son biorreactores agitados autoclavables con sondas invasivas. Diferencia de escala >2000x.
- Sartorius 5 L y 10 L comparten controlador, difieren en geometría y rango de agitación.

**Información no establecida:**

- No hay comparación directa de kLa o potencia específica entre sistemas en el corpus.

## 8. Tabla de afirmaciones y evidencia

| ID  | Afirmación                                                      | Tipo      | Documento | Fragmento fiel                                                                                                                                                                                             |
| --- | --------------------------------------------------------------- | --------- | --------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | 
| E01 | BioLector XT opera con placas de 48 pocillos y sensores ópticos | Explícita | DOC-01    | "based on a standard ANSI/SLAS (SBS) microtiter plate (MTP) format, and operates with online, pre-calibrated optical sensors"【8009893174837283377†L5-L7】                                                 |
| E02 | Volumen BioLector XT 800-2400 µL                                | Explícita | DOC-01    | "Volume 800 - 2400 µL"【8009893174837283377†L106-L107】 |
| E03 | Permite 48/32 cultivos paralelos                                | Explícita | DOC-01    | "Real-time kinetics out of 48/32 parallel cultivations"【8009893174837283377†L82-L84】                                                                                                                     |
| E04 | UniVessel disponible 1-10 L                                     | Explícita | DOC-04    | "It is available in 1 L, 2 L, 5 L and 10 L working volume"【7994170111834507682†L34-L36】                                                                                                                  |
| E05 | Biostat B con UniVessel para cultivo controlado                 | Explícita | DOC-03    | "device is used as the control unit for various bioreactor systems in combination with the UniVessel Glass or UniVessel SU... under controlled and reproducible conditions"【2441582828990923054†L78-L81】 |
| E06 | Working volume 5L 0.6-5L, 10L 1.5-10L                           | Explícita | DOC-05    | "Working volume: 2L (0.4-2L); 5L (0.6-5L); 10L (1.5-10L)"【724095730734625047†L15-L17】                                                                                                                    |
| E07 | Agitación 5L 20-1500 rpm, 10L 20-800 rpm                        | Explícita | DOC-05    | "Permitted stirring speed: 2L (20-2000rpm); 5L (20-1500rpm); 10L (20-800rpm)"【724095730734625047†L15-L17】                                                                                                |
| E08 | BioLector XT para screening 1-2 mL vs 5L producción             | Explícita | DOC-06    | "ranging from 1 to 2 mL scale in a BioLector XT® for screening applications... up to a 5 L bioreactor for larger-scale lab production"【2598993920621889847†L55-L58】                                      |
| E09 | Biostat B5 con dos turbinas Rushton                             | Explícita | DOC-06    | "Bioreactor cultivations were conducted in a 5 L bioreactor (Biostat B5, Sartorius AG...), equipped with two Rushton turbines"【2598993920621889847†L96-L99】                                              |

## 9. Conceptos ontológicos candidatos

| Concepto                           | Tipo      | Definición                                         | Fuente |
| ---------------------------------- | --------- | -------------------------------------------------- | ------ |
| BioreactorSystem                   | Clase     | Sistema para cultivar bajo condiciones controladas | DOC-03 |
| MicroscaleHighThroughputBioreactor | Subclase  | Bioreactor microtiter con sensores ópticos <3 mL   | DOC-01 |
| BenchtopStirredTankBioreactor      | Subclase  | Biorreactor agitado autoclavable                   | DOC-04 |
| BioLectorXT                        | Individuo | 48 pocillos, 800-2400 µL                           | DOC-01 |
| SartoriusBiostatB5L                | Individuo | UniVessel 5 L, 0.6-5 L                             | DOC-05 |
| SartoriusBiostatB10L               | Individuo | UniVessel 10 L, 1.5-10 L                           | DOC-05 |

## 10. Relaciones ontológicas candidatas

| Relación                   | Dominio                            | Rango                         | Significado             |
| -------------------------- | ---------------------------------- | ----------------------------- | ----------------------- |
| hasWorkingVolumeRange      | BioreactorSystem                   | xsd:string                    | Rango volumétrico       |
| enablesParallelCultivation | MicroscaleHighThroughputBioreactor | xsd:integer                   | Cultivos simultáneos    |
| usesVesselType             | BenchtopStirredTankBioreactor      | Vessel                        | Asocia UniVessel        |
| hasStirringSpeedRange      | BenchtopStirredTankBioreactor      | xsd:string                    | Rango rpm               |
| isScaleDownModelOf         | MicroscaleHighThroughputBioreactor | BenchtopStirredTankBioreactor | Screening vs producción |

## 11. Triadas RDF candidatas

- BioLectorXT -> rdf:type -> MicroscaleHighThroughputBioreactor (soportada)
- BioLectorXT -> hasWorkingVolumeRange -> "800-2400 µL" (soportada)
- SartoriusBiostatB5L -> hasWorkingVolumeRange -> "0.6-5 L" (soportada)
- SartoriusBiostatB10L -> hasWorkingVolumeRange -> "1.5-10 L" (soportada)
- SartoriusBiostatB5L -> hasStirringSpeedRange -> "20-1500 rpm" (soportada)
- SartoriusBiostatB10L -> hasStirringSpeedRange -> "20-800 rpm" (soportada)

## 12. Sinónimos y variantes

| Término        | Sinónimos                                        |
| -------------- | ------------------------------------------------ |
| BioLector XT   | Microbioreactor, high-throughput microbioreactor |
| Sartorius 5 L  | Biostat B5, UniVessel Glass 5 L                  |
| Sartorius 10 L | Biostat B 10L, UniVessel Glass 10 L              |

## 13. Vacíos y riesgos

- Falta kLa y potencia específica comparativa
- Separar controlador de vaso en ontología
- Validar relación isScaleDownModelOf con expertos

## 14. Registro metodológico

Se analizó ALC-03 con fuentes oficiales Beckman y Sartorius y artículo 2025. Se seleccionaron cinco documentos del corpus. La evidencia diferencia BioLector XT (microscale paralelizado) de Sartorius 5/10 L (agitados autoclavables). Se propusieron conceptos OWL candidatos.

## 15. Estado final

- **Confianza:** Medio-Alto
- **Respuesta:** Parcialmente soportada
- **Corpus:** Parcial
- **Próxima acción:** Aportar manuales completos Biostat B-DCU y curvas kLa BioLector XT
