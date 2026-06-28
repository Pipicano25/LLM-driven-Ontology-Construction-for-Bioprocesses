## 1. Identificación de la pregunta

- **ID:** ALC-03
- **Nivel metodológico:** Conceptual-comparativo y de extracción de evidencia técnica.
- **Tema:** Diferenciación ontológica de sistemas de bioproceso multiescala.
- **Pregunta:** ¿Cómo se diferencian conceptualmente BioLector XT, Sartorius 5 L y Sartorius 10 L como sistemas de bioproceso?

**Cautela de alcance:** “Sartorius 5 L” y “Sartorius 10 L” no aparecen en las fuentes como nombres únicos de producto. En el corpus se documentan como configuraciones potenciales de un sistema `Biostat B` con recipientes `Univessel Glass` de 5 L y 10 L. Por tanto, esas etiquetas se tratarán como candidatos ontológicos, no como identificadores definitivos de equipos físicos. ([Sartorius][1])

## 2. Propósito de la pregunta

La pregunta busca distinguir tres niveles de representación: un sistema de microbioreactor orientado a cribado paralelo (`BioLector XT`), un sistema de biorreactor de sobremesa con recipiente de capacidad máxima de 5 L y una configuración equivalente de 10 L. Esta diferenciación evita modelar erróneamente el volumen como si fuera un equipo autónomo, cuando puede ser una propiedad de un recipiente, una configuración de controlador o una instancia física concreta.

La respuesta aporta clases, propiedades y triadas candidatas para representar escala, formato de cultivo, tipo de recipiente, paralelización, monitoreo y volumen de trabajo.

## 3. Plan de búsqueda documental

**Información técnica requerida**

- Identidad exacta del fabricante, línea, controlador y recipiente.
- Formato de cultivo, mezcla, aireación y control.
- Volumen nominal, volumen mínimo y máximo de trabajo.
- Sensores, variables monitoreadas y actuadores.
- Capacidad de paralelización.
- Modos de proceso: batch, fed-batch, continuo o perfusión.
- Evidencia de relación entre escalas.

**Tipos de documentos necesarios**

- Fichas técnicas y manuales oficiales.
- Brochures de fabricante.
- Procedimientos operativos y configuraciones de equipo.
- Artículos científicos revisados por pares.
- Registros internos del laboratorio: inventario, SOP, hojas de configuración y calibración.

**Repositorios y sitios sugeridos**

- Sitios oficiales de Beckman Coulter Life Sciences y Sartorius.
- PubMed, PMC, Crossref, Scopus, Web of Science y Google Scholar.
- Repositorios institucionales para protocolos o tesis verificables.

**Términos de búsqueda**

- Español: `"BioLector XT microbioreactor ficha técnica"`, `"Sartorius Biostat B 5 L 10 L"`, `"Univessel Glass 5 L 10 L"`, `"escalado microbioreactor biorreactor tanque agitado"`.
- Inglés: `"BioLector XT technical data sheet"`, `"BioLector XT microfluidics"`, `"Biostat B 5 L 10 L"`, `"Univessel Glass working volume"`, `"microtiter plate stirred tank scale-up"`.

**Ecuaciones sugeridas**

```text
"BioLector XT" AND (technical data OR manual OR microbioreactor)

"Biostat B" AND ("5 L" OR "10 L") AND "Univessel Glass"

"Univessel Glass" AND ("maximum working volume" OR "minimum working volume")

("BioLector XT" OR BioLector) AND ("stirred tank" OR fermenter) AND scale-up
```

**Criterios aplicados**

- Incluir documentación oficial o artículos revisados por pares con evidencia localizable.
- Excluir o dejar inciertos documentos de generaciones de equipo no confirmadas.
- No asumir que el volumen identifica por sí solo una línea de producto Sartorius.

## 4. Documentos candidatos encontrados

| ID documento | Título                                                                                               | Entidad autora                           |         Año | Tipo de fuente              | URL/DOI verificable                               | Relación con la pregunta                                                                                         | Decisión preliminar |
| ------------ | ---------------------------------------------------------------------------------------------------- | ---------------------------------------- | ----------: | --------------------------- | ------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------- | ------------------- |
| D1           | _BioLector XT Technical Data Sheet_                                                                  | Beckman Coulter Life Sciences            | No indicado | Ficha técnica oficial       | Página oficial verificable. ([beckman.com][2])    | Especificaciones, control y monitoreo del BioLector XT.                                                          | Include             |
| D2           | _Using the BioLector XT Microbioreactor Gassing Lid_                                                 | Beckman Coulter Life Sciences / m2p-labs | No indicado | Nota técnica oficial        | PDF oficial verificable. ([media.beckman.com][3]) | Define cribado de alto rendimiento, MTP, paralelización y microfluídica.                                         | Include             |
| D3           | _Biostat B – Benchtop Bioreactor Controller_                                                         | Sartorius                                | No indicado | Página oficial de producto  | Página oficial verificable. ([Sartorius][1])      | Relaciona `Biostat B` con recipientes agitados de 5 L y 10 L.                                                    | Include             |
| D4           | _Univessel Glass: Reliability and Continuity_                                                        | Sartorius                                | No indicado | Brochure técnico oficial    | PDF oficial verificable. ([Sartorius][4])         | Define recipientes `Univessel Glass` de 5 L y 10 L y sus rangos de trabajo.                                      | Include             |
| D5           | _Optimizing Yeast Surface-Displayed Unspecific Peroxygenase Production for Sustainable Biocatalysis_ | Teetz, Zuhse y Holtmann                  |        2025 | Artículo revisado por pares | DOI: 10.3390/bioengineering12080822. ([MDPI][5])  | Caso experimental con BioLector XT de 1–2 mL y Biostat B5 de 5 L.                                                | Include             |
| D6           | _Scale-up from microtiter plate to laboratory fermenter_                                             | Kensy, Engelbrecht y Büchs               |        2009 | Artículo revisado por pares | DOI: 10.1186/1475-2859-8-68. ([PubMed][6])        | Evidencia histórica de escalado desde microplaca hacia tanque agitado.                                           | Include             |
| D7           | _Biostat B-DCU Brochure_                                                                             | Sartorius                                | No indicado | Brochure técnico oficial    | PDF oficial verificable. ([Sartorius][7])         | Describe una generación específica de Biostat B-DCU, pero no se confirmó que corresponda al equipo del proyecto. | Uncertain           |
| D8           | _Univessel SU – Stirred Tank Single-Use Bioreactor_                                                  | Sartorius                                | No indicado | Página oficial de producto  | Página oficial verificable. ([Sartorius][8])      | Evidencia de que “10 L Sartorius” puede referirse también a una opción single-use distinta.                      | Uncertain           |

## 5. Evaluación de documentos candidatos

| ID documento | Relevancia | Autoridad | Trazabilidad | Cobertura de la pregunta | Evidencia localizable | Justificación                                                                                       |
| ------------ | ---------- | --------- | ------------ | ------------------------ | --------------------- | --------------------------------------------------------------------------------------------------- |
| D1           | Alta       | Alta      | Alta         | Alta                     | Alta                  | Especifica funciones de control, condiciones de cultivo y medición del BioLector XT.                |
| D2           | Alta       | Alta      | Alta         | Alta                     | Alta                  | Documenta MTP, hasta 48 experimentos simultáneos y funciones microfluídicas.                        |
| D3           | Alta       | Alta      | Alta         | Alta                     | Alta                  | Identifica `Biostat B` como controlador de sobremesa y vincula recipientes de 5 L y 10 L.           |
| D4           | Alta       | Alta      | Alta         | Alta                     | Alta                  | Aporta rangos mínimo y máximo de volumen de trabajo para 5 L y 10 L.                                |
| D5           | Alta       | Alta      | Alta         | Media                    | Alta                  | Caso experimental reciente que utiliza BioLector XT y Biostat B5.                                   |
| D6           | Media      | Alta      | Alta         | Media                    | Alta                  | Fuente histórica útil para escala, pero no describe específicamente BioLector XT ni Sartorius 10 L. |
| D7           | Media      | Alta      | Alta         | Media                    | Alta                  | Puede ser una generación distinta; no debe asumirse como configuración instalada.                   |
| D8           | Media      | Alta      | Alta         | Baja                     | Alta                  | Demuestra ambigüedad de la etiqueta “10 L Sartorius”; no cubre un par 5 L/10 L equivalente.         |

## 6. Corpus documental seleccionado

| ID documento | Documento seleccionado                             | Pregunta asociada | Fragmentos o páginas relevantes                                                                                              | Estado                    |
| ------------ | -------------------------------------------------- | ----------------- | ---------------------------------------------------------------------------------------------------------------------------- | ------------------------- |
| D1           | BioLector XT Technical Data Sheet                  | ALC-03            | Secciones “Cultivation conditions” y “Microfluidic features”. ([beckman.com][2])                                             | Incluido                  |
| D2           | Using the BioLector XT Microbioreactor Gassing Lid | ALC-03            | PDF, p. 1–2: cribado de alto rendimiento, MTP de 32/48 pozos, hasta 48 experimentos, microfluídica. ([media.beckman.com][3]) | Incluido                  |
| D3           | Biostat B – Benchtop Bioreactor Controller         | ALC-03            | Secciones “Top Features”, “Proven Cultivation Vessels”, “Automatic Feed Control” y “Automatic DO Control”. ([Sartorius][1])  | Incluido                  |
| D4           | Univessel Glass: Reliability and Continuity        | ALC-03            | PDF, portada y tabla “Inside Dimensions”: 5 L y 10 L, máximo y mínimo volumen de trabajo. ([Sartorius][4])                   | Incluido                  |
| D5           | Teetz et al., 2025                                 | ALC-03            | Resumen, sección 2.2 y sección 3.3: BioLector XT de 1–2 mL y Biostat B5 de 5 L. ([MDPI][5])                                  | Incluido                  |
| D6           | Kensy et al., 2009                                 | ALC-03            | Resumen: microplaca de 200 µL frente a fermentador de tanque agitado de 1.4 L. ([PubMed][6])                                 | Incluido como antecedente |

El corpus es suficiente para una diferenciación conceptual preliminar, pero es parcial para identificar con certeza los equipos Sartorius físicos presentes en el laboratorio.

## 7. Respuesta basada en evidencia

### Evidencia explícita

`BioLector XT` es un microbioreactor de sobremesa orientado al cribado de cultivos microbianos de alto rendimiento. Opera con placas de microtitulación de formato SBS/SLAS de 32 o 48 pozos y puede ejecutar hasta 48 experimentos simultáneos. Monitorea en línea biomasa, pH, oxígeno disuelto y fluorescencia.

En cambio, `Biostat B` es documentado por Sartorius como un controlador universal de sobremesa para sistemas agitados y de movimiento oscilante. Puede utilizar recipientes `Univessel Glass` convencionales de tanque agitado, incluidos modelos de 5 L y 10 L. ([Sartorius][1])

Para la configuración `Univessel Glass`, el recipiente de 5 L tiene volumen máximo de trabajo de 5 L y mínimo de 0.6 L; el recipiente de 10 L tiene volumen máximo de trabajo de 10 L y mínimo de 1.5 L.

El controlador Biostat B puede configurarse para procesos batch, fed-batch, continuo o de perfusión, además de control de oxígeno disuelto mediante ajuste de agitación y flujos de gas. ([Sartorius][1])

### Inferencia razonable basada en evidencia

Conceptualmente, `BioLector XT` representa un sistema de microescala y alta paralelización para cribado, caracterización de cepas, optimización de medios y exploración de condiciones.

Las configuraciones Sartorius de 5 L y 10 L representan sistemas de cultivo en tanque agitado de escala de laboratorio, con menor paralelización pero mayor capacidad de volumen por recipiente y mayor cercanía estructural a un proceso de biorreactor convencional.

La diferencia primaria entre Sartorius 5 L y Sartorius 10 L no es de categoría tecnológica sino de capacidad y geometría del recipiente. Ambos pueden pertenecer a una misma arquitectura `Biostat B + Univessel Glass`, aunque deben modelarse como configuraciones diferentes por sus rangos de volumen y características físicas. ([Sartorius][4])

Un estudio reciente utilizó BioLector XT a escala de 1–2 mL para cribado y un Biostat B5 de 5 L para producción a mayor escala de laboratorio, lo que respalda una relación metodológica de progresión de escala, no una equivalencia automática entre ambos sistemas. ([MDPI][5])

### Información no establecida en el corpus

- No se confirmó el modelo exacto de los equipos Sartorius instalados.
- No se confirmó si los sistemas de 5 L y 10 L son `Biostat B`, `Biostat B-DCU`, otra línea Sartorius o sistemas single-use.
- No existe evidencia de equivalencia funcional automática entre BioLector XT, 5 L y 10 L.
- No se establecieron parámetros universales de escalado, como `kLa`, potencia por volumen, velocidad de punta o tiempo de mezcla.
- No se documentó la configuración específica de sensores, bombas, gases, placas o consumibles del laboratorio.

## 8. Tabla de afirmaciones y evidencia

| ID evidencia | Afirmación                                                                             | Tipo de evidencia | Documento                   | Página/sección               | Fragmento o resumen fiel                                                                                  | Confianza | Validación experta |
| ------------ | -------------------------------------------------------------------------------------- | ----------------- | --------------------------- | ---------------------------- | --------------------------------------------------------------------------------------------------------- | --------- | ------------------ |
| EV-01        | BioLector XT es un microbioreactor para cribado de alto rendimiento.                   | Explícita         | D2 ([media.beckman.com][3]) | PDF, p. 1                    | Se describe como dispositivo de sobremesa para cribado de cultivos microbianos de alto rendimiento.       | Alta      | No                 |
| EV-02        | BioLector XT monitorea biomasa, pH, DO y fluorescencia.                                | Explícita         | D2 ([media.beckman.com][3]) | PDF, p. 1                    | El documento enumera biomasa, pH, oxígeno disuelto y fluorescencia como parámetros monitoreados en línea. | Alta      | No                 |
| EV-03        | BioLector XT utiliza MTP de 32 o 48 pozos y permite hasta 48 experimentos simultáneos. | Explícita         | D2 ([media.beckman.com][3]) | PDF, p. 1                    | Se indican placas MTP de 32 o 48 pozos y hasta 48 experimentos por corrida.                               | Alta      | No                 |
| EV-04        | BioLector XT dispone de control microfluídico de pH y alimentación.                    | Explícita         | D1 ([beckman.com][2])       | “Microfluidic features”      | Se describen control de pH, líneas de alimentación y perfiles de alimentación.                            | Alta      | No                 |
| EV-05        | Biostat B es un controlador de sobremesa para sistemas agitados y rocking.             | Explícita         | D3 ([Sartorius][1])         | “Top Features”               | Sartorius lo describe como controlador universal para sistemas agitados y de movimiento oscilante.        | Alta      | No                 |
| EV-06        | Biostat B puede asociarse con Univessel Glass de 5 L y 10 L.                           | Explícita         | D3 ([Sartorius][1])         | “Proven Cultivation Vessels” | Se listan recipientes de vidrio autoclavable de 1 L, 2 L, 5 L y 10 L.                                     | Alta      | No                 |
| EV-07        | Univessel Glass 5 L tiene rango de trabajo de 0.6 a 5 L.                               | Explícita         | D4                          | Tabla “Inside Dimensions”    | La tabla reporta mínimo 0.6 L y máximo 5 L.                                                               | Alta      | No                 |
| EV-08        | Univessel Glass 10 L tiene rango de trabajo de 1.5 a 10 L.                             | Explícita         | D4                          | Tabla “Inside Dimensions”    | La tabla reporta mínimo 1.5 L y máximo 10 L.                                                              | Alta      | No                 |
| EV-09        | BioLector XT puede servir como etapa de cribado antes de un Biostat B5 de 5 L.         | Inferida          | D5 ([MDPI][5])              | Resumen; secciones 2.2 y 3.3 | El estudio usa BioLector XT de 1–2 mL para cribado y Biostat B5 de 5 L para producción de laboratorio.    | Media     | Sí                 |
| EV-10        | BioLector XT, Sartorius 5 L y Sartorius 10 L son funcionalmente equivalentes.          | No establecida    | D1–D6                       | Corpus completo              | Ningún documento demuestra equivalencia automática entre estas configuraciones.                           | Baja      | Sí                 |
| EV-11        | El modelo Sartorius de 5 L y 10 L del laboratorio es Biostat B.                        | No establecida    | D3–D8                       | Corpus completo              | La documentación soporta configuraciones posibles, pero no identifica los activos físicos del proyecto.   | Baja      | Sí                 |

## 9. Conceptos ontológicos candidatos

| Concepto candidato             | Tipo sugerido                      | Definición basada en evidencia                                                       | Fuente asociada                 | Estado    |
| ------------------------------ | ---------------------------------- | ------------------------------------------------------------------------------------ | ------------------------------- | --------- |
| `BioprocessSystem`             | Clase                              | Sistema físico o lógico destinado a ejecutar y controlar un proceso de cultivo.      | D1–D4                           | Candidato |
| `MicrobioreactorSystem`        | Subclase                           | Sistema de microescala que utiliza microplacas y permite cultivos paralelos.         | D1, D2 ([media.beckman.com][3]) | Candidato |
| `BenchtopBioreactorSystem`     | Subclase                           | Sistema de biorreactor de sobremesa con control de proceso y recipiente de cultivo.  | D3 ([Sartorius][1])             | Candidato |
| `BenchtopBioreactorController` | Clase                              | Controlador que regula aireación, bombas, temperatura y otras funciones del sistema. | D3 ([Sartorius][1])             | Candidato |
| `CultureVessel`                | Clase                              | Recipiente físico donde ocurre el cultivo.                                           | D3, D4                          | Candidato |
| `MicrotiterPlate`              | Clase                              | Placa de microtitulación usada como formato de cultivo paralelo.                     | D2 ([media.beckman.com][3])     | Candidato |
| `CultivationWell`              | Clase                              | Compartimento individual de cultivo dentro de una microplaca.                        | D2                              | Candidato |
| `BioLectorXT`                  | Individuo de modelo de equipo      | Modelo de microbioreactor de Beckman Coulter para cribado y monitoreo en línea.      | D1, D2                          | Candidato |
| `BiostatB`                     | Individuo de modelo de controlador | Modelo de controlador Sartorius para sistemas agitados y rocking.                    | D3                              | Candidato |
| `UnivesselGlass5LModel`        | Individuo de modelo de recipiente  | Configuración Univessel Glass con volumen máximo de trabajo de 5 L.                  | D4                              | Candidato |
| `UnivesselGlass10LModel`       | Individuo de modelo de recipiente  | Configuración Univessel Glass con volumen máximo de trabajo de 10 L.                 | D4                              | Candidato |
| `OnlineMonitoredParameter`     | Concepto auxiliar                  | Variable medida durante el cultivo, como biomasa, pH, DO o fluorescencia.            | D1, D2                          | Candidato |
| `CultivationMode`              | Clase                              | Modalidad operativa como batch, fed-batch, continuo o perfusión.                     | D3                              | Candidato |
| `hasMaximumWorkingVolumeL`     | Propiedad de dato                  | Relaciona un modelo de recipiente con su volumen máximo de trabajo en litros.        | D4                              | Candidato |
| `hasMinimumWorkingVolumeL`     | Propiedad de dato                  | Relaciona un modelo de recipiente con su volumen mínimo de trabajo en litros.        | D4                              | Candidato |

## 10. Relaciones ontológicas candidatas

| Relación candidata            | Dominio sugerido           | Rango sugerido                 | Significado                                                              | Evidencia asociada | Estado                      |
| ----------------------------- | -------------------------- | ------------------------------ | ------------------------------------------------------------------------ | ------------------ | --------------------------- |
| `usesCultivationFormat`       | `MicrobioreactorSystem`    | `MicrotiterPlate`              | Indica el formato físico de cultivo usado.                               | D2                 | Candidata                   |
| `hasCultivationWell`          | `MicrotiterPlate`          | `CultivationWell`              | Indica que una placa contiene pozos de cultivo.                          | D2                 | Candidata                   |
| `monitorsParameter`           | `BioprocessSystem`         | `OnlineMonitoredParameter`     | Indica una variable monitoreada durante el cultivo.                      | D1, D2             | Candidata                   |
| `supportsMicrofluidicControl` | `MicrobioreactorSystem`    | `ControlFunction`              | Indica control microfluídico de pH o alimentación.                       | D1                 | Candidata                   |
| `usesCultivationVessel`       | `BenchtopBioreactorSystem` | `CultureVessel`                | Vincula un sistema controlado con su recipiente.                         | D3, D4             | Candidata                   |
| `hasMaximumWorkingVolumeL`    | `CultureVessel`            | `xsd:decimal`                  | Define volumen máximo de trabajo expresado en litros.                    | D4                 | Candidata                   |
| `hasMinimumWorkingVolumeL`    | `CultureVessel`            | `xsd:decimal`                  | Define volumen mínimo de trabajo expresado en litros.                    | D4                 | Candidata                   |
| `supportsProcessMode`         | `BenchtopBioreactorSystem` | `CultivationMode`              | Indica modos de operación soportados.                                    | D3                 | Candidata                   |
| `isControlledBy`              | `BenchtopBioreactorSystem` | `BenchtopBioreactorController` | Relaciona el sistema con su controlador.                                 | D3                 | Requiere validación experta |
| `precedesInScale`             | `BioprocessSystem`         | `BioprocessSystem`             | Indica una progresión experimental desde cribado hacia una escala mayor. | D5, D6             | Requiere validación experta |

## 11. Triadas RDF candidatas

| Triada RDF candidata                                                                    | Documento de soporte | Página o sección             | Estado                      |
| --------------------------------------------------------------------------------------- | -------------------- | ---------------------------- | --------------------------- |
| `BioLectorXT -> rdf:type -> MicrobioreactorSystem`                                      | D1, D2               | Ficha técnica; PDF p. 1      | Soportada                   |
| `BioLectorXT -> usesCultivationFormat -> MicrotiterPlate`                               | D2                   | PDF p. 1                     | Soportada                   |
| `BioLectorXT -> hasMaximumParallelCultivationCount -> "48"`                             | D2                   | PDF p. 1                     | Soportada                   |
| `BioLectorXT -> monitorsParameter -> Biomass`                                           | D2                   | PDF p. 1                     | Soportada                   |
| `BioLectorXT -> monitorsParameter -> pH`                                                | D2                   | PDF p. 1                     | Soportada                   |
| `BioLectorXT -> monitorsParameter -> DissolvedOxygen`                                   | D2                   | PDF p. 1                     | Soportada                   |
| `BioLectorXT -> monitorsParameter -> Fluorescence`                                      | D2                   | PDF p. 1                     | Soportada                   |
| `BioLectorXT -> supportsMicrofluidicControl -> TriggeredPHControl`                      | D1                   | “Microfluidic features”      | Soportada                   |
| `BioLectorXT -> supportsMicrofluidicControl -> FeedingControl`                          | D1                   | “Microfluidic features”      | Soportada                   |
| `BiostatB -> rdf:type -> BenchtopBioreactorController`                                  | D3                   | “Top Features”               | Soportada                   |
| `BiostatB -> supportsMotionSystem -> ConventionalStirredTankSystem`                     | D3                   | “Top Features”               | Soportada                   |
| `BiostatB -> usesCultivationVessel -> UnivesselGlass5LModel`                            | D3, D4               | “Proven Cultivation Vessels” | Soportada                   |
| `BiostatB -> usesCultivationVessel -> UnivesselGlass10LModel`                           | D3, D4               | “Proven Cultivation Vessels” | Soportada                   |
| `UnivesselGlass5LModel -> hasMaximumWorkingVolumeL -> "5.0"`                            | D4                   | Tabla “Inside Dimensions”    | Soportada                   |
| `UnivesselGlass5LModel -> hasMinimumWorkingVolumeL -> "0.6"`                            | D4                   | Tabla “Inside Dimensions”    | Soportada                   |
| `UnivesselGlass10LModel -> hasMaximumWorkingVolumeL -> "10.0"`                          | D4                   | Tabla “Inside Dimensions”    | Soportada                   |
| `UnivesselGlass10LModel -> hasMinimumWorkingVolumeL -> "1.5"`                           | D4                   | Tabla “Inside Dimensions”    | Soportada                   |
| `BiostatB -> supportsProcessMode -> BatchCultivation`                                   | D3                   | “Automatic Feed Control”     | Soportada                   |
| `BiostatB -> supportsProcessMode -> FedBatchCultivation`                                | D3                   | “Automatic Feed Control”     | Soportada                   |
| `BiostatB -> supportsProcessMode -> ContinuousCultivation`                              | D3                   | “Automatic Feed Control”     | Soportada                   |
| `BiostatB -> supportsProcessMode -> PerfusionCultivation`                               | D3                   | “Automatic Feed Control”     | Soportada                   |
| `BioLectorXT -> precedesInScale -> BiostatB5LConfiguredSystem`                          | D5                   | Resumen; secciones 2.2 y 3.3 | Parcialmente soportada      |
| `UnivesselGlass5LModel -> hasSmallerMaximumWorkingVolumeThan -> UnivesselGlass10LModel` | D4                   | Tabla “Inside Dimensions”    | Requiere validación experta |

## 12. Sinónimos y variantes terminológicas

| Término principal        | Sinónimos o variantes documentadas                                                  | Idioma | Documento de soporte |
| ------------------------ | ----------------------------------------------------------------------------------- | ------ | -------------------- |
| `BioLector XT`           | BioLector XT microbioreactor; BioLector XT®; parallelized microfermentation reactor | Inglés | D1, D2, D5           |
| `MicrotiterPlate`        | MTP; SBS/SLAS standard format microtiter plate                                      | Inglés | D2                   |
| `DissolvedOxygen`        | DO; dissolved oxygen                                                                | Inglés | D1, D2               |
| `Biostat B`              | Biostat® B; universal benchtop controller                                           | Inglés | D3                   |
| `Univessel Glass`        | Univessel® Glass; autoclavable cultivation vessel                                   | Inglés | D3, D4               |
| `UnivesselGlass5LModel`  | Univessel Glass 5 L; 5 L working volume                                             | Inglés | D4                   |
| `UnivesselGlass10LModel` | Univessel Glass 10 L; 10 L working volume                                           | Inglés | D4                   |
| `Biostat B5`             | 5 L bioreactor; Biostat B5                                                          | Inglés | D5                   |

## 13. Vacíos, riesgos y decisiones pendientes

- Debe confirmarse el modelo exacto de Sartorius instalado en el laboratorio.
- Debe verificarse si 5 L y 10 L son recipientes `Univessel Glass`, sistemas single-use o otra línea Sartorius.
- La equivalencia entre escalas no puede modelarse como automática.
- Los valores de volumen máximo no deben confundirse con volumen operativo real de cada lote.
- Las capacidades de sensores, gases, bombas y control dependen de la configuración adquirida.
- Debe obtenerse el manual del equipo físico, configuración de controladores, lista de sensores y SOP de operación.
- Debe definirse un patrón formal para cantidades y unidades, idealmente con QUDT u OM.
- La relación `precedesInScale` requiere criterios expertos: `kLa`, potencia por volumen, tiempo de mezcla, velocidad de punta, estrategia de aireación y calidad de datos.
- El artículo D6 es útil como antecedente de escalado, pero no debe utilizarse para asignar especificaciones del BioLector XT actual.

## 14. Registro metodológico para el documento de investigación

Texto para incorporar y revisar:

La pregunta ALC-03 examinó las diferencias conceptuales entre el BioLector XT y configuraciones Sartorius de 5 L y 10 L dentro de un marco de sistemas de bioproceso multiescala. La estrategia documental priorizó fichas técnicas y notas oficiales de fabricante, complementadas con artículos científicos revisados por pares sobre uso y transición de escala entre microbioreactores y biorreactores de tanque agitado. Los criterios de selección exigieron trazabilidad, entidad autora verificable y evidencia localizable sobre formato de cultivo, volumen de trabajo, monitoreo, control y modos operativos. El corpus permitió identificar al BioLector XT como un sistema de microbioreactor de alta paralelización basado en microplacas, y a las configuraciones Sartorius de 5 L y 10 L como posibles combinaciones de un controlador Biostat B con recipientes Univessel Glass de distinta capacidad máxima de trabajo. Se propusieron clases, propiedades y triadas RDF preliminares para representar sistemas, recipientes, escalas, variables monitoreadas y modos de cultivo. La principal limitación es la ausencia de documentación que confirme el modelo y la configuración exacta de los equipos Sartorius disponibles en el laboratorio, por lo que las relaciones de equivalencia funcional y progresión de escala requieren validación experta.

## 15. Estado final

- **Nivel de confianza general:** Medio.
- **Estado de la respuesta:** Parcialmente soportada.
- **Estado del corpus:** Parcial.
- **Próxima acción recomendada:** Obtener el modelo, número de serie, manual, hoja de configuración y SOP de los equipos Sartorius de 5 L y 10 L antes de convertir las triadas candidatas en axiomas ontológicos definitivos.

[1]: https://www.sartorius.com/en/products/fermentation-bioreactors/benchtop-bioreactors/biostat-b " Biostat® B - Benchtop Bioreactor Controller | Sartorius"
[2]: https://www.beckman.com/resources/reading-material/product-instructions/biolector-xt-technical-data-sheet "BioLector XT Technical Data Sheet"
[3]: https://media.beckman.com/-/media/m2p-labs/pdfs/using-the-biolector-xt-microbioreactor-gassing-lid.pdf?rev=87161a7aedf9471bb01702126a63302a&utm_source=chatgpt.com "https://media.beckman.com/-/media/m2p-labs/pdfs/using-the-biolector-xt-microbioreactor-gassing-lid.pdf?rev=87161a7aedf9471bb01702126a63302a"
[4]: https://www.sartorius.com/download/10336/broch-univesselglass-sbi1554-e-data.pdf "Univessel Glass Reliability and Continuity"
[5]: https://www.mdpi.com/2306-5354/12/8/822 "Optimizing Yeast Surface-Displayed Unspecific Peroxygenase Production for Sustainable Biocatalysis | MDPI"
[6]: https://pubmed.ncbi.nlm.nih.gov/20028556/ "Scale-up from microtiter plate to laboratory fermenter: evaluation by online monitoring techniques of growth and protein expression in Escherichia coli and Hansenula polymorpha fermentations - PubMed"
[7]: https://www.sartorius.com/download/12080/broch-biostat-b-dcu-sbi1555-e-data.pdf "Biostat B-DCU, Brochure"
[8]: https://www.sartorius.com/en/products/fermentation-bioreactors/benchtop-bioreactors/univessel-su?utm_source=chatgpt.com "Univessel® SU - Stirred Tank Single-Use Bioreactor"
