# Paquete de entrada para extracción condicionada por corpus

## Pregunta [ALC-05]: ¿Cómo se separan ontológicamente el equipo físico, el proceso biológico, el sistema de control, las variables medidas y los datos generados?

## Reglas para el modelo receptor

- Trabaja exclusivamente con las fuentes y fragmentos incluidos.
- No uses conocimiento externo.
- Cuando la evidencia sea insuficiente, responde: No establecido en el corpus suministrado.
- Diferencia evidencia explícita e inferencia razonable.
- No conviertas conceptos o triadas en axiomas definitivos.

## Corpus de fuentes seleccionadas

### [SRC-001]

- **Título:** BioLector XT Microbioreactor – Technical Specifications
- **Entidad autora:** Beckman Coulter, Inc. / m2p-labs GmbH
- **Año:** 2021
- **Tipo de fuente:** Datasheet oficial
- **URL o DOI:** https://media.beckman.com/-/media/pdf-assets/technical-note/technical-datasheet-biolector-xt.pdf
- **Página, sección o ubicación:** Technical Specifications
- **Fragmento verificable:** > 0 – 100 % dissolved oxygen\*1
- **Fragmento verificable:** > pH 4 – 7.5 (depending on plate)
- **Fragmento verificable:** > 10 – 50 °C (min. temp.: 8 °C below ambient temp.)
- **Fragmento verificable:** > 100 – 1500 rpm (3 mm diameter)
- **Fragmento verificable:** > pH control range: 4.0 – 7.5 (depending on plate) Fully editable PI control
- **Fragmento verificable:** > Filling volume: 800 – 1900 μL (rpm dependent)

### [SRC-002]

- **Título:** Biostat® B – The Multi-Talented Bioreactor for Research and Development
- **Entidad autora:** Sartorius Stedim Biotech
- **Año:** 2023 (documento vigente)
- **Tipo de fuente:** Brochure técnico
- **URL o DOI:** https://www.sartorius.com/download/34576/5/broch-biostat-b-sbi1513-e-1--data.pdf
- **Página, sección o ubicación:** p.2-5, p.8
- **Fragmento verificable:** > Our proven autoclavable borosilicate glass culture vessel is available in four different volumes: 1 L, 2 L, 5 L and 10 L
- **Fragmento verificable:** > The control tower contains both the aeration, pump and temperature control modules
- **Fragmento verificable:** > Control the pH of your culture by automatic acid and base addition or by CO₂ aeration and base addition
- **Fragmento verificable:** > Besides classic DO cascade control, we have developed the unique advanced DO controller that gives you more flexibility to develop and optimize your DO control strategy
- **Fragmento verificable:** > BioPAT® MFCS is a "plugandplay" solution, ideally suited for capturing, storing and visualizing process data of the Biostat® B Control Tower

### [SRC-003]

- **Título:** BIOSTAT B Operating Manual – PID Controller Parameters
- **Entidad autora:** Sartorius Stedim Biotech
- **Año:** 2023
- **Tipo de fuente:** Manual de operación
- **URL o DOI:** https://www.manualslib.com/manual/3343908/Sartorius-Stedim-Biotech-Biostat-B.html?page=144
- **Página, sección o ubicación:** p.144
- **Fragmento verificable:** > Setting the "P", "I", or "D" Controller Parameters:
- **Fragmento verificable:** > The adaptation of PID controllers requires knowledge of control theory.

### [SRC-004]

- **Título:** BioLector XT Microbioreactor – High-Throughput Bioreactor
- **Entidad autora:** Beckman Coulter Life Sciences
- **Año:** 2024
- **Tipo de fuente:** Página técnica oficial
- **URL o DOI:** https://goto.beckman.com/en/microbioreactor-for-high-throughput-microfermentation-and-bioprocess-control/
- **Página, sección o ubicación:** descripción principal
- **Fragmento verificable:** > rapidly evaluate biomass, pH, dissolved oxygen (DO), fluorescence
- **Fragmento verificable:** > Superior Data Quality: Continuous monitoring improves reproducibility and reduces human error.

### [SRC-005]

- **Título:** Knowledge-Based Bioprocess Design for Protein Therapeutic Manufacturing
- **Entidad autora:** Stanford University – Bay Ontology Protein Solutions
- **Año:** 2020 (aprox.)
- **Tipo de fuente:** Proyecto académico
- **URL o DOI:** http://web.stanford.edu/class/biomedin210/Previous%20Projects/knowledge_based_protein_therapeutics_design.pdf
- **Página, sección o ubicación:** sección Ontology
- **Fragmento verificable:** > are Publication, Experiment, Culture, Organism, Product, Protocol, Vessel, and Chemical.
- **Fragmento verificable:** > Vessel data: volume (str)
- **Fragmento verificable:** > Control Protocol data: deadband (int), duration (ind), setpoint (int)

### [SRC-006]

- **Título:** Process analytical technology (PAT) needs and applications in the bioprocess industry
- **Entidad autora:** VTT Technical Research Centre of Finland
- **Año:** 2006
- **Tipo de fuente:** Informe técnico
- **URL o DOI:** https://www.researchgate.net/publication/240935706_Process_analytical_technology_PAT_needs_and_applications_in_the_bioprocess_industry
- **Página, sección o ubicación:** pp.3,6
- **Fragmento verificable:** > The bioprocess, generally associated with cultivation in appropriate bioreactors (fermenters), includes the cultivation of the living biocatalyst to a high density
- **Fragmento verificable:** > Generally only 'basic' measurements, like physical (temperature, weight, pressure, conductivity, gas and liquid flow, foam level, stirrer speed and power) and chemical measurements (pH, pO2)
