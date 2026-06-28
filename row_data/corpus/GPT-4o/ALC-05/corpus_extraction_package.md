# Paquete de entrada para extracción condicionada por corpus

## Pregunta ALC-05: ¿Cómo se separan ontológicamente el equipo físico, el proceso biológico, el sistema de control, las variables medidas y los datos generados?

## Reglas para el modelo receptor

- Trabaja exclusivamente con las fuentes y fragmentos incluidos.
- No uses conocimiento externo.
- Cuando la evidencia sea insuficiente, responde: No establecido en el corpus suministrado.
- Diferencia evidencia explícita e inferencia razonable.
- No conviertas conceptos o triadas en axiomas definitivos.

## Corpus de fuentes seleccionadas

### [SRC-001]

- **Título:** BioLector XT Microbioreactor
- **Entidad autora:** Beckman Coulter Life Sciences
- **Año:** No especificado en la página
- **Tipo de fuente:** Página oficial de producto
- **URL o DOI:** [https://www.beckman.com/microbioreactor/biolector-xt](https://www.beckman.com/microbioreactor/biolector-xt) ([beckman.com][1])
- **Página, sección o ubicación:** Descripción principal del producto
- **Fragmento verificable:** > “The high-throughput microbioreactor enables real-time evaluation of biomass, fluorescence, pH, dissolved oxygen in the liquid phase (DO), and other key cultivation parameters for aerobes and anaerobes.”

### [SRC-002]

- **Título:** BioLector XT Technical Data Sheet
- **Entidad autora:** Beckman Coulter Life Sciences
- **Año:** No especificado en la página
- **Tipo de fuente:** Ficha técnica oficial
- **URL o DOI:** [https://www.beckman.com/resources/reading-material/product-instructions/biolector-xt-technical-data-sheet](https://www.beckman.com/resources/reading-material/product-instructions/biolector-xt-technical-data-sheet) ([beckman.com][2])
- **Página, sección o ubicación:** “Microfluidic Bioprocess Control”; “Cultivation conditions”; “Microfluidic features”; “Available optional modules”
- **Fragmento verificable:** > “TRIGGERED pH CONTROL (CLOSED LOOP CONTROLLER)”
- **Fragmento verificable:** > “Active control of pH according to online signals and continuous feeding of up to two solutions”

### [SRC-003]

- **Título:** Biostat® B: The Multi-Talented Bioreactor for Research and Development
- **Entidad autora:** Sartorius Stedim Biotech GmbH
- **Año:** 2025
- **Tipo de fuente:** Brochure técnico oficial
- **URL o DOI:** [https://www.sartorius.com/download/34576/broch-biostat-b-sbi1513-e-1--data.pdf](https://www.sartorius.com/download/34576/broch-biostat-b-sbi1513-e-1--data.pdf) ([Sartorius][3])
- **Página, sección o ubicación:** Página 6, “Biostat® B – Configurable Flexibility”; página 11, “Automatic Feed Control and Continuous Processing”; “Automatic pH Control”; “Automatic DO Control”
- **Fragmento verificable:** > “The control tower contains both the aeration, pump and temperature control modules, saving valuable bench space in your lab.”

### [SRC-004]

- **Título:** Univessel® Glass - Autoclavable Cultivation Vessel
- **Entidad autora:** Sartorius
- **Año:** No especificado en la página
- **Tipo de fuente:** Página oficial de producto
- **URL o DOI:** [https://www.sartorius.com/en/products/fermentation-bioreactors/benchtop-bioreactors/univessel-glass](https://www.sartorius.com/en/products/fermentation-bioreactors/benchtop-bioreactors/univessel-glass) ([Sartorius][4])
- **Página, sección o ubicación:** Párrafo inmediatamente anterior a “Downloads”
- **Fragmento verificable:** > “The vessel is available as 2 L, 5 L and 10 L version.”

### [SRC-005]

- **Título:** Semantic Sensor Network Ontology - 2023 Edition
- **Entidad autora:** World Wide Web Consortium
- **Año:** 2025
- **Tipo de fuente:** Estándar semántico W3C
- **URL o DOI:** [https://www.w3.org/TR/vocab-ssn-2023/](https://www.w3.org/TR/vocab-ssn-2023/) ([W3C][5])
- **Página, sección o ubicación:** Sección 5.3.2.2.2, `sosa:Property`; sección 5.3.5.1, “Overview”
- **Fragmento verificable:** > “Property — identifiable quality of features of interest that can be observed or acted upon.”
- **Fragmento verificable:** > “A sosa:System is an instrument or equipment, including software systems and agents where relevant, that implements a procedure in the context of executions.”

### [SRC-006]

- **Título:** PROV-O: The PROV Ontology
- **Entidad autora:** W3C Provenance Working Group
- **Año:** 2013
- **Tipo de fuente:** Recomendación W3C
- **URL o DOI:** [https://www.w3.org/TR/prov-o/](https://www.w3.org/TR/prov-o/) ([W3C][6])
- **Página, sección o ubicación:** Sección 3.1, “Starting Point Terms”; sección 4, `prov:wasGeneratedBy`
- **Fragmento verificable:** > “An activity is something that occurs over a period of time and acts upon or with entities.”
- **Fragmento verificable:** > “Generation is the completion of production of a new entity by an activity.”

[1]: https://www.beckman.com/microbioreactor/biolector-xt "BioLector XT Microbioreactor"
[2]: https://www.beckman.com/resources/reading-material/product-instructions/biolector-xt-technical-data-sheet "BioLector XT Technical Data Sheet"
[3]: https://www.sartorius.com/download/34576/broch-biostat-b-sbi1513-e-1--data.pdf "Biostat® B Multi-talented bioreactor"
[4]: https://www.sartorius.com/en/products/fermentation-bioreactors/benchtop-bioreactors/univessel-glass "Univessel® Glass - Autoclavable Cultivation Vessel | Sartorius"
[5]: https://www.w3.org/TR/vocab-ssn-2023/ "Semantic Sensor Network Ontology - 2023 Edition"
[6]: https://www.w3.org/TR/prov-o/ "PROV-O: The PROV Ontology"
