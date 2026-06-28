# Paquete de entrada para extracción condicionada por corpus

## Pregunta ALC-05: ¿Cómo se separan ontológicamente el equipo físico, el proceso biológico, el sistema de control, las variables medidas y los datos generados?

---

## Reglas para el modelo receptor

- Trabaja exclusivamente con las fuentes y fragmentos incluidos.
- No uses conocimiento externo.
- Cuando la evidencia sea insuficiente, responde: No establecido en el corpus suministrado.
- Diferencia evidencia explícita e inferencia razonable.
- No conviertas conceptos o triadas en axiomas definitivos.

---

## Corpus de fuentes seleccionadas

---

### [SRC-001]

- **Título:** Semantic Sensor Network Ontology (SSN/SOSA 2017)
- **Entidad autora:** W3C / OGC Spatial Data on the Web Working Group
- **Año:** 2017
- **Tipo de fuente:** Especificación técnica W3C (estándar internacional)
- **URL o DOI:** https://www.w3.org/TR/vocab-ssn/
- **Página, sección o ubicación:** Sección SOSA core; clases Sensor, Observation, ObservableProperty, FeatureOfInterest, Actuator, Platform; sección SSN System
- **Fragmento verificable:**
  > "The following specifications introduce the new Semantic Sensor Network (SSN) and Sensor, Observation, Sample, and Actuator (SOSA) ontologies that are set out to provide flexible but coherent perspectives for representing the entities, relations, and activities involved in sensing. With the rise of the Web of Things and smart cities and homes more generally, actuators and the data they produce also become first-class citizens of the Web. Given their close relation to sensors, observations, procedures, and features of interest, it is desirable to provide a common ontology that also includes actuators and actuation."

---

### [SRC-002]

- **Título:** Semantic Sensor Network Ontology — 2023 Edition (Draft)
- **Entidad autora:** W3C / OGC Spatial Data on the Web Working Group
- **Año:** 2023
- **Tipo de fuente:** Especificación técnica W3C (Draft público)
- **URL o DOI:** https://w3c.github.io/sdw-sosa-ssn/ssn/
- **Página, sección o ubicación:** Sección de cambios respecto a edición 2017; nuevas clases y deprecaciones
- **Fragmento verificable:**
  > "Mark `ssn:Input`, `ssn:Output`, `sosa:Result` deprecated · Add 'abstract' superclasses `Execution` (superclass of Actuation, Observation and Sampling), `Asset` (superclass of Platform and System) Add `ExecutionCollection`, `ActuationCollection`, `ObservationCollection`, `SamplingCollection`, `SampleCollection`, `hasMember`, `isMemberOf` · Add `ActuatingProcedure`, `ObservingProcedure`, `SamplingProcedure` specializations of `Procedure` for each execution type · Add `hasFeatureOfInterest` support to `Deployment`"

---

### [SRC-003]

- **Título:** The modular SSN ontology: A joint W3C and OGC standard specifying the semantics of sensors, observations, sampling, and actuation
- **Entidad autora:** Haller et al. (W3C/OGC SDW Working Group)
- **Año:** 2019
- **Tipo de fuente:** Artículo científico revisado por pares — Semantic Web Journal
- **URL o DOI:** https://dl.acm.org/doi/abs/10.3233/SW-180320
- **Página, sección o ubicación:** Abstract; sección de arquitectura modular SSN/SOSA; tabla de clases y relaciones
- **Fragmento verificable:**
  > "The Sensor, Observation, Sample, and Actuator (SOSA) ontology provides a formal but lightweight general-purpose specification for modelling the interaction between the entities involved in the acts of observation, actuation, and sampling. SOSA is the result of rethinking the W3C-XG Semantic Sensor Network (SSN) ontology based on changes in scope and target audience, technical developments, and lessons learned over the past years. SOSA also acts as a replacement of SSN's Stimulus Sensor Observation (SSO) core."

---

### [SRC-004]

- **Título:** MCBO: Mammalian Cell Bioprocessing Ontology, A Hub-and-Spoke, IOF-Anchored Application Ontology
- **Entidad autora:** Robasky, Morrissey, Riedl, Dräger, Borth, Betenbaugh, Lewis
- **Año:** 2026
- **Tipo de fuente:** Preprint — bioRxiv (no peer-reviewed al momento de consulta)
- **URL o DOI:** https://doi.org/10.64898/2026.01.05.697007
- **Página, sección o ubicación:** Sección de diseño ontológico; definición de `MammalianCellCultureProcess`; modelado de condiciones de cultivo
- **Fragmento verificable:**
  > "MammalianCellCultureProcess is defined as the intersection of CellCultureProcess and a participant restriction requiring at least one MammalianCell. This supports automated classification and prevents generic bioprocessing templates from being conflated with mammalian-specific logic. To maintain BFO consistency, culture environmental conditions are modeled as qualities of the material cell culture system, consistent with BFO principles."

---

### [SRC-005]

- **Título:** Towards Ontologizing a Digital Twin Framework for Manufacturing
- **Entidad autora:** Drobnjaković, Kulvatunyou, Frechette, Srinivasan — NIST / ASME CIE
- **Año:** 2023
- **Tipo de fuente:** Artículo técnico NIST — conferencia ASME Computers and Information in Engineering (CIE)
- **URL o DOI:** https://tsapps.nist.gov/publication/get_pdf.cfm?pub_id=936637
- **Página, sección o ubicación:** Figuras 5, 6, 7 y 8; sección de aplicación a biorreactor
- **Fragmento verificable:**
  > "As an example of application-level ontology for biomanufacturing, consider a bioreactor (an essential biomanufacturing equipment) and its digital twin. Figure 7 represents how the data collected from sensors attached to a bioreactor are used to update the digital twin of the bioreactor. The other direction represents how simulation results from a digital twin of the bioreactor are used to control the parameters of actuators of the bioreactor."

---

### [SRC-006]

- **Título:** A Basic Formal Ontology-Based Ontological Modeling for Plan and Occurrence, a Biomanufacturing Process Verification Use Case
- **Entidad autora:** Šormaz, Seeharit, Kulvatunyou, Drobnjaković — NIST / ASME CIE
- **Año:** 2024
- **Tipo de fuente:** Artículo técnico NIST — conferencia ASME Computers and Information in Engineering (CIE 44)
- **URL o DOI:** https://www.nist.gov/publications/basic-formal-ontology-based-ontological-modeling-plan-and-occurrence-biomanufacturing
- **Página, sección o ubicación:** Abstract; introducción; sección de desarrollo ontológico; validación con biorreactor fed-batch
- **Fragmento verificable:**
  > "The nature of biochemical processes requires complex planning and control, with many controlled and non-controllable variables that impact the quality of bioproducts. Representing biomanufacturing process knowledge, control models, and actual occurrences in coherent ontologies could aid both humans and computers in dealing with the complexity. However, there is a lack of such coherent ontologies. Even though the Industrial Ontology Foundry (IOF) Core ontology has provided a groundwork based on the widely used Basic Formal Ontology (BFO) for such ontological requirements, there are still insufficient constructs and clear guidance on the representation of digital artifacts and their correspondences to the physical counterparts."

---

### [SRC-007]

- **Título:** Basic Formal Ontology (BFO) — ISO/IEC 21838-2:2021
- **Entidad autora:** Smith et al. / ISO Joint Technical Committee
- **Año:** 2021
- **Tipo de fuente:** Estándar internacional ISO (referenciado a través de fuentes secundarias verificables)
- **URL o DOI:** ISO/IEC 21838-2:2021 (no acceso abierto); referencia verificable en https://en.wikipedia.org/wiki/Basic_Formal_Ontology
- **Página, sección o ubicación:** Estructura general BFO: división Continuant / Occurrent; subclases MaterialEntity, Object, Quality, GenericallyDependentContinuant, Process
- **Fragmento verificable:**
  > "BFO is a formal ontology. The structure of BFO is based on a division of entities into two disjoint categories of continuant and occurrent, the former consists of objects and spatial regions, the latter contains processes conceived as extended through (or spanning) time. BFO thereby seeks to consolidate both time and space within a single framework."

---

### [SRC-008]

- **Título:** ISA-88 Formalization. A Step Towards its Integration with the ISA-95 Standard
- **Entidad autora:** Esteras-Chópite et al.
- **Año:** 2014
- **Tipo de fuente:** Artículo científico — taller FOMI, CEUR Workshop Proceedings Vol. 1333
- **URL o DOI:** https://ceur-ws.org/Vol-1333/fomi2014_4.pdf
- **Página, sección o ubicación:** Sección de implementación OWL 2; módulo de Control Procedimental; descripción de módulos ontológicos ISA-88
- **Fragmento verificable:**
  > "The models proposed within ISA-88 are taken into account to divide the proposed ontology into small ontology modules. The main goal of the ontology implementation activity is to create a computable model deployed in an ontology language from the conceptual model created during the conceptualization phase. Based on its ample acceptance, the OWL 2 language, developed by the W3C (World Wide Web Consortium), was chosen to implement the ontology and the Protegé 4.3 editor has been selected to support the ontology development and implementation."

---

### [SRC-009]

- **Título:** Data Infrastructure for Biomanufacturing Process Control
- **Entidad autora:** NIST — Material Measurement Laboratory / Engineering Laboratory
- **Año:** 2025
- **Tipo de fuente:** Página de proyecto institucional NIST
- **URL o DOI:** https://www.nist.gov/programs-projects/data-infrastructure-biomanufacturing-process-control
- **Página, sección o ubicación:** Sección "Technical Idea"; descripción de arquitectura hub-and-spoke BFO+IOF; mención de ISA-88 e ISA-95
- **Fragmento verificable:**
  > "To develop a high-quality and consistent manufacturing ontology for the biopharmaceutical industry and beyond, the technical idea is to use the Basic Formal Ontology (BFO), which has been successfully used as the top-level ontology for the biomedical domain, as a basis. From there, a hub-and-spoke architecture to derive increasingly domain-specific ontologies will be used. Other technical ideas for developing domain ontology includes ontologizing based on existing industry standards such as the ISA-88 and ISA-95 and defining ontology quality metrics."
