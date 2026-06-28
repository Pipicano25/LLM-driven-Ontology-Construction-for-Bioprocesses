# Paquete de entrada para extracción condicionada por corpus

## Pregunta ALC-06: ¿Qué propiedades generales deben describir cualquier biorreactor del proyecto, independientemente de su escala o volumen?

## Reglas para el modelo receptor

- Trabaja exclusivamente con las fuentes y fragmentos incluidos.
- No uses conocimiento externo.
- Cuando la evidencia sea insuficiente, responde: No establecido en el corpus suministrado.
- Diferencia evidencia explícita e inferencia razonable.
- No conviertas conceptos o triadas en axiomas definitivos.

---

## Corpus de fuentes seleccionadas

### [SRC-001]

- **Título:** BioLector XT Microbioreactor — Technical Specifications
- **Entidad autora:** m2p-labs GmbH / Beckman Coulter, Inc.
- **Año:** 2021
- **Tipo de fuente:** Ficha técnica oficial de fabricante
- **URL o DOI:** https://star-lab.am/upload/iblock/090/k7j5o0umvmxo8yun07514kcwfs77bwos/planshetnyj_mikrobioreaktor_biolector_xt_m2p_labs_specifikaciya.pdf
- **Página, sección o ubicación:** Sección CULTIVATION CONDITIONS; sección OXYGEN OPTODES; sección pH OPTODES; sección MICROFLUIDIC FEATURES; sección MICROTITER PLATES; sección AVAILABLE OPTIONAL MODULES; sección LAB SPACE AND MATERIAL REQUIREMENTS
- **Fragmento verificable:**

> CULTIVATION CONDITIONS / TEMPERATURE: 10 – 50 °C (min. temp.: 8 °C below ambient temp.) / SHAKING SPEED: 100 – 1500 rpm (3 mm diameter) / ENVIRONMENTAL CONDITIONS: Active humidification / Ambient air / 1 – 100 % O2 (optional) / 0 – 12 % CO2 (optional) / Anaerobic cultivation (optional) / OXYGEN OPTODES: 0 – 100 % dissolved oxygen / pH OPTODES: pH 4 – 7.5 (depending on plate) / MTP READING TIME: 2.7 min / filter / 48 wells @ 1000 rpm
>
> MICROFLUIDIC FEATURES / TRIGGERED pH CONTROL (CLOSED LOOP CONTROLLER): pH control range: 4.0 – 7.5 (depending on plate) / Fully editable PI control / Slow, medium and fast PI default settings / FEEDING OPTIONS: Two sided pH control (alkali and acid) / One sided pH control and one feed line (alkali or acid + one feed) / Two feed lines / FEEDING PROFILES: Profile equation: dV/dt = A+B×t+C×eD×t / Constant: A [μL/h] / Linear: A [μL/h] and B [μL/h²] / Exponential: A [μL/h], B [μL/h²], C [μL/h] and D [h-1] / Pulse feed
>
> MICROTITER PLATES / FLOWERPLATE: 48 cultivation wells / Filling volume: 800 – 1900 μL (rpm dependent) / High OTR and high kLa / ROUND WELL PLATE: 48 cultivation wells / Filling volume: 1000 – 2400 μL (rpm dependent) / Lower OTR and low shear force / MICROFLUIDIC PLATE: Available as both FlowerPlate and Round Well Plate / 32 cultivation wells controlled by 16 reservoir wells / Maximum filling volumes in reservoir wells: 1800 µL (FlowerPlate) and 2000 µL (Round Well Plate)
>
> AVAILABLE OPTIONAL MODULES: E-XTMF Microfluidic module — Active control of pH according to online signals and continuous feeding of up to two solutions (only with Microfluidic plates) / E-O2XT-100 O2 up-regulation module — Control of gas atmosphere in head space: 21 – 100 % O2 / E-O2XT-25 O2 down-regulation module — Control of gas atmosphere in head space: 1 – 21 % O2 (use only with N2) / E-CO2XT-12 CO2 up-regulation module — Control of gas atmosphere in head space: 0 – 12 % CO2 / E-AN-300 Anaerobic cultivation module — Gassing with 100 % N2 allows cultivation of organisms in anaerobic conditions (use only with N2) / All optional modules compatible in one BioLector microbioreactor device.
>
> Application mode: Disposable technology / Interface: Ethernet / Device weight: 58 kg for BioLector XT microbioreactor (61 kg with microfluidic module) and 44 kg for valve control unit

---

### [SRC-002]

- **Título:** BIOSTAT® Bplus Exclusive Flow — Benchtop Bioreactor Controller Specifications
- **Entidad autora:** Sartorius Stedim Biotech
- **Año:** 2023 (fecha de publicación del documento en repositorio de Richmond Scientific)
- **Tipo de fuente:** Ficha técnica oficial de fabricante
- **URL o DOI:** https://www.richmondscientific.com/wp-content/uploads/2023/04/Sartorius-Stedim-Biostat-Bplus-Exclusive-Flow-Benchtop-Bioreactor-Controller-Specifications.pdf
- **Página, sección o ubicación:** Secciones: Basic Unit; Measurement Ranges; Gassing System Exclusive Flow; Agitation System; Temperature Control System; Culture Vessel (pp. 24–27 del documento fuente)
- **Fragmento verificable:**

> Digital Controller: Graphical user interface with color display and touch-screen operation / Integrated amplifiers for Temperature, pH, DO, Foam & Level (Twin: combined Foam|Level amplifier) / Space for Redox and Turbidity amplifier (single only) / Integrated digital control loops for Temperature, pH, DO, agitation, gas mixing, total Sparger flow, total Overlay flow and 2+ substrate / Level control via Level probe or balance / Multi-stage DO cascade control / Totalizers with digital calibration for valves and pumps / In-process pH-recalibration / Trend display with up to 6 process values / Up to 2 direct balance connections
>
> Measurement Ranges: Agitation motor speed 1 L | 2 L | 5 L | 10 L: 20–2,000 | 20–2,000 | 20–1,500 | 20–800 rpm / Temperature: 0–150°C / pH: 2–12 / pO2: 0–100% / Turbidity (option): 0–6 AU / Redox (optional): –1,000 – 1,000 mV
>
> Gassing System Exclusive Flow: 4-gas mixing with Sparger and Overlay outlet / Gas mixing of Air, O2, N2, CO2 for Sparger gassing / Air for Overlay gassing / Gas flow range "Sparger" 1 L | 2 L | 5 L | 10 L: 0.016–0.166 | 0.016–0.166 | 0.05–0.5 | 0.1–1.0 [l/min] / Gas flow range "Overlay" 1 L | 2 L | 5 L | 10 L: 0.016–0.166 | 0.16–1.6 | 0.42–4.2 | 0.83–8.3 [l/min]
>
> Agitation Motor: Maintenance and gear-free servo drive / Performance: 200 W
>
> Temperature Control System: Dry heating system via heating blanket and automatic cooling water control valve / Temperature control range: 8°C above cooling water to 60°C / Heating blanket performance 1 L | 2 L | 5 L | 10 L: 100 | 170 | 400 | 780 [W] per culture vessel
>
> Culture Vessel: Total volume 1 L | 2 L | 5 L | 10 L: 1.6 | 3 | 6.6 | 13 [L] / Working volume 0.4–1 | 0.6–2 | 0.6–5 | 1.5 | 5–10 [L] / Design: Single wall glass vessel with stainless steel head and vertical lifting handles / pO2 electrode: Polarographic / pH electrode: Gel-filled / Temperature probe: Pt 100 / Redox electrode (option): Gel-filled / Turbidity probe (option): Single Channel NIR Absorption Probe, OPL 20 mm / Material (product wetted parts): Borosilicate glass | Stainless steel AISI 316L | EPDM
>
> Host communication: Ethernet | RS422 | RS232 / Housing material: Stainless steel AISI 304 / Power supply: 120 VAC or 230 VAC / Gasses: Controlled @ 1.5 barg dry, particle and oil-free
>
> Applicable for: Cell culture of insect, mammalian and plant cells / Culture of microorganisms / Batch, fed batch and continuous culture / Perfusion operation (easy to upgrade) / Small-scale cell mass, protein, MAb & vaccine production / High-cell density cultures / Suspension and microcarrier cultures

---

### [SRC-003]

- **Título:** Bioreactor — an overview (ScienceDirect Topics)
- **Entidad autora:** ScienceDirect / Elsevier (síntesis de literatura técnica revisada)
- **Año:** Vigente (actualización continua)
- **Tipo de fuente:** Revisión enciclopédica técnica
- **URL o DOI:** https://www.sciencedirect.com/topics/engineering/bioreactor
- **Página, sección o ubicación:** Párrafos descriptivos de propiedades generales y clasificación de biorreactores
- **Fragmento verificable:**

> These reactors have been designed to maintain certain parameters like flow rates, aeration, temperature, pH, foam control, and agitation rate. Reactors can provide an output to specified process parameter control elements to rectify any deviation in the value of these parameters from the user-defined set point. The number of parameters that can be monitored and controlled is limited by the number of sensors and control elements incorporated into a given bioreactor.
>
> Bioreactors are commonly designed as a cylindrical tank with an agitator and integral heating or cooling system, ranging in size from less than 1 L to more than 50,000 L, often made of steel, stainless steel, glass lined steel, or glass.
>
> The bioreactor's environmental conditions, including flow rates of gas (i.e., air, oxygen, nitrogen, carbon dioxide), temperature, pH and dissolved oxygen levels, and agitation speed/circulation rate, need to be closely monitored and controlled. As shown in Figure 1, most industrial bioreactor manufacturers use vessels, sensors, and a control system networked together.
>
> On the basis of mode of operation, a bioreactor may be classified as batch, fed batch, or continuous (e.g., a continuous stirred-tank reactor model).

---

### [SRC-004]

- **Título:** Deep Dive: Fermentation Upstream Bioprocess Design
- **Entidad autora:** Good Food Institute (GFI)
- **Año:** 2025
- **Tipo de fuente:** Revisión técnica institucional con referencias citadas
- **URL o DOI:** https://gfi.org/science/the-science-of-fermentation/deep-dive-fermentation-upstream-bioprocess-design/
- **Página, sección o ubicación:** Sección de clasificación de parámetros de biorreactor
- **Fragmento verificable:**

> These can be grouped into three [categories]: (1) physical, such as temperature, vessel pressure, agitation rate, and medium viscosity, (2) chemical, such as pH, nutrient concentration, and gas concentration like dissolved oxygen (DO), and (3) [biological/biochemical parameters].
>
> Many different bioreactors can be classified in several ways, such as by gas transfer, agitation type, water content, feedstock, and temperature. In general, bioreactors can be classified as either submerged or SSF systems. In submerged fermentation, the substrate to be fermented is always in a liquid phase along with the nutrients required for microorganism growth, and gas exchange occurs via mixing.
