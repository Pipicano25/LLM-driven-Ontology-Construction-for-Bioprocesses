# Paquete de entrada para extracción condicionada por corpus

## Pregunta [ALC-04]: ¿Qué componentes comunes permiten describir estos tres biorreactores en una misma ontología?

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
- **Año:** No establecido en la fuente.
- **Tipo de fuente:** Ficha técnica oficial.
- **URL o DOI:** [https://www.beckman.com/resources/reading-material/product-instructions/biolector-xt-technical-data-sheet](https://www.beckman.com/resources/reading-material/product-instructions/biolector-xt-technical-data-sheet) ([Beckman Coulter][1])
- **Página, sección o ubicación:** “Cultivation conditions”.
- **Fragmento verificable:**

  > “SHAKING SPEED 100 – 1500 rpm (3 mm diameter)
  > OXYGEN OPTODES 0 – 100 % dissolved oxygen
  > pH OPTODES pH 4 – 7.5 (depending on plate)” ([Beckman Coulter][1])

### [SRC-002]

- **Título:** Biostat® B: The Multi-Talented Bioreactor for Research and Development
- **Entidad autora:** Sartorius Stedim Biotech GmbH
- **Año:** 2025
- **Tipo de fuente:** Folleto técnico oficial.
- **URL o DOI:** [https://www.sartorius.com/download/34576/broch-biostat-b-sbi1513-e-1--data.pdf](https://www.sartorius.com/download/34576/broch-biostat-b-sbi1513-e-1--data.pdf) ([Sartorius][2])
- **Página, sección o ubicación:** PDF p. 22, “Basic Configurations for Univessel® Glass”, “Microbial Packages”.
- **Fragmento verificable:**

  > “Volume: 1 L, 2 L, 5 L or 10 L
  > Control temperature, pH, DO, stirrer speed
  > 2 integrated pumps for pH control (acid | base)” ([Sartorius][2])

[1]: https://www.beckman.com/resources/reading-material/product-instructions/biolector-xt-technical-data-sheet "BioLector XT Technical Data Sheet"
[2]: https://www.sartorius.com/download/34576/broch-biostat-b-sbi1513-e-1--data.pdf "Biostat® B Multi-talented bioreactor"
