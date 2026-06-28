# ALC-08: Conceptos fuera del alcance inicial de la ontología

## 1. Identificación de la pregunta

- **ID:** ALC-08
- **Nivel metodológico:** Delimitación de alcance (scoping) — pregunta de diseño ontológico, no de caracterización técnica de equipos.
- **Tema:** Definición de límites del dominio ontológico para BioLector XT, Sartorius 5 L y Sartorius 10 L.
- **Pregunta:** ¿Qué conceptos deben quedar fuera del alcance inicial para evitar que la ontología sea demasiado amplia?

## 2. Propósito de la pregunta

Esta pregunta no busca evidencia técnica sobre los equipos, sino **delimitar el dominio de modelado** antes de construir clases y relaciones. Su función en el proyecto es evitar el "scope creep" ontológico: incluir conceptos periféricos (regulatorios, comerciales, de otras escalas de proceso, de disciplinas no relacionadas) que inflarían la ontología sin aportar valor a la representación de equipos, variables operativas, sensores, fases de proceso y equivalencias entre escalas. El resultado de esta pregunta no es evidencia empírica sino una **decisión de diseño informada por la evidencia documental disponible** sobre qué cubren realmente los sistemas BioLector XT y Sartorius BIOSTAT B 5 L/10 L.

**Aclaración importante:** dado que es una pregunta de alcance/diseño, no de caracterización técnica, la mayor parte de la respuesta es **inferencia razonable y juicio metodológico**, no extracción literal de un documento que enuncie "exclusiones". Ningún manual o ficha técnica revisada declara explícitamente qué debe excluirse de una ontología; esa es una decisión del investigador. Esto se marca explícitamente en las secciones siguientes.

## 3. Plan de búsqueda documental

**Información técnica requerida:**

- Alcance funcional declarado de BioLector XT (qué mide, qué controla, qué no controla).
- Alcance funcional declarado de Sartorius BIOSTAT B 5 L/10 L.
- Volúmenes de trabajo, sensores y variables soportadas por cada sistema (para distinguir lo que es propio del equipo de lo que pertenece a otras capas, p. ej. bioquímica metabólica, regulación GMP, costos).

**Tipos de documentos necesarios:** fichas técnicas de fabricante, manuales de operación, notas de aplicación, comparativas de literatura científica sobre equivalencia de escalas (scale-down/scale-up).

**Repositorios sugeridos:** sitios oficiales beckman.com (BioLector XT) y sartorius.com (BIOSTAT B), ManualsLib/Manualzz (copias de manuales), PubMed/Scopus para artículos de equivalencia de escalas, repositorios institucionales (p. ej. A\*STAR ASEF).

**Términos de búsqueda:** "BioLector XT specifications", "BIOSTAT B operating manual", "scale-down bioreactor equivalence", "microbioreactor vs bench-scale bioreactor scope", "bioprocess ontology scope", "ontología alcance bioprocesos".

**Ecuaciones de búsqueda sugeridas:** `("BioLector XT" OR "BIOSTAT B") AND (specification OR manual OR "technical data sheet")`; `("scale-down" OR "scale equivalence") AND bioreactor AND (microbioreactor OR "5 L" OR "10 L")`.

**Criterios de inclusión/exclusión:** los generales del prompt maestro (documentos verificables, con autoría y trazabilidad, relacionados directamente con los tres sistemas).

## 4. Documentos candidatos encontrados

| ID documento | Título                                                         | Entidad autora                                 | Año                               | Tipo de fuente                                         | URL/DOI verificable                                                                                                        | Relación con la pregunta                                                           | Decisión preliminar |
| ------------ | -------------------------------------------------------------- | ---------------------------------------------- | --------------------------------- | ------------------------------------------------------ | -------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ------------------- |
| D1           | BioLector XT Technical Data Sheet                              | Beckman Coulter                                | s.f. (vigente)                    | Ficha técnica fabricante                               | https://www.beckman.com/resources/reading-material/product-instructions/biolector-xt-technical-data-sheet                  | Delimita qué mide/controla el BioLector XT                                         | Include             |
| D2           | BioLector XT — página de producto y módulos                    | Beckman Coulter                                | s.f. (vigente, © 2026)            | Página oficial fabricante                              | https://www.beckman.com/microbioreactor/biolector-xt ; https://www.beckman.com/microbioreactor/biolector-xt/modules        | Define alcance funcional (biomasa, pH, DO, fluorescencia; agitación y temperatura) | Include             |
| D3           | BioLector XT Safety Notices (manual)                           | Beckman Coulter                                | 2021 (fecha de página vista)      | Manual técnico oficial                                 | https://www.manualslib.com/manual/2169370/Beckman-Coulter-Biolector-Xt.html                                                | Especificaciones de instrumento, riesgos, límites operativos                       | Include             |
| D4           | Using the BioLector XT Microbioreactor Gassing Lid             | Beckman Coulter                                | s.f.                              | Nota técnica/instructivo oficial                       | https://www.beckman.com/resources/reading-material/product-instructions/using-the-biolector-xt-microbioreactor-gassing-lid | Detalla módulos de gasificación, modos disponibles                                 | Include             |
| D5           | BIOSTAT B 2nd Gen — Operating Manual                           | Sartorius Stedim Biotech                       | manual vigente (copia vista 2025) | Manual técnico oficial                                 | https://studylib.net/doc/27751717/sartorius-biostat-b-2nd-gen-user-manual                                                  | Define alcance del sistema, recipientes, módulos                                   | Include             |
| D6           | Biostat B-DCU — folleto técnico                                | Sartorius                                      | s.f.                              | Ficha/folleto fabricante                               | https://www.sartorius.com/download/12080/broch-biostat-b-dcu-sbi1555-e-data.pdf                                            | Alcance funcional y de control                                                     | Include             |
| D7           | Sartorius Stedim Biotech BIOSTAT B Operating Manual (completo) | Sartorius Stedim Biotech                       | Vers. 05/2014 (impresión 2023)    | Manual técnico oficial                                 | https://www.manualslib.com/manual/3343908/Sartorius-Stedim-Biotech-Biostat-B.html                                          | Especificaciones de setup, gases, sensores, mantenimiento                          | Include             |
| D8           | Bioreactor: Sartorius 10 (w/MFCS) — BIOSTAT B                  | A\*STAR Scientific Equipment & Services Finder | s.f.                              | Ficha institucional de equipo                          | https://asef.a-star.edu.sg/equipment/bioreactor-sartorius-10-w-mfcs-biostat-b-sifbi                                        | Especificaciones de volumen, agitación, sensores para 5L/10L                       | Include             |
| D9           | BIOSTAT B (Bplus) Exclusive Flow — especificaciones            | Richmond Scientific (distribuidor)             | s.f.                              | Ficha comercial sin autoría científica directa         | https://www.richmondscientific.com/.../Sartorius-Stedim-Biostat-Bplus...                                                   | Información comercial complementaria, sin trazabilidad institucional fuerte        | Uncertain           |
| D10          | LabX — listado comercial BIOSTAT B                             | LabX (marketplace)                             | s.f.                              | Contenido comercial no verificable como fuente técnica | https://www.labx.com/product-a/sartorius-biostat-b                                                                         | Texto promocional, sin autoría técnica trazable                                    | Exclude             |

## 5. Evaluación de documentos candidatos

| ID documento | Relevancia | Autoridad | Trazabilidad | Cobertura de la pregunta | Evidencia localizable | Justificación                                                                                                                                              |
| ------------ | ---------- | --------- | ------------ | ------------------------ | --------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------- |
| D1           | Alta       | Alta      | Alta         | Media                    | Sí                    | Define explícitamente qué parámetros mide/controla el equipo, lo que permite inferir qué queda fuera (p. ej. no mide variables metabólicas intracelulares) |
| D2           | Alta       | Alta      | Media        | Media                    | Sí                    | Confirma alcance funcional (biomasa, pH, DO, fluorescencia, agitación, temperatura); no menciona control de variables bioquímicas avanzadas                |
| D3           | Media      | Alta      | Alta         | Baja                     | Sí                    | Cubre riesgos y especificaciones de instrumento, no alcance conceptual                                                                                     |
| D5           | Alta       | Alta      | Alta         | Media                    | Sí                    | Define explícitamente el alcance de validez del manual (qué módulos y recipientes cubre, y por exclusión, qué no)                                          |
| D6           | Media      | Alta      | Media        | Baja                     | Sí                    | Folleto comercial pero de fabricante; complementa alcance funcional                                                                                        |
| D7           | Alta       | Alta      | Alta         | Media                    | Sí                    | Manual completo con alcance de setup, gases, sensores — permite inferir límites del sistema                                                                |
| D8           | Media      | Media     | Media        | Media                    | Sí                    | Ficha institucional con especificaciones concretas de 5L/10L                                                                                               |
| D9           | Baja       | Baja      | Baja         | Baja                     | Parcial               | Fuente comercial de distribuidor, sin autoría técnica primaria                                                                                             |

## 6. Corpus documental seleccionado

| ID documento | Documento seleccionado                  | Pregunta asociada | Fragmentos relevantes                                         | Estado   |
| ------------ | --------------------------------------- | ----------------- | ------------------------------------------------------------- | -------- |
| D1           | BioLector XT Technical Data Sheet       | ALC-08            | Sección de "cultivation conditions" y "microfluidic features" | Incluido |
| D2           | BioLector XT página de producto/módulos | ALC-08            | Descripción de parámetros medidos y módulos opcionales        | Incluido |
| D5           | BIOSTAT B 2nd Gen Operating Manual      | ALC-08            | Sección 1.1 "Validity" (alcance del manual)                   | Incluido |
| D7           | BIOSTAT B Operating Manual completo     | ALC-08            | Capítulos de setup, gases, sensores, mantenimiento            | Incluido |
| D8           | Ficha A\*STAR ASEF Sartorius 10         | ALC-08            | Tabla de especificaciones técnicas                            | Incluido |

## 7. Respuesta basada en evidencia

**Evidencia explícita (de los documentos):** los tres sistemas tienen un alcance funcional bien delimitado por sus propios fabricantes:

- BioLector XT mide y controla en línea biomasa, pH, DO y fluorescencia, además de agitación y temperatura, en placas de 32/48 pocillos, con módulos opcionales de gasificación (anaerobio, CO2, O2) y microfluídica.The BioLector XT microbioreactor measures biomass, pH, DO, and fluorescence online while running a cultivation experiment. The system controls the shaking speed and the temperature inside the cultivation chamber.
- BIOSTAT B (5 L/10 L) controla temperatura, pH, DO, agitación y aporte de gases, con módulos de aireación, bombas peristálticas y diversos recipientes intercambiables.Besides classic DO cascade control, we have developed the unique advanced DO controller that gives you more flexibility to develop and optimize your DO control strategy. El manual operativo declara explícitamente su validez limitada a configuraciones específicas (modelos, recipientes y volúmenes definidos).

**Inferencia razonable (no declarada explícitamente, pero derivada de la evidencia anterior):** dado que la documentación oficial circunscribe el alcance de cada sistema a variables operativas (físico-químicas y de proceso), instrumentación propia y configuración mecánica del equipo, **se infiere razonablemente** que deben quedar **fuera del alcance inicial** de la ontología los siguientes tipos de conceptos:

1. **Biología molecular y genómica de los organismos cultivados** (rutas metabólicas, expresión génica, proteómica) — los equipos no miden ni reportan estos niveles; pertenecen a un dominio ontológico distinto (biología de sistemas).
2. **Aspectos regulatorios y de calidad GMP/GxP, validación farmacéutica formal** — mencionados tangencialmente en fichas comerciales (IVD/ASR) pero no parte del modelo de equipo/proceso/sensor.
3. **Aspectos económicos y comerciales** (precios, proveedores, garantías, marketplace) — presentes en fuentes como D9/D10 pero excluidos por criterio documental (contenido comercial no verificable o irrelevante al modelo técnico).
4. **Otras escalas de biorreactor no contempladas en el proyecto** (p. ej. recipientes de 1 L, 2 L, RM Rocker de bolsa, plantas piloto >10 L) — aunque aparecen en los mismos manuales (D5, D7) como parte de la familia de productos, **no son objeto del proyecto**, que se limita a BioLector XT, Sartorius 5 L y 10 L.
5. **Detalles de mantenimiento, limpieza, instalación eléctrica/de gases y seguridad ocupacional detallada** — documentados extensamente en los manuales (D3, D7) pero pertenecen a procedimientos operativos, no a la estructura conceptual de equipos/variables/fases de proceso que la ontología busca representar.
6. **Software de control específico no estandarizado** (detalles de interfaz de usuario, menús, programación de scripts) — mencionado en D4/D5 pero es implementación, no concepto de dominio.
7. **Aspectos de propiedad intelectual, normativa de marcas y disponibilidad regional** — presentes en pies de página de fichas (D8 menciona "regulatory status") pero ajenos al modelo de bioproceso.

**Información no establecida en el corpus:** ningún documento del corpus declara de forma explícita una lista de "exclusiones ontológicas"; toda la lista anterior es una **propuesta de delimitación de alcance**, no un hallazgo documental directo, y requiere validación por el investigador y posiblemente por un experto en ontologías de bioprocesos.

## 8. Tabla de afirmaciones y evidencia

| ID evidencia | Afirmación                                                                                                      | Tipo de evidencia | Documento                                                          | Página/sección                         | Fragmento o resumen fiel                        | Confianza            | Validación experta                                             |
| ------------ | --------------------------------------------------------------------------------------------------------------- | ----------------- | ------------------------------------------------------------------ | -------------------------------------- | ----------------------------------------------- | -------------------- | -------------------------------------------------------------- |
| E1           | BioLector XT mide biomasa, pH, DO y fluorescencia; controla agitación y temperatura                             | Explícita         | D2/D4                                                              | Página de producto / Modules           | Resumido arriba con cita                        | Alta                 | No requerida                                                   |
| E2           | BIOSTAT B controla DO, pH, temperatura, agitación y gases mediante módulos de aireación                         | Explícita         | D5/D6/D7                                                           | Secciones de control y aeración        | Resumido arriba con cita                        | Alta                 | No requerida                                                   |
| E3           | El manual BIOSTAT B delimita su validez a modelos y recipientes específicos (1L–10L UniVessel, RM Rocker, etc.) | Explícita         | D5                                                                 | Sección 1.1 "Validity"                 | Resumido (no citado textualmente)               | Alta                 | No requerida                                                   |
| E4           | Conceptos de biología molecular/genómica deben excluirse del alcance inicial                                    | Inferida          | — (inferencia metodológica)                                        | —                                      | No hay fragmento; es juicio de diseño           | Media                | Sí, requiere validación del investigador/experto en ontologías |
| E5           | Aspectos regulatorios GMP, comerciales y de otras escalas (1L, 2L, RM) deben excluirse                          | Inferida          | D5/D7 (delimitación de validez) + criterio de exclusión documental | Sección "Validity" y notas comerciales | No hay fragmento textual de exclusión explícita | Media                | Sí                                                             |
| E6           | No existe en el corpus una declaración explícita de "alcance ontológico excluido"                               | No establecida    | —                                                                  | —                                      | —                                               | Alta (como ausencia) | No aplica                                                      |

## 9. Conceptos ontológicos candidatos

| Concepto candidato                                         | Tipo sugerido                             | Definición basada en evidencia                                                                                                            | Fuente asociada                  | Estado              |
| ---------------------------------------------------------- | ----------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------- | ------------------- |
| `OutOfScopeConcept` (clase auxiliar de control de alcance) | Concepto auxiliar                         | Categoría usada para documentar explícitamente, dentro de la ontología o su documentación, qué conceptos fueron deliberadamente excluidos | Inferencia metodológica          | Candidato           |
| `MolecularBiologyDomain`                                   | Concepto auxiliar (marcador de exclusión) | Dominio de rutas metabólicas/genómica, no cubierto por sensores de los equipos                                                            | Inferencia (D1, D2)              | Candidato — excluir |
| `RegulatoryComplianceConcept`                              | Concepto auxiliar (marcador de exclusión) | Aspectos GMP/GxP/IVD mencionados en pies de ficha pero no parte del modelo de proceso                                                     | D8 (mención "regulatory status") | Candidato — excluir |
| `NonTargetVesselScale`                                     | Concepto auxiliar (marcador de exclusión) | Escalas de recipiente (1L, 2L, RM Rocker, >10L) presentes en manuales pero fuera del alcance del proyecto                                 | D5, D7                           | Candidato — excluir |
| `ControlSoftwareUIDetail`                                  | Concepto auxiliar (marcador de exclusión) | Detalles de interfaz/menú del software de control (BioLection, MFCS/DCU)                                                                  | D4, D5                           | Candidato — excluir |

## 10. Relaciones ontológicas candidatas

| Relación candidata        | Dominio sugerido | Rango sugerido                                       | Significado                                                       | Evidencia asociada      | Estado                                 |
| ------------------------- | ---------------- | ---------------------------------------------------- | ----------------------------------------------------------------- | ----------------------- | -------------------------------------- |
| `isOutOfScopeFor`         | Concept          | OntologyProject                                      | Marca que un concepto fue evaluado y excluido del alcance inicial | Inferencia metodológica | Candidato, requiere validación experta |
| `belongsToExcludedDomain` | Concept          | ExcludedDomain (p. ej. MolecularBiology, Regulatory) | Clasifica el motivo de exclusión                                  | Inferencia              | Candidato                              |

## 11. Triadas RDF candidatas

```
MolecularBiologyDomain -> isOutOfScopeFor -> BioprocessOntologyProject
```

Documento de soporte: inferencia basada en D1/D2 (alcance de sensores del BioLector XT). Página/sección: no aplica (no es cita textual). Estado: **requiere validación experta**.

```
NonTargetVesselScale -> belongsToExcludedDomain -> ScaleOutOfProjectScope
```

Documento de soporte: D5, sección "Validity". Estado: **requiere validación experta** (la decisión de excluir otras escalas es del investigador, no del fabricante).

```
RegulatoryComplianceConcept -> isOutOfScopeFor -> BioprocessOntologyProject
```

Documento de soporte: D8 (mención tangencial de "regulatory status"). Estado: **requiere validación experta**.

## 12. Sinónimos y variantes terminológicas

| Término principal    | Sinónimos o variantes documentadas              | Idioma | Documento de soporte                                            |
| -------------------- | ----------------------------------------------- | ------ | --------------------------------------------------------------- |
| Scope delimitation   | Alcance, delimitación de dominio, "scoping"     | ES/EN  | Inferencia metodológica (no hay término exacto en los manuales) |
| Out-of-scope concept | Concepto fuera de alcance, exclusión de dominio | ES/EN  | Inferencia metodológica                                         |

No se encontraron variantes terminológicas explícitas en los documentos del corpus para "alcance ontológico"; este es un concepto de la metodología de construcción ontológica, no del dominio técnico de bioprocesos.

## 13. Vacíos, riesgos y decisiones pendientes

- **Información faltante:** no existe ningún documento (manual, ficha, artículo) que declare explícitamente criterios de exclusión para una ontología de estos sistemas — esto es inherente al hecho de que la pregunta es de diseño, no de caracterización técnica.
- **Ambigüedad terminológica:** el límite entre "variable operativa del equipo" y "variable de proceso biológico" (p. ej., tasa de consumo de oxígeno, OUR) puede ser ambiguo: puede considerarse tanto un dato del sensor como un indicador metabólico.
- **Configuraciones dependientes del equipo:** módulos opcionales (microfluídica, anaerobiosis, CO2) amplían el alcance funcional real del BioLector XT; su inclusión/exclusión depende de si el proyecto cubre esas configuraciones específicas.
- **Datos que requieren validación con expertos:** la lista completa de "exclusiones" presentada aquí debe ser revisada por el equipo de ingeniería ontológica y, preferiblemente, por un experto en bioprocesos para confirmar que no se excluye algo relevante (p. ej., calidad de datos, trazabilidad de muestras, que sí están en el alcance original del proyecto).
- **Documentos adicionales necesarios:** un documento de alcance del proyecto (project charter u ontology requirements specification, ORSD) que el investigador no ha proporcionado todavía, y que sería la fuente primaria ideal para responder ALC-08 de forma definitiva.

## 14. Registro metodológico para el documento de investigación

La pregunta ALC-08 fue analizada con el propósito de delimitar el alcance inicial de la ontología OWL/RDF orientada a representar los sistemas BioLector XT y Sartorius BIOSTAT B (5 L y 10 L). La estrategia de búsqueda se centró en fichas técnicas y manuales oficiales de los fabricantes (Beckman Coulter y Sartorius Stedim Biotech), priorizando fuentes con autoría y trazabilidad verificables, y excluyendo contenido puramente comercial sin valor técnico. Se incorporaron al corpus cinco documentos principales que delimitan explícitamente el alcance funcional y de validez de cada sistema (parámetros medidos, módulos disponibles, recipientes y volúmenes cubiertos). A partir de esta evidencia explícita se derivó, mediante inferencia razonable, una propuesta de conceptos a excluir del alcance inicial: biología molecular/genómica del organismo cultivado, cumplimiento regulatorio GMP/GxP, escalas de recipiente no contempladas en el proyecto (1 L, 2 L, RM Rocker), y detalles de implementación de software de control. Se identificaron conceptos y relaciones ontológicas candidatas para marcar formalmente estas exclusiones (`OutOfScopeConcept`, `isOutOfScopeFor`), todas etiquetadas como candidatas pendientes de validación. Las principales limitaciones son la ausencia de un documento de alcance del proyecto (ORSD) que defina criterios de exclusión de forma autoritativa, y la naturaleza inherentemente metodológica —más que documental— de la pregunta analizada.

## 15. Estado final

- **Nivel de confianza general:** Medio (alto en la evidencia técnica de alcance funcional de los equipos; medio-bajo en las inferencias de exclusión, que son juicio metodológico).
- **Estado de la respuesta:** Parcialmente soportada.
- **Estado del corpus:** Parcial — suficiente para fundamentar el alcance funcional de los equipos, pero insuficiente para una decisión definitiva de exclusión, que depende del documento de alcance del proyecto (no disponible).
- **Próxima acción recomendada:** Solicitar al investigador un documento de especificación de requisitos de la ontología (ORSD) o un acta de alcance del proyecto, y someter la lista de exclusiones propuesta a revisión por un experto en bioprocesos y en ingeniería ontológica antes de fijarla como definitiva.
