1. **ID y pregunta**

**ALC-02:** ¿Qué características mínimas debe tener un sistema para ser considerado biorreactor y no solo un recipiente de cultivo?

2. **Respuesta basada en evidencia**

Según los fragmentos suministrados, un biorreactor se describe no solo como contenedor, sino como aparato que:

- es un "apparatus used to carry out any kind of bioprocess" [SRC-001]
- es "a device, vessel, or system... provide a controlled environment for optimal cell growth" [SRC-002]
- tiene como propósito "provide a suitable and regulated environment" [SRC-003]
- es "Easy to monitor and/or control reaction parameters (such as dissolved oxygen concentration, pH, temperature, agitation rate, redox value, and so on)" [SRC-004]
- requiere que "Dissolved oxygen concentration, pH, temperature, mixing, and supplementation of nutrients all need to be controlled and optimized" [SRC-005]
- opera "under tightly controlled conditions" [SRC-006]
- integra "Sensors... monitor key process parameters, including pH, dissolved oxygen and temperature continuously in real-time" [SRC-007], "Control software... calculates the adjustments... to maintain parameter levels within their specified setpoint" [SRC-008] y "Actuators... pumps, valves, or motors, that adjust the parameter back to its specified setpoint" [SRC-009]
- en ejemplos concretos, dispone de "OXYGEN OPTODES 0 – 100 % dissolved oxygen", "pH OPTODES pH 4 – 7.5" y "TRIGGERED pH CONTROL (CLOSED LOOP CONTROLLER)" [SRC-010][SRC-011][SRC-012]
- se usa "under controlled and reproducible conditions" y "forms the interface between the culture vessel and the measurement and control system" [SRC-013][SRC-015]
- se distingue de sistemas estáticos porque "require... the ability to monitor and control culture parameters, which cannot be accomplished in traditional static culture systems" [SRC-016] y "allow the implementation of culture monitoring and control systems... by adjusting feeding regimes and physicochemical parameters (e.g., O2 concentration and pH) according to real-time culture measurements" [SRC-017]

**No establecido en el corpus suministrado:** una lista normativa cerrada y mínima (por ejemplo, número exacto de parámetros o si el control debe ser obligatoriamente en lazo cerrado). El corpus describe características recurrentes pero no las fija como requisitos mínimos formales.

3. **Tabla de afirmaciones y evidencia**

| Afirmación                                                                                                     | Fragmento                                                                                                                                                                                                       | Fuente                       | Concepto/Relación/Triada candidata                      | Tipo evidencia | Confianza | Validación experta                            |
| -------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------- | ------------------------------------------------------- | -------------- | --------- | --------------------------------------------- |
| Un biorreactor es un aparato para bioprocesos                                                                  | "An apparatus used to carry out any kind of bioprocess; examples include fermenter or enzyme reactor."                                                                                                          | SRC-001 – definición         | Bioreactor subClassOf Apparatus                         | explícita      | alta      | no                                            |
| Es un dispositivo que provee entorno controlado                                                                | "provide a controlled environment for optimal cell growth or product synthesis"                                                                                                                                 | SRC-002 – 7.1.1              | Bioreactor provides ControlledEnvironment               | explícita      | alta      | no                                            |
| Su propósito es entorno adecuado y regulado                                                                    | "provide a suitable and regulated environment"                                                                                                                                                                  | SRC-003 – 7.1.2              | Bioreactor hasPurpose RegulatedEnvironment              | explícita      | alta      | no                                            |
| Debe poder monitorizar y/o controlar parámetros (DO, pH, temperatura, agitación, redox)                        | "Easy to monitor and/or control reaction parameters (such as dissolved oxygen concentration, pH, temperature, agitation rate, redox value, and so on)"                                                          | SRC-004 – 7.1.2              | Bioreactor monitorsOrControls ProcessParameter          | explícita      | alta      | sí (¿monitorizar basta o se exige controlar?) |
| Es necesario controlar DO, pH, temperatura, mezcla y nutrientes                                                | "Dissolved oxygen concentration, pH, temperature, mixing, and supplementation of nutrients all need to be controlled and optimized"                                                                             | SRC-005 – Introducción       | Bioreactor controls ProcessParameter                    | explícita      | alta      | sí (¿todos son mínimos?)                      |
| Opera bajo condiciones estrechamente controladas                                                               | "under tightly controlled conditions"                                                                                                                                                                           | SRC-006 – definición         | Bioreactor operatesUnder TightlyControlledConditions    | explícita      | alta      | no                                            |
| Incluye sensores que monitorizan pH, DO y temperatura en tiempo real                                           | "Sensors: These monitor key process parameters, including pH, dissolved oxygen and temperature continuously in real-time"                                                                                       | SRC-007 – componentes        | Bioreactor hasComponent Sensor                          | explícita      | alta      | no                                            |
| Incluye software que calcula ajustes para mantener setpoint                                                    | "Control software... calculates the adjustments... to maintain parameter levels within their specified setpoint"                                                                                                | SRC-008 – componentes        | Bioreactor hasComponent ControlSoftware                 | explícita      | alta      | no                                            |
| Incluye actuadores (bombas, válvulas, motores) regulados por software                                          | "Actuators... pumps, valves, or motors, that adjust the parameter back to its specified setpoint"                                                                                                               | SRC-009 – componentes        | Bioreactor hasComponent Actuator                        | explícita      | alta      | no                                            |
| Ejemplo BioLector mide DO 0-100%                                                                               | "OXYGEN OPTODES 0 – 100 % dissolved oxygen"                                                                                                                                                                     | SRC-010                      | BioLectorXT hasSensor OxygenOptode                      | explícita      | alta      | no                                            |
| Ejemplo BioLector mide pH 4-7.5                                                                                | "pH OPTODES pH 4 – 7.5 (depending on plate)"                                                                                                                                                                    | SRC-011                      | BioLectorXT hasSensor pHOptode                          | explícita      | alta      | no                                            |
| Ejemplo BioLector tiene control pH en lazo cerrado                                                             | "TRIGGERED pH CONTROL (CLOSED LOOP CONTROLLER)"                                                                                                                                                                 | SRC-012                      | BioLectorXT implements ClosedLoopControl                | explícita      | alta      | no                                            |
| Sartorius cultiva bajo condiciones controladas y reproducibles                                                 | "under controlled and reproducible conditions"                                                                                                                                                                  | SRC-013 – Intended Use       | Bioreactor provides ControlledAndReproducibleConditions | explícita      | alta      | no                                            |
| Sartorius forma interfaz con sistema de medición y control                                                     | "forms the interface between the culture vessel and the measurement and control system (DCU system)"                                                                                                            | SRC-015 – Device Description | Bioreactor hasInterface MeasurementAndControlSystem     | explícita      | alta      | no                                            |
| La capacidad de monitorizar y controlar distingue de sistemas estáticos                                        | "ability to monitor and control culture parameters, which cannot be accomplished in traditional static culture systems"                                                                                         | SRC-016 – Discusión          | Bioreactor distinguishesFrom StaticCultureSystem        | explícita      | alta      | no                                            |
| Permite implementar monitorización y control ajustando alimentación y parámetros según medición en tiempo real | "allow the implementation of culture monitoring and control systems... by adjusting feeding regimes and physicochemical parameters (e.g., O2 concentration and pH) according to real-time culture measurements" | SRC-017 – Discusión          | Bioreactor implements MonitoringAndControlSystem        | explícita      | alta      | no                                            |
| Un recipiente de cultivo sin estas capacidades no es biorreactor                                               | No establecido en el corpus suministrado (inferencia a partir de SRC-016)                                                                                                                                       | —                            | —                                                       | inferida       | baja      | sí                                            |

4. **Conceptos candidatos**

- Bioreactor
- Apparatus
- ControlledEnvironment
- SuitableAndRegulatedEnvironment
- TightlyControlledConditions
- ProcessParameter (DO, pH, Temperature, AgitationRate, RedoxValue, Mixing, NutrientSupplementation)
- Sensor
- ControlSoftware
- Actuator
- MeasurementAndControlSystem
- ClosedLoopController
- StaticCultureSystem
- CultureVessel

5. **Relaciones candidatas con dominio y rango sugeridos**

| Relación           | Dominio    | Rango                       | Basado en        |
| ------------------ | ---------- | --------------------------- | ---------------- |
| provides           | Bioreactor | ControlledEnvironment       | SRC-002, SRC-003 |
| monitorsOrControls | Bioreactor | ProcessParameter            | SRC-004          |
| controls           | Bioreactor | ProcessParameter            | SRC-005          |
| operatesUnder      | Bioreactor | TightlyControlledConditions | SRC-006          |
| hasComponent       | Bioreactor | Sensor                      | SRC-007          |
| hasComponent       | Bioreactor | ControlSoftware             | SRC-008          |
| hasComponent       | Bioreactor | Actuator                    | SRC-009          |
| implements         | Bioreactor | ClosedLoopController        | SRC-012          |
| hasInterface       | Bioreactor | MeasurementAndControlSystem | SRC-015          |
| distinguishesFrom  | Bioreactor | StaticCultureSystem         | SRC-016          |

6. **Triadas RDF candidatas**

- Bioreactor -> rdf:type -> Apparatus — [SRC-001]
- Bioreactor -> provides -> ControlledEnvironment — [SRC-002]
- Bioreactor -> hasPurpose -> SuitableAndRegulatedEnvironment — [SRC-003]
- Bioreactor -> monitorsOrControls -> ProcessParameter — [SRC-004]
- Bioreactor -> controls -> DissolvedOxygen — [SRC-005]
- Bioreactor -> operatesUnder -> TightlyControlledConditions — [SRC-006]
- Bioreactor -> hasComponent -> Sensor — [SRC-007]
- Bioreactor -> hasComponent -> ControlSoftware — [SRC-008]
- Bioreactor -> hasComponent -> Actuator — [SRC-009]
- BioLectorXT -> hasSensor -> OxygenOptode — [SRC-010]
- BioLectorXT -> implements -> ClosedLoopController — [SRC-012]
- SartoriusBiostat -> provides -> ControlledAndReproducibleConditions — [SRC-013]

7. **Sinónimos documentados**

| Término    | Sinónimo/variante | Fuente  |
| ---------- | ----------------- | ------- |
| bioreactor | fermenter         | SRC-001 |
| bioreactor | enzyme reactor    | SRC-001 |
| bioreactor | device            | SRC-002 |
| bioreactor | vessel            | SRC-002 |
| bioreactor | system            | SRC-002 |

8. **Vacíos del corpus**

- No establece lista mínima obligatoria de parámetros (¿basta uno o se requieren varios?).
- No define si "monitorizar y/o controlar" significa que monitorizar solo es suficiente.
- No especifica si el control debe ser automático en lazo cerrado o si ajuste manual califica.
- No proporciona umbral que separe formalmente "recipiente de cultivo" de "biorreactor" más allá de la capacidad de monitorizar/controlar.
- No menciona requisitos de esterilidad, escalabilidad o reproducibilidad como mínimos (solo aparecen como propósitos).

9. **Estado final**

- **Soportado / parcialmente soportado / no soportado:** parcialmente soportado
- Justificación: el corpus describe de forma explícita múltiples características asociadas (entorno controlado, sensores, software, actuadores, capacidad de monitorizar y controlar), pero no establece normativamente cuáles son mínimas e indispensables para distinguir un biorreactor de un simple recipiente.
