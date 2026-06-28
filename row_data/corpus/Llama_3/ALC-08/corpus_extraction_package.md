# Paquete de entrada para extracción condicionada por corpus

## Pregunta [ALC-08]: ¿Qué conceptos deben quedar fuera del alcance inicial para evitar que la ontología sea demasiado amplia?

## Reglas para el modelo receptor

- Trabaja exclusivamente con las fuentes y fragmentos incluidos.
- No uses conocimiento externo.
- Cuando la evidencia sea insuficiente, responde: No establecido en el corpus suministrado.
- Diferencia evidencia explícita e inferencia razonable.
- No conviertas conceptos o triadas en axiomas definitivos.

## Corpus de fuentes seleccionadas

### [SRC-001]

- **Título:** BioLector XT Technical Data Sheet
- **Entidad autora:** Beckman Coulter / m2p-labs
- **Año:** s.f.
- **Tipo de fuente:** Ficha técnica oficial
- **URL o DOI:** https://www.beckman.es/resources/reading-material/product-instructions/biolector-xt-technical-data-sheet
- **Página, sección o ubicación:** Cultivation conditions
- **Fragmento verificable:** > TEMPERATURE
  > 10 – 50 °C (min. temp.: 8 °C below ambient temp.)
  > SHAKING SPEED
  > 100 – 1500 rpm (3 mm diameter)
  > OXYGEN OPTODES
  > 0 – 100 % dissolved oxygen\*1
  > pH OPTODES
  > pH 4 – 7.5 (depending on plate)

### [SRC-002]

- **Título:** BIOSTAT B-DCU Operating Instructions Manual
- **Entidad autora:** Sartorius Stedim Biotech
- **Año:** 2023
- **Tipo de fuente:** Manual oficial
- **URL o DOI:** https://www.manualslib.com/manual/3061881/Sartorius-Stedim-Biotech-Biostat-B-Dcu.html
- **Página, sección o ubicación:** Page 19, Device Description
- **Fragmento verificable:** > Com Alarm
  > Potential-free alarm contacts (X23)
  > When an alarm triggers (see Chapter 10 .3, page 163):
  > Host
  > Ethernet port for an external host system
  > e .g ., MFCS SCADA

### [SRC-003]

- **Título:** Ten Simple Rules for Selecting a Bio-ontology
- **Entidad autora:** Malone J., Stevens R., Jupp S., Hancocks T., Parkinson H., Brooksbank C.
- **Año:** 2016
- **Tipo de fuente:** Artículo revisado por pares
- **URL o DOI:** https://doi.org/10.1371/journal.pcbi.1004743
- **Página, sección o ubicación:** Rule 1
- **Fragmento verificable:** > Rule 1: The Ontology Should Be about a Specific Domain of Knowledge
  > Specifically, an ontology should provide coverage for the area it claims to describe.

### [SRC-004]

- **Título:** Best Practices: Ontology Development and Curation
- **Entidad autora:** Carmody L., NIEHS
- **Año:** 2025
- **Tipo de fuente:** Guía institucional
- **URL o DOI:** https://www.niehs.nih.gov/sites/default/files/2025-03/CARMODY_bestpractices_508.pdf
- **Página, sección o ubicación:** OBO Foundry Principles, P5
- **Fragmento verificable:** > P5) Scope - extent of the domain or subject matter it intends to cover.

### [SRC-005]

- **Título:** Survey of modular ontology techniques and their applications in the biomedical domain
- **Entidad autora:** PMC
- **Año:** 2009
- **Tipo de fuente:** Revisión
- **URL o DOI:** https://pmc.ncbi.nlm.nih.gov/articles/PMC3113511/
- **Página, sección o ubicación:** Section 2.3 Properties; Section 2.2 Goals
- **Fragmento verificable:** > Size: A module M i (O) of an ontology O should be as small as possible.
  > Partial Reuse: With the increasing popularity of Semantic Web and modern ontology development languages such as OWL [ 1 ], there has been a proliferation of numerous domain-specific ontologies in the recent years. Thus, to promote their adoption in developing both intra- and inter-domain applications, reuse emerges as an important issue.
