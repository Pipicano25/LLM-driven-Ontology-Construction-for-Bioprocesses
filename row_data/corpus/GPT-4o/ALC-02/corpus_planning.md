## 1. Identificación de la pregunta

- **ID:** ALC-02
- **Nivel metodológico:** Conceptual-definicional y de delimitación ontológica.
- **Tema:** Distinción entre `BioreactorSystem` y `CultureVessel`.
- **Pregunta:** ¿Qué características mínimas debe tener un sistema para ser considerado biorreactor y no solo un recipiente de cultivo?

---

## 2. Propósito de la pregunta

La pregunta busca establecer un criterio ontológico mínimo para distinguir un sistema de biorreacción de un recipiente pasivo de cultivo, como un matraz, placa, frasco o tanque sin capacidades explícitas de control del proceso.

Este criterio contribuye al corpus y a la ontología preliminar porque permite:

- Separar `CultureVessel` de `BioreactorSystem`.
- Representar capacidades de control, monitorización, sensores, actuadores y software.
- Evitar asumir que volumen, material, tipo de agitación o número de sensores son requisitos universales.
- Modelar correctamente sistemas multiescala como BioLector XT y Biostat B de 5 L y 10 L.

---

## 3. Plan de búsqueda documental

### Información técnica requerida

1. Definiciones académicas o técnicas de biorreactor.
2. Evidencia sobre control de condiciones de cultivo.
3. Diferenciación entre biorreactores, matraces agitados, incubadores y recipientes de cultivo.
4. Componentes funcionales: recipiente, sensor, controlador, actuador, software, setpoint.
5. Evidencia de variantes multiescala: microbioreactores, sistemas de sobremesa de 5 L y 10 L.
6. Evidencia sobre qué características son dependientes de la aplicación: pH, DO, temperatura, aireación, agitación, alimentación y muestreo.

### Tipos de documentos necesarios

- Revisiones científicas revisadas por pares.
- Artículos sobre control de biorreactores y microbioreactores.
- Manuales, brochures y application notes oficiales.
- Fichas técnicas de BioLector XT y Sartorius Biostat B.
- Normas terminológicas o estándares, solo si su alcance incluye cultivo o bioprocesamiento.

### Repositorios y sitios sugeridos

- PubMed, PMC, Crossref, ScienceDirect, Springer, MDPI.
- Sitios oficiales de Sartorius, Beckman Coulter Life Sciences y Eppendorf.
- ISO Online Browsing Platform.
- Repositorios académicos institucionales, como UCL Discovery.

### Términos de búsqueda

**Español**

- `"biorreactor sistema controlado cultivo"`
- `"biorreactor recipiente de cultivo diferencia"`
- `"sensor actuador controlador biorreactor"`
- `"microbiorreactor control pH oxígeno disuelto"`
- `"biorreactor Sartorius 5 L 10 L control pH DO"`
- `"BioLector XT monitorización control pH DO"`

**Inglés**

- `"bioreactor controlled system cultivation definition"`
- `"bioreactor versus culture vessel process control"`
- `"bioreactor sensor controller actuator setpoint"`
- `"microbioreactor online monitoring process control"`
- `"Biostat B 5 L 10 L temperature pH DO control"`
- `"BioLector XT microfluidic pH control dissolved oxygen"`

### Ecuaciones de búsqueda sugeridas

```text
("bioreactor" AND "controlled system" AND cultivation)
```

```text
("bioreactor" AND sensor AND controller AND actuator AND setpoint)
```

```text
("culture vessel" OR "shake flask") AND bioreactor AND control
```

```text
("microbioreactor" AND "online monitoring" AND "process control")
```

```text
("BioLector XT" AND pH AND DO AND control)
```

```text
("Biostat B" AND "5 L" AND "10 L" AND "temperature" AND "pH")
```

### Criterios aplicados

**Inclusión**

- Relación directa con definición, control o arquitectura funcional de biorreactores.
- Fuente oficial, artículo revisado por pares o repositorio académico verificable.
- Evidencia localizable por página, sección, tabla o método.
- Utilidad para BioLector XT, Biostat B de 5 L y 10 L, o sistemas comparables.

**Exclusión**

- Alcance distinto del cultivo biológico, por ejemplo biorreactores de tratamiento de suelos.
- Fuentes comerciales sin trazabilidad técnica.
- Manuales alojados por terceros sin verificación oficial.
- Documentos sin fecha, entidad responsable o evidencia localizable.

---

## 4. Documentos candidatos encontrados

| ID documento | Título                                                                                             |                              Entidad autora |   Año | Tipo de fuente                | URL/DOI verificable                                                                                                                                                              | Relación con la pregunta                                                                                         | Decisión preliminar |
| ------------ | -------------------------------------------------------------------------------------------------- | ------------------------------------------: | ----: | ----------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------- | ------------------- |
| DOC-01       | _Bioreactors: Applications and Innovations for a Sustainable and Healthy Future—A Critical Review_ |                            Palladino et al. |  2024 | Revisión revisada por pares   | DOI: 10.3390/app14209346                                                                                                                                                         | Define los biorreactores como sistemas controlados para cultivar microorganismos y células.                      | Include             |
| DOC-02       | _Recent Advances in Fed-Batch Microscale Bioreactor Design_                                        |                              Teworte et al. |  2022 | Revisión revisada por pares   | DOI: 10.1016/j.biotechadv.2021.107888                                                                                                                                            | Describe arquitectura de control en microbioreactores: sensores, unidad de control, alimentación y ajuste de pH. | Include             |
| DOC-03       | _Bioreactor Control Systems in the Biopharmaceutical Industry: A Critical Perspective_             |                              Mitra y Murthy |  2022 | Revisión revisada por pares   | DOI: 10.1007/s43393-021-00048-6                                                                                                                                                  | Examina control de condiciones y variantes de biorreactores.                                                     | Include             |
| DOC-04       | _Bioreactors and Fermenters: Powerful Tools for Resolving Cultivation Bottlenecks_                 |                 Ulrike Rasche, Eppendorf AG |  2020 | Documento técnico patrocinado | [PDF oficial](https://www.eppendorf.com/product-media/doc/en/897339/Fermentors-Bioreactors_Publication_Bioprocess_Bioprocessing-basics.pdf)                                      | Distingue biorreactores de matraces y describe sensores, software y actuadores.                                  | Include             |
| DOC-05       | _Biostat® B: The Multi-Talented Bioreactor for Research and Development_                           |                                   Sartorius |  2021 | Brochure técnico oficial      | [PDF oficial](https://www.sartorius.com/download/34576/broch-biostat-b-sbi1513-e-1--data.pdf)                                                                                    | Evidencia concreta para configuraciones Sartorius de 5 L y 10 L.                                                 | Include             |
| DOC-06       | _Aerobic Cultivation of High-Oxygen-Demanding Microorganisms in the BioLector XT Microbioreactor_  | Noud Drummen, Beckman Coulter Life Sciences |  2025 | Application note oficial      | [PDF oficial](https://media.beckman.com/-/media/pdf-assets/application-notes/aerobic-cultivation-high-oxygen-demanding-microorganisms-biolector-xt-microbioreactor-app-note.pdf) | Evidencia específica de BioLector XT con monitorización, control de pH, alimentación y gases.                    | Include             |
| DOC-07       | _BioLector XT Technical Data Sheet_                                                                |               Beckman Coulter Life Sciences | s. f. | Ficha técnica oficial         | [Página oficial](https://www.beckman.com/resources/reading-material/product-instructions/biolector-xt-technical-data-sheet)                                                      | Especifica temperatura, velocidad de agitación, optodos de pH y DO, y opciones de control.                       | Uncertain           |
| DOC-08       | ISO 11074:2025, _Soil Quality — Vocabulary_                                                        |                                         ISO |  2025 | Norma terminológica           | ISO Online Browsing Platform                                                                                                                                                     | Define biorreactor en contexto de biotratamiento de sólidos, no de cultivo multiescala.                          | Exclude             |

DOC-01 caracteriza al biorreactor como un sistema controlado de cultivo. ([MDPI][1]) DOC-02 está disponible como versión aceptada de una revisión publicada en _Biotechnology Advances_. ([UCL Discovery][2]) DOC-03 está publicado en _Systems Microbiology and Biomanufacturing_. ([Hep Journals][3])

---

## 5. Evaluación de documentos candidatos

| ID documento | Relevancia | Autoridad | Trazabilidad | Cobertura de la pregunta | Evidencia localizable | Justificación                                                                                                                              |
| ------------ | ---------- | --------- | ------------ | ------------------------ | --------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| DOC-01       | Alta       | Alta      | Alta         | Alta                     | Alta                  | Aporta una definición general reciente de biorreactor como sistema controlado de cultivo. ([MDPI][1])                                      |
| DOC-02       | Alta       | Alta      | Alta         | Alta                     | Alta                  | Presenta mecanismos de control en microbioreactores y relaciones entre sensores, controladores y adición de líquidos. ([UCL Discovery][2]) |
| DOC-03       | Alta       | Alta      | Alta         | Alta                     | Media                 | Revisión especializada sobre sistemas de control para biorreactores y parámetros operativos. ([Hep Journals][3])                           |
| DOC-04       | Alta       | Media     | Alta         | Alta                     | Alta                  | Aunque anterior a 2021 y patrocinado, ofrece comparación directa entre matraces y biorreactores.                                           |
| DOC-05       | Alta       | Alta      | Alta         | Media                    | Alta                  | Fuente primaria para las configuraciones Biostat B de 5 L y 10 L. ([Sartorius][4])                                                         |
| DOC-06       | Alta       | Alta      | Alta         | Media                    | Alta                  | Fuente primaria específica para BioLector XT con módulo microfluídico.                                                                     |
| DOC-07       | Media      | Alta      | Media        | Media                    | Alta                  | La entidad y las especificaciones son verificables, pero la ficha no muestra una fecha documental clara. ([beckman.com][5])                |

---

## 6. Corpus documental seleccionado

| ID documento | Documento seleccionado    | Pregunta asociada | Fragmentos o páginas relevantes                                               | Estado      |
| ------------ | ------------------------- | ----------------- | ----------------------------------------------------------------------------- | ----------- |
| DOC-01       | Palladino et al., 2024    | ALC-02            | Resumen; sección sobre sensores y control de procesos                         | Incorporado |
| DOC-02       | Teworte et al., 2022      | ALC-02            | PDF pp. 10–13; control de pH, sensores, actuadores y alimentación             | Incorporado |
| DOC-03       | Mitra y Murthy, 2022      | ALC-02            | Sección “Brief overview of bioreactor control systems”                        | Incorporado |
| DOC-04       | Rasche, 2020              | ALC-02            | PDF pp. 3, 5 y 10; comparación con matraces, setpoints, sensores y actuadores | Incorporado |
| DOC-05       | Sartorius Biostat B, 2021 | ALC-02            | PDF p. 22; paquetes de 5 L y 10 L, control y sensores                         | Incorporado |
| DOC-06       | Drummen, 2025             | ALC-02            | PDF pp. 1–3; BioLector XT, control de pH, alimentación y gases                | Incorporado |

El corpus es suficiente para formular una definición funcional preliminar, pero no para afirmar una definición regulatoria universal.

---

## 7. Respuesta basada en evidencia

### Evidencia explícita

La definición más sólida recuperada describe a los biorreactores como sistemas controlados para cultivar microorganismos y células. ([MDPI][1])

La evidencia técnica muestra que el control de un biorreactor puede involucrar medición de variables, software o controlador, y acciones sobre actuadores como bombas, dispositivos térmicos, sistemas de gases o agitación.

Los sistemas Sartorius Biostat B de 5 L y 10 L incluyen controlador digital, control de temperatura, pH, DO y velocidad de agitación, además de sensores de temperatura, pH y oxígeno disuelto. ([Sartorius][4])

El BioLector XT, cuando está configurado con el módulo microfluídico descrito en DOC-06, permite control de pH, alimentación abierta o cerrada y regulación de la composición y flujo de gases.

### Inferencia razonable basada en evidencia

Para fines ontológicos, un sistema debería ser considerado candidato a `BioreactorSystem` cuando cumple simultáneamente con estas características mínimas:

1. Posee un espacio o compartimento de cultivo, representable como `CultureCompartment`.
2. Soporta un proceso biológico de cultivo o transformación, representable como `BiologicalCultivationProcess`.
3. Tiene capacidad de establecer, mantener o modificar al menos una condición de proceso relevante, representable como `ProcessControlCapability`.

La tercera condición es la frontera funcional principal frente a un recipiente de cultivo pasivo.

Un matraz, placa o frasco puede ser un `CultureVessel` aunque contenga medio y células. No debería clasificarse automáticamente como `BioreactorSystem` si no existe evidencia de que el sistema, considerado dentro de un límite técnico explícito, controle una condición del cultivo.

Para una ontología orientada a BioLector XT, Sartorius 5 L y Sartorius 10 L, conviene separar tres niveles:

| Nivel candidato                      | Criterio                                                                            |
| ------------------------------------ | ----------------------------------------------------------------------------------- |
| `CultureVessel`                      | Contiene medio, muestra o cultivo, sin capacidad demostrada de control del proceso. |
| `BioreactorSystem`                   | Sistema de cultivo con al menos una capacidad de control de condiciones de proceso. |
| `InstrumentedBioreactorSystem`       | Biorreactor con medición, sensores u observaciones trazables.                       |
| `FeedbackControlledBioreactorSystem` | Biorreactor instrumentado con sensor, controlador, actuador y setpoint.             |

### Información no establecida en el corpus

El corpus no establece que todos los biorreactores deban tener obligatoriamente:

- Agitación mecánica mediante impulsor.
- Aireación con aire u oxígeno.
- Sensor de pH.
- Sensor de DO.
- Control automático en lazo cerrado.
- Alimentación fed-batch.
- Registro electrónico de datos.
- Volumen mínimo.
- Material específico del recipiente.
- Geometría de tanque agitado.

Estas características son frecuentes en Biostat B y en configuraciones avanzadas de BioLector XT, pero deben modelarse como capacidades, configuraciones o especializaciones, no como requisitos universales de la clase raíz `BioreactorSystem`.

---

## 8. Tabla de afirmaciones y evidencia

| ID evidencia | Afirmación                                                                                                  | Tipo de evidencia | Documento       | Página/sección                                | Fragmento o resumen fiel                                                                                          | Confianza | Validación experta |
| ------------ | ----------------------------------------------------------------------------------------------------------- | ----------------- | --------------- | --------------------------------------------- | ----------------------------------------------------------------------------------------------------------------- | --------- | ------------------ |
| EV-01        | Un biorreactor es un sistema controlado para cultivar microorganismos y células.                            | Explícita         | DOC-01          | Resumen                                       | La revisión define los biorreactores como sistemas controlados de cultivo.                                        | Alta      | No                 |
| EV-02        | Sensores y sistemas de control son importantes para mantener condiciones controladas.                       | Explícita         | DOC-01          | Sección 3                                     | El artículo relaciona sensores y control operacional con condiciones controladas y eficiencia del proceso.        | Alta      | No                 |
| EV-03        | Un esquema de control de biorreactor puede integrar sensores, software y actuadores.                        | Explícita         | DOC-04          | PDF p. 5 y p. 10                              | Sensores transmiten información al software; este regula bombas, gases y dispositivos térmicos.                   | Alta      | No                 |
| EV-04        | Los matraces agitados usualmente no controlan el pH del cultivo.                                            | Explícita         | DOC-04          | PDF p. 5                                      | El documento contrasta el ajuste de pH en biorreactor con cultivos en shake flasks.                               | Media     | No                 |
| EV-05        | El control de pH puede seguir una secuencia sensor-controlador-actuador.                                    | Explícita         | DOC-02          | PDF p. 12                                     | El sensor detecta cambio de pH; la unidad de control manda la adición de ácido o base hasta retornar al setpoint. | Alta      | No                 |
| EV-06        | Las condiciones relevantes y estrategias de control dependen de configuración y proceso.                    | Explícita         | DOC-03          | Sección de visión general                     | La revisión indica que el control depende del tipo de biorreactor, biocatalizador y perturbaciones.               | Alta      | No                 |
| EV-07        | Biostat B admite configuraciones de 5 L y 10 L con control de temperatura, pH, DO y velocidad de agitación. | Explícita         | DOC-05          | PDF p. 22                                     | Sartorius lista paquetes de 1, 2, 5 y 10 L con controlador digital y control de esas variables.                   | Alta      | No                 |
| EV-08        | BioLector XT con módulo microfluídico puede controlar pH, alimentación y condiciones gaseosas.              | Explícita         | DOC-06          | PDF pp. 1–3                                   | Beckman describe control de pH, alimentación abierta/cerrada y control de composición y flujo de gases.           | Alta      | No                 |
| EV-09        | El volumen no debe ser requisito universal de clasificación.                                                | Inferida          | DOC-05, DOC-06  | Biostat B 5–10 L; BioLector XT en microescala | Hay evidencia de sistemas llamados biorreactor en escalas de microlitros y litros.                                | Media     | Sí                 |
| EV-10        | Un sensor debe ser obligatorio en todo biorreactor.                                                         | No establecida    | Corpus completo | —                                             | Los documentos muestran sensores como frecuentes y valiosos, pero no prueban obligatoriedad universal.            | Baja      | Sí                 |
| EV-11        | La aireación debe ser obligatoria en todo biorreactor.                                                      | No establecida    | Corpus completo | —                                             | La evidencia incluye cultivo aeróbico, anaeróbico y configuraciones dependientes de la aplicación.                | Baja      | Sí                 |
| EV-12        | Todo biorreactor debe usar control automático en lazo cerrado.                                              | No establecida    | Corpus completo | —                                             | Existen ejemplos de control avanzado, pero no una norma universal de obligatoriedad.                              | Baja      | Sí                 |

La base de las afirmaciones EV-01 a EV-08 está documentada en las fuentes seleccionadas. ([MDPI][1])

---

## 9. Conceptos ontológicos candidatos

| Concepto candidato                   | Tipo sugerido     | Definición basada en evidencia                                                                                               | Fuente asociada | Estado    |
| ------------------------------------ | ----------------- | ---------------------------------------------------------------------------------------------------------------------------- | --------------- | --------- |
| `BioreactorSystem`                   | Clase             | Sistema destinado a cultivar organismos o células bajo condiciones controladas.                                              | DOC-01, DOC-04  | Candidato |
| `CultureVessel`                      | Clase             | Recipiente físico que contiene medio, células u organismos durante cultivo.                                                  | DOC-04, DOC-05  | Candidato |
| `CultureCompartment`                 | Concepto auxiliar | Espacio donde ocurre el cultivo; puede ser tanque, recipiente, pozo o compartimento microfluídico.                           | DOC-05, DOC-06  | Candidato |
| `BiologicalCultivationProcess`       | Clase             | Proceso de crecimiento, mantenimiento o producción biológica en un medio de cultivo.                                         | DOC-01, DOC-04  | Candidato |
| `ProcessParameter`                   | Clase             | Variable relevante para el cultivo, por ejemplo temperatura, pH, DO o velocidad de agitación.                                | DOC-04, DOC-05  | Candidato |
| `ProcessControlCapability`           | Concepto auxiliar | Capacidad del sistema para modificar una condición de proceso hacia una condición deseada.                                   | DOC-02, DOC-04  | Candidato |
| `MonitoringCapability`               | Concepto auxiliar | Capacidad de obtener observaciones de variables del cultivo o del proceso.                                                   | DOC-01, DOC-06  | Candidato |
| `Sensor`                             | Clase             | Dispositivo que mide una variable del proceso, como temperatura, pH o DO.                                                    | DOC-04, DOC-05  | Candidato |
| `Actuator`                           | Clase             | Componente que modifica una condición del proceso, como bomba, sistema de gas o dispositivo térmico.                         | DOC-02, DOC-04  | Candidato |
| `Controller`                         | Clase             | Componente físico o software que recibe señales y determina acciones de control.                                             | DOC-02, DOC-04  | Candidato |
| `ControlLoop`                        | Clase             | Estructura funcional que conecta observación, lógica de control y actuación para mantener una variable cerca de un setpoint. | DOC-02, DOC-04  | Candidato |
| `Setpoint`                           | Concepto auxiliar | Valor objetivo asociado a una variable de proceso controlada.                                                                | DOC-02, DOC-04  | Candidato |
| `FeedbackControlledBioreactorSystem` | Subclase          | Biorreactor instrumentado con sensor, controlador, actuador y control basado en señal.                                       | DOC-02, DOC-06  | Candidato |
| `BioLectorXT`                        | Individuo         | Modelo comercial de microbioreactor de Beckman Coulter Life Sciences.                                                        | DOC-06          | Candidato |
| `BiostatB_5LConfiguration`           | Individuo         | Configuración Biostat B con recipiente de 5 L y capacidades de control documentadas.                                         | DOC-05          | Candidato |
| `BiostatB_10LConfiguration`          | Individuo         | Configuración Biostat B con recipiente de 10 L y capacidades de control documentadas.                                        | DOC-05          | Candidato |
| `hasWorkingVolume`                   | Propiedad de dato | Relaciona una configuración de sistema con su volumen de trabajo.                                                            | DOC-05          | Candidato |

---

## 10. Relaciones ontológicas candidatas

| Relación candidata            | Dominio sugerido   | Rango sugerido                 | Significado                                                                         | Evidencia asociada     | Estado    |
| ----------------------------- | ------------------ | ------------------------------ | ----------------------------------------------------------------------------------- | ---------------------- | --------- |
| `hasCultureCompartment`       | `BioreactorSystem` | `CultureCompartment`           | El sistema dispone de un espacio donde ocurre el cultivo.                           | DOC-04, DOC-05, DOC-06 | Candidato |
| `realizesCultivationProcess`  | `BioreactorSystem` | `BiologicalCultivationProcess` | El sistema ejecuta o soporta un proceso de cultivo.                                 | DOC-01, DOC-04         | Candidato |
| `hasProcessControlCapability` | `BioreactorSystem` | `ProcessControlCapability`     | El sistema puede modificar una condición de proceso.                                | DOC-01, DOC-04         | Candidato |
| `monitorsProcessParameter`    | `BioreactorSystem` | `ProcessParameter`             | El sistema observa una variable relevante del cultivo.                              | DOC-01, DOC-06         | Candidato |
| `usesSensor`                  | `BioreactorSystem` | `Sensor`                       | El sistema utiliza un sensor para obtener mediciones.                               | DOC-04, DOC-05         | Candidato |
| `sendsSignalTo`               | `Sensor`           | `Controller`                   | El sensor transmite una señal al componente de control.                             | DOC-02, DOC-04         | Candidato |
| `commandsActuator`            | `Controller`       | `Actuator`                     | El controlador determina una acción física o digital.                               | DOC-02, DOC-04         | Candidato |
| `regulatesParameter`          | `Actuator`         | `ProcessParameter`             | El actuador modifica una variable de proceso.                                       | DOC-04, DOC-06         | Candidato |
| `hasSetpointFor`              | `ControlLoop`      | `ProcessParameter`             | El bucle de control opera respecto de una condición objetivo.                       | DOC-02, DOC-04         | Candidato |
| `hasWorkingVolume`            | `BioreactorSystem` | `xsd:decimal`                  | Expresa volumen de trabajo o intervalo operativo.                                   | DOC-05                 | Candidato |
| `hasEquipmentConfiguration`   | `BioreactorSystem` | `BioreactorConfiguration`      | Vincula un equipo con una configuración concreta de módulos, sensores y actuadores. | DOC-05, DOC-06         | Candidato |
| `hasOptionalModule`           | `BioreactorSystem` | `EquipmentModule`              | Relaciona un equipo con módulos que cambian sus capacidades.                        | DOC-06                 | Candidato |

---

## 11. Triadas RDF candidatas

| Triada candidata                                                                 | Documento de soporte   | Página o sección                     | Estado                      |
| -------------------------------------------------------------------------------- | ---------------------- | ------------------------------------ | --------------------------- |
| `BioreactorSystem -> realizesCultivationProcess -> BiologicalCultivationProcess` | DOC-01                 | Resumen                              | Soportada                   |
| `BioreactorSystem -> hasProcessControlCapability -> ProcessControlCapability`    | DOC-01, DOC-04         | Resumen; PDF p. 5                    | Soportada                   |
| `BioreactorSystem -> hasCultureCompartment -> CultureCompartment`                | DOC-04, DOC-05, DOC-06 | PDF p. 3; p. 22; método BioLector XT | Parcialmente soportada      |
| `Sensor -> sendsSignalTo -> BioprocessControlSoftware`                           | DOC-04                 | PDF p. 5                             | Soportada                   |
| `BioprocessControlSoftware -> commandsActuator -> Pump`                          | DOC-04                 | PDF p. 10                            | Soportada                   |
| `BioprocessControlSoftware -> commandsActuator -> GassingDevice`                 | DOC-04                 | PDF p. 10                            | Soportada                   |
| `ControlLoop -> hasSetpointFor -> Culture_pH`                                    | DOC-02                 | PDF p. 12                            | Soportada                   |
| `BiostatB_5LConfiguration -> hasNominalVolume -> "5 L"`                          | DOC-05                 | PDF p. 22                            | Soportada                   |
| `BiostatB_10LConfiguration -> hasNominalVolume -> "10 L"`                        | DOC-05                 | PDF p. 22                            | Soportada                   |
| `BiostatB_5LConfiguration -> controlsParameter -> Temperature`                   | DOC-05                 | PDF p. 22                            | Soportada                   |
| `BiostatB_10LConfiguration -> controlsParameter -> DissolvedOxygen`              | DOC-05                 | PDF p. 22                            | Soportada                   |
| `BiostatB_5LConfiguration -> usesSensor -> pHSensor`                             | DOC-05                 | PDF p. 22                            | Soportada                   |
| `BioLectorXT_withMicrofluidicModule -> controlsParameter -> Culture_pH`          | DOC-06                 | PDF p. 1                             | Soportada                   |
| `BioLectorXT_withMicrofluidicModule -> controlsParameter -> GassingComposition`  | DOC-06                 | PDF pp. 2–3                          | Soportada                   |
| `CultureVessel -> rdf:type -> BioreactorSystem`                                  | Corpus completo        | —                                    | Requiere validación experta |

La última triada no debe inferirse automáticamente: un `CultureVessel` puede formar parte de un `BioreactorSystem`, pero no es equivalente al sistema completo.

---

## 12. Sinónimos y variantes terminológicas

| Término principal                    | Sinónimos o variantes documentadas                  | Idioma | Documento de soporte   |
| ------------------------------------ | --------------------------------------------------- | ------ | ---------------------- |
| `Bioreactor`                         | Fermenter                                           | Inglés | DOC-04                 |
| `BioreactorSystem`                   | Bioprocess system, cultivation system               | Inglés | DOC-03, DOC-04         |
| `CultureVessel`                      | Vessel, tank, cultivation chamber                   | Inglés | DOC-04, DOC-05         |
| `DissolvedOxygen`                    | DO, oxygen saturation                               | Inglés | DOC-04, DOC-05, DOC-06 |
| `ProcessControlCapability`           | Process control, control strategy, control system   | Inglés | DOC-02, DOC-03, DOC-04 |
| `Setpoint`                           | Desired setpoint, pH setpoint                       | Inglés | DOC-02, DOC-04         |
| `Microbioreactor`                    | Microscale bioreactor, BioLector XT microbioreactor | Inglés | DOC-02, DOC-06         |
| `FeedbackControlledBioreactorSystem` | Closed-loop control, feedback control               | Inglés | DOC-02, DOC-06         |

DOC-04 indica que “bioreactor” y “fermenter” se usan de forma prácticamente equivalente, con diferencias habituales de contexto disciplinar.

---

## 13. Vacíos, riesgos y decisiones pendientes

1. **Frontera del sistema:** debe definirse si un matraz dentro de incubador-agitador será modelado solo como `CultureVessel` o como parte de un `ControlledCultivationSystem`.

2. **Control manual versus automático:** el corpus demuestra control por software y lazo cerrado, pero no define si un ajuste manual programado basta para clasificar un sistema como biorreactor.

3. **Sensor como requisito mínimo:** la evidencia muestra que sensores son centrales en sistemas instrumentados, pero no prueba que todo biorreactor deba incorporar uno.

4. **Configuración específica del BioLector XT:** las capacidades de pH, alimentación y gases dependen de módulo microfluídico, placas, tapas de gaseado y módulos opcionales.

5. **Modelo Sartorius exacto:** la evidencia encontrada corresponde a Biostat B. Debe verificarse si los equipos del proyecto son exactamente Biostat B, Biostat B-DCU u otra configuración Sartorius de 5 L y 10 L.

6. **Asepsia, esterilidad, contención y seguridad:** son importantes para operación real, pero no se identificaron como requisitos definitorios universales en el corpus seleccionado.

7. **Alarmas, eventos y calidad de datos:** pertenecen al alcance general de la ontología, pero requieren manuales, SOPs o URS específicos para modelarse con evidencia.

8. **Normativa universal:** la búsqueda no recuperó una norma ISO o ASTM transversal que defina biorreactor de cultivo para todas las escalas. ISO 11074:2025 fue excluida porque su definición pertenece a biotratamiento de sólidos y calidad de suelos. ([ISO][6])

### Documentos adicionales recomendados

- Manual oficial del modelo exacto de Sartorius instalado.
- Manual oficial completo del BioLector XT y de los módulos instalados.
- SOPs de operación, calibración, limpieza y mantenimiento.
- Esquemas P&ID o diagramas de conexiones.
- Registros de alarmas, recetas de control y listas de sensores.
- URS, IQ/OQ/PQ o documentación de cualificación, si existe.

---

## 14. Registro metodológico para el documento de investigación

La pregunta ALC-02 examinó las características mínimas necesarias para distinguir un sistema de biorreacción de un recipiente de cultivo. Se realizó una búsqueda documental focalizada en definiciones de biorreactor, control de bioprocesos, microbioreactores y sistemas de sobremesa de 5 L y 10 L. La selección priorizó revisiones revisadas por pares y documentación oficial de fabricantes. Se incorporaron seis documentos al corpus: tres revisiones científicas, un documento técnico comparativo de Eppendorf, una brochure oficial de Sartorius Biostat B y una application note oficial de Beckman Coulter Life Sciences para BioLector XT. La evidencia recuperada permite proponer, de forma preliminar, que un `BioreactorSystem` debe representar un sistema de cultivo con capacidad de controlar al menos una condición relevante del proceso, diferenciándose así de un `CultureVessel` pasivo. Se identificaron conceptos candidatos como `BioreactorSystem`, `CultureCompartment`, `ProcessParameter`, `Sensor`, `Actuator`, `Controller` y `ControlLoop`, junto con relaciones candidatas para representar control, monitorización, setpoints y configuraciones de equipo. La principal limitación es la ausencia de una definición regulatoria universal recuperada en el corpus; por tanto, la clasificación propuesta requiere validación experta y contraste con los manuales y configuraciones reales de los equipos del proyecto.

---

## 15. Estado final

- **Nivel de confianza general:** Medio-Alto.
- **Estado de la respuesta:** Parcialmente soportada.
- **Estado del corpus:** Suficiente para una definición funcional preliminar; parcial para una definición normativa universal.
- **Próxima acción recomendada:** Validar con un experto en bioprocesos la regla operativa propuesta y revisar los manuales oficiales de las configuraciones reales de BioLector XT, Sartorius 5 L y Sartorius 10 L antes de convertir las clases y relaciones candidatas en axiomas OWL definitivos.

[1]: https://www.mdpi.com/2076-3417/14/20/9346 "Bioreactors: Applications and Innovations for a Sustainable and Healthy Future—A Critical Review | MDPI"
[2]: https://discovery.ucl.ac.uk/id/eprint/10194388/ "
       Recent advances in fed-batch microscale bioreactor design 
      -
      UCL Discovery
    "
[3]: https://journal.hep.com.cn/smab/EN/1160583959287488586 "
        Bioreactor control systems in the biopharmaceutical industry: a critical perspective
    "
[4]: https://www.sartorius.com/download/34576/broch-biostat-b-sbi1513-e-1--data.pdf "Biostat® B Multi-talented bioreactor"
[5]: https://www.beckman.com/resources/reading-material/product-instructions/biolector-xt-technical-data-sheet "BioLector XT Technical Data Sheet"
[6]: https://www.iso.org/obp/ui/en/?utm_source=chatgpt.com "ISO 11074:2025(en), Soil quality — Vocabulary"
