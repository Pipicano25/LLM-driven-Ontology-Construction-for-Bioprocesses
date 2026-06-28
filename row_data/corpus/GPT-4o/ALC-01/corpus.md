# Extracción de conocimiento para ontología OWL/RDF de biorreactores multiescala

## 1. ID y pregunta

**ID:** `ALC-01`  

**Pregunta:** ¿Qué se entiende por biorreactor dentro del proyecto, considerando BioLector XT, Sartorius 5 L y Sartorius 10 L?

---

## 2. Respuesta basada en evidencia

Dentro del corpus, un **biorreactor** se entiende provisionalmente como un aparato manufacturado que permite generar un entorno específico para el cultivo altamente controlado de células vivas.

En ese marco:

- **BioLector XT** está explícitamente identificado como un **microbiorreactor de sobremesa**, basado en el formato estándar de microplaca ANSI/SLAS (SBS), destinado al cribado de alto rendimiento de cultivos microbianos y usado en combinación con monitorización en línea.
- **Biostat B** está explícitamente descrito como un **biorreactor de sobremesa**.
- **UniVessel Glass** está descrito como un recipiente de cultivo de plataforma para biorreactores Biostat de sobremesa y se ofrece, entre otros, en volúmenes de trabajo de **5 L** y **10 L**.

Por tanto, el corpus respalda tratar a BioLector XT y a configuraciones Sartorius asociadas con recipientes UniVessel Glass de 5 L o 10 L como parte del dominio de biorreactores de diferentes escalas operativas.

Sin embargo, que los nombres del proyecto “Sartorius 5 L” y “Sartorius 10 L” designen exactamente configuraciones concretas de Biostat B con UniVessel Glass **no establecido en el corpus suministrado**.

---

## 3. Tabla de afirmaciones y evidencia

| ID | Afirmación | Fragmento de evidencia | Fuente y ubicación | Concepto / relación candidata | Tipo de evidencia | Confianza | Validación experta |
|---|---|---|---|---|---|---|---|
| A01 | Un biorreactor es un aparato manufacturado para generar un entorno específico de cultivo altamente controlado. | “Bioreactors are manufactured apparatuses that allow the generation of a specific environment for the highly controlled cultivation of living cells.” | `SRC-007`, Abstract | `Bioreactor`; `supportsCultivation` | Explícita | Alta | No |
| A02 | Los biorreactores pueden distinguirse por material de construcción, mezcla, volumen de trabajo y propósito. | “Bioreactors can be separated into different types based on their material of construction, mechanism of mixing, working volume and overall purpose.” | `SRC-006`, FAQ “What Are the Different Types of Bioreactors?” | `mayBeClassifiedBy` | Explícita | Alta | No |
| A03 | BioLector XT es un microbiorreactor basado en formato de microplaca estándar ANSI/SLAS (SBS). | “the BioLector XT microbioreactor is based on a standard ANSI/SLAS (SBS) microtiter plate (MTP) format” | `SRC-001`, descripción principal; “Features of the BioLector XT” | `BioLectorXT rdf:type Microbioreactor`; `basedOnFormat` | Explícita | Alta | No |
| A04 | BioLector XT es un equipo de sobremesa para cribado de alto rendimiento de cultivos microbianos, en combinación con monitorización en línea. | “The BioLector XT microbioreactor is a bench-top device for high-throughput screening of microbial cultivations in combination with online-monitoring” | `SRC-003`, “Introduction” | `usedFor`; `usedInCombinationWith`; `BenchTopDevice` | Explícita | Alta | No |
| A05 | BioLector XT incluye evidencia documental de optodos de oxígeno y de un intervalo de control de pH condicionado por la placa. | “OXYGEN OPTODES 0 – 100 % dissolved oxygen”; “pH control range: 4.0 – 7.5 (depending on plate)” | `SRC-002`, “Cultivation conditions” y “Microfluidic features” | `hasOxygenOptode`; `hasPHControlRange` | Explícita | Alta | No |
| A06 | El sistema BioLector fue seleccionado en un estudio como plataforma de cultivo HTP. | “we selected the BioLector micro-bioreactor (µ-bioreactor) system as an HTP cultivation platform” | `SRC-009`, Abstract | `HighThroughputCultivationPlatform` | Explícita | Alta | No |
| A07 | Biostat B es un biorreactor de sobremesa para laboratorio. | “Our Biostat® B is the ideal benchtop bioreactor for your lab.” | `SRC-004`, “Biostat® B at a Glance”, p. 2 | `BiostatB rdf:type BenchtopBioreactor` | Explícita | Alta | No |
| A08 | UniVessel Glass es un recipiente de cultivo de plataforma para los biorreactores Biostat de sobremesa. | “The Univessel® Glass is our platform cultivation vessel for all Biostat® benchtop bioreactors.” | `SRC-005`, resumen inicial | `UnivesselGlass rdf:type CultivationVessel`; `platformVesselFor` | Explícita | Alta | No |
| A09 | UniVessel Glass está disponible en volúmenes de trabajo de 5 L y 10 L. | “It is available in 1 L, 2 L, 5 L and 10 L working volume.” | `SRC-005`, tabla “Inside Dimensions”, p. 8 | `hasAvailableWorkingVolume` | Explícita | Alta | No |
| A10 | “Sartorius 5 L” y “Sartorius 10 L” pueden modelarse provisionalmente como configuraciones asociadas a UniVessel Glass de 5 L y 10 L. | Integración de A07–A09; no aparece el nombre exacto de esas configuraciones en los fragmentos. | `SRC-004`, p. 2; `SRC-005`, resumen inicial y p. 8 | `Sartorius5LConfiguration`; `Sartorius10LConfiguration` | Inferida | Media | Sí |

---

## 4. Conceptos candidatos

| Concepto candidato | Tipo ontológico preliminar | Evidencia |
|---|---|---|
| `Bioreactor` | Clase | A01 |
| `Microbioreactor` | Subclase candidata de `Bioreactor` | A03; relación de subclase inferida |
| `BenchtopBioreactor` | Subclase candidata de `Bioreactor` | A07; relación de subclase inferida |
| `BioLectorXT` | Instancia o sistema de producto | A03–A05 |
| `BiostatB` | Instancia o sistema de producto | A07 |
| `CultivationVessel` | Clase | A08 |
| `UnivesselGlass` | Instancia o familia de recipiente de cultivo | A08–A09 |
| `WorkingVolume` | Clase o especificación de cantidad | A02, A09 |
| `MicrotiterPlateFormat` | Clase | A03 |
| `OnlineMonitoring` | Capacidad o componente funcional | A04 |
| `OxygenOptode` | Instrumento o sensor candidato | A05 |
| `DissolvedOxygen` | Variable de proceso | A05 |
| `PHControlRange` | Especificación operativa | A05 |
| `HighThroughputCultivationScreening` | Actividad o finalidad | A04, A06 |
| `Sartorius5LConfiguration` | Configuración candidata de proyecto | A10; requiere validación |
| `Sartorius10LConfiguration` | Configuración candidata de proyecto | A10; requiere validación |

---

## 5. Relaciones candidatas con dominio y rango sugeridos

| Relación candidata | Dominio | Rango | Soporte |
|---|---|---|---|
| `supportsCultivation` | `Bioreactor` | `LivingCellCultivation` | Explícito, `SRC-007` |
| `mayBeClassifiedBy` | `Bioreactor` | `ClassificationCriterion` | Explícito, `SRC-006` |
| `basedOnFormat` | `BioLectorXT` | `MicrotiterPlateFormat` | Explícito, `SRC-001` |
| `usedFor` | `BioLectorXT` | `HighThroughputCultivationScreening` | Explícito, `SRC-003` |
| `usedInCombinationWith` | `BioLectorXT` | `OnlineMonitoring` | Explícito, `SRC-003` |
| `hasOxygenOptode` | `BioLectorXT` | `OxygenOptode` | Explícito, `SRC-002` |
| `hasDissolvedOxygenRange` | `BioLectorXT` | `MeasurementRange` | Explícito, `SRC-002` |
| `hasPHControlRange` | `BioLectorXT` | `ControlRange` | Explícito, `SRC-002` |
| `platformVesselFor` | `CultivationVessel` | `BiostatBenchtopBioreactorCategory` | Explícito, `SRC-005` |
| `hasAvailableWorkingVolume` | `CultivationVessel` | `WorkingVolume` | Explícito, `SRC-005` |
| `usesCultivationVessel` | `Sartorius5LConfiguration` / `Sartorius10LConfiguration` | `UnivesselGlass` | Inferido; requiere validación |
| `hasWorkingVolume` | `Sartorius5LConfiguration` / `Sartorius10LConfiguration` | `WorkingVolume` | Inferido; requiere validación |

---

## 6. Triadas RDF candidatas

Prefijo local provisional: `ex:`.

```turtle
ex:Bioreactor ex:supportsCultivation ex:LivingCellCultivation .

ex:BioLectorXT a ex:Microbioreactor ;
    ex:basedOnFormat ex:ANSI_SLAS_SBS_MicrotiterPlateFormat ;
    ex:usedFor ex:HighThroughputMicrobialCultivationScreening ;
    ex:usedInCombinationWith ex:OnlineMonitoring ;
    ex:hasOxygenOptode ex:OxygenOptode ;
    ex:hasDissolvedOxygenRange "0–100 %" ;
    ex:hasPHControlRange "4.0–7.5; depending on plate" .

ex:BiostatB a ex:BenchtopBioreactor .

ex:UnivesselGlass a ex:PlatformCultivationVessel ;
    ex:hasAvailableWorkingVolume "5 L" ;
    ex:hasAvailableWorkingVolume "10 L" .
```

### Triadas condicionadas a validación experta

```turtle
ex:Sartorius5LConfiguration
    ex:usesCultivationVessel ex:UnivesselGlass ;
    ex:hasWorkingVolume "5 L" .

ex:Sartorius10LConfiguration
    ex:usesCultivationVessel ex:UnivesselGlass ;
    ex:hasWorkingVolume "10 L" .
```

---

## 7. Sinónimos documentados

| Término | Variante documentada | Evidencia | Estado |
|---|---|---|---|
| `micro-bioreactor` | `µ-bioreactor` | “BioLector micro-bioreactor (µ-bioreactor) system” | Equivalencia explícita, `SRC-009` |
| `microbioreactor` | `micro-bioreactor` | “BioLector XT microbioreactor” frente a “BioLector micro-bioreactor” | Variante terminológica inferida entre fuentes; validación recomendable |
| `benchtop bioreactor` | biorreactor de sobremesa | El término aparece en `SRC-004` y `SRC-005`; la forma española es una traducción de trabajo | No documentado como sinónimo textual en el corpus |
| `cultivation vessel` | recipiente de cultivo | La forma española es una traducción de trabajo de “cultivation vessel” | No documentado como sinónimo textual en el corpus |

No hay sinónimos documentados para “Sartorius 5 L” ni “Sartorius 10 L”.

---

## 8. Vacíos del corpus

- La identidad comercial, controlador, accesorios y composición exacta de los sistemas llamados “Sartorius 5 L” y “Sartorius 10 L”: **No establecido en el corpus suministrado**.
- La afirmación de que Biostat B es específicamente el sistema utilizado en las configuraciones de 5 L y 10 L del proyecto: **No establecido en el corpus suministrado**.
- El volumen de trabajo concreto de BioLector XT: **No establecido en el corpus suministrado**.
- La equivalencia funcional, operativa o semántica entre BioLector XT, Sartorius 5 L y Sartorius 10 L: **No establecido en el corpus suministrado**.
- Reglas de escalado, criterios de comparabilidad y variables comunes entre escalas: **No establecido en el corpus suministrado**.
- Inventario de sensores, actuadores, alarmas, eventos, fases de proceso y mecanismos de control para los equipos Sartorius de 5 L y 10 L: **No establecido en el corpus suministrado**.
- Que la disponibilidad de UniVessel Glass de 5 L o 10 L implique automáticamente que todo el sistema Sartorius tenga ese volumen operativo efectivo: **No establecido en el corpus suministrado**.

---

## 9. Estado final

**Parcialmente soportado.**

El corpus permite definir una clase amplia de biorreactor e identificar explícitamente a BioLector XT como microbiorreactor y a Biostat B como biorreactor de sobremesa, además de documentar recipientes UniVessel Glass de 5 L y 10 L.

La correspondencia exacta entre esos recipientes y los sistemas de proyecto denominados “Sartorius 5 L” y “Sartorius 10 L” requiere validación experta.
