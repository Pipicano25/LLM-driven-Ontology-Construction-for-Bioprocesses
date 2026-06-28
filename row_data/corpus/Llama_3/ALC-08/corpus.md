1. **ID y pregunta**

- **ID:** ALC-08
- **Pregunta:** ¿Qué conceptos deben quedar fuera del alcance inicial para evitar que la ontología sea demasiado amplia?

2. **Respuesta basada en evidencia**

El corpus suministrado no contiene una lista explícita de conceptos a excluir.

**Evidencia explícita:**

- La ontología "should provide coverage for the area it claims to describe"
- El alcance se define como "extent of the domain or subject matter it intends to cover"
- Un módulo "should be as small as possible"

Los únicos elementos de dominio mencionados son:

- Temperatura, velocidad de agitación, optodos de oxígeno y pH
- Contactos de alarma y puerto Ethernet host para sistema externo ej. MFCS SCADA

**Inferencia razonable:** para cumplir con los principios anteriores, el alcance inicial debe limitarse a esos elementos.

**No establecido en el corpus suministrado:** nombres concretos de conceptos a excluir (p. ej., downstream, ERP, biología molecular) porque no aparecen en los fragmentos.

3. **Tabla de afirmaciones y evidencia**

| Afirmación                                     | Fragmento de evidencia                                                                                                                                      | Fuente y sección                | Concepto/relación/triada candidata                     | Tipo evidencia | Confianza | Validación experta |
| ---------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------- | ------------------------------------------------------ | -------------- | --------- | ------------------ |
| La ontología debe cubrir un dominio específico | "Rule 1: The Ontology Should Be about a Specific Domain of Knowledge Specifically, an ontology should provide coverage for the area it claims to describe." | SRC-003, Rule 1                 | Ontology -> shouldProvideCoverageFor -> SpecificDomain | Explícita      | Alta      | No                 |
| Alcance = extensión del dominio                | "P5) Scope - extent of the domain or subject matter it intends to cover."                                                                                   | SRC-004, P5                     | Ontology -> hasScope -> Scope                          | Explícita      | Alta      | No                 |
| Módulo debe ser lo más pequeño posible         | "Size: A module M i (O) of an ontology O should be as small as possible."                                                                                   | SRC-005, Section 2.3            | Module -> hasSizeConstraint -> Minimal                 | Explícita      | Alta      | No                 |
| Reutilización parcial es importante            | "Partial Reuse: ... reuse emerges as an important issue."                                                                                                   | SRC-005, Section 2.2            | Ontology -> supports -> PartialReuse                   | Explícita      | Alta      | No                 |
| Equipo incluye temperatura 10–50°C             | "TEMPERATURE 10 – 50 °C (min. temp.: 8 °C below ambient temp.)"                                                                                             | SRC-001, Cultivation conditions | Equipment -> hasTemperatureRange -> "10-50°C"          | Explícita      | Alta      | No                 |
| Equipo incluye agitación 100–1500 rpm          | "SHAKING SPEED 100 – 1500 rpm (3 mm diameter)"                                                                                                              | SRC-001                         | Equipment -> hasShakingSpeed -> "100-1500 rpm"         | Explícita      | Alta      | No                 |
| Equipo incluye optodos de oxígeno 0–100%       | "OXYGEN OPTODES 0 – 100 % dissolved oxygen\*1"                                                                                                              | SRC-001                         | Equipment -> hasOxygenOptodeRange -> "0-100%"          | Explícita      | Alta      | No                 |
| Equipo incluye optodos pH 4–7.5                | "pH OPTODES pH 4 – 7.5 (depending on plate)"                                                                                                                | SRC-001                         | Equipment -> hasPHOptodeRange -> "4-7.5"               | Explícita      | Alta      | No                 |
| BIOSTAT incluye contactos de alarma            | "Com Alarm Potential-free alarm contacts (X23) When an alarm triggers..."                                                                                   | SRC-002, Page 19                | BiostatSystem -> hasComponent -> ComAlarm              | Explícita      | Alta      | No                 |
| BIOSTAT incluye puerto host para MFCS SCADA    | "Host Ethernet port for an external host system e .g ., MFCS SCADA"                                                                                         | SRC-002, Page 19                | BiostatSystem -> connectsTo -> MFCS_SCADA              | Explícita      | Alta      | No                 |
| Lista específica de conceptos a excluir        | No establecido en el corpus suministrado                                                                                                                    | —                               | —                                                      | No establecida | Baja      | Sí                 |

4. **Conceptos candidatos**

- Ontology
- SpecificDomain
- Scope
- Module
- Temperature
- ShakingSpeed
- OxygenOptode
- pHOptode
- ComAlarm
- PotentialFreeAlarmContact
- Host
- EthernetPort
- MFCS_SCADA

5. **Relaciones candidatas con dominio y rango sugeridos**

| Relación                 | Dominio sugerido | Rango sugerido | Basado en |
| ------------------------ | ---------------- | -------------- | --------- |
| shouldProvideCoverageFor | Ontology         | SpecificDomain | SRC-003   |
| hasScope                 | Ontology         | Scope          | SRC-004   |
| hasSizeConstraint        | Module           | MinimalSize    | SRC-005   |
| supports                 | Ontology         | PartialReuse   | SRC-005   |
| hasTemperatureRange      | Equipment        | xsd:string     | SRC-001   |
| hasShakingSpeed          | Equipment        | xsd:string     | SRC-001   |
| hasOxygenOptodeRange     | Equipment        | xsd:string     | SRC-001   |
| hasPHOptodeRange         | Equipment        | xsd:string     | SRC-001   |
| hasComponent             | BiostatSystem    | ComAlarm       | SRC-002   |
| connectsTo               | BiostatSystem    | MFCS_SCADA     | SRC-002   |

6. **Triadas RDF candidatas**

- Ontology -> shouldProvideCoverageFor -> SpecificDomain (SRC-003)
- Ontology -> hasScope -> Scope (SRC-004)
- Module -> hasSizeConstraint -> "as small as possible" (SRC-005)
- Equipment -> hasTemperatureRange -> "10 – 50 °C" (SRC-001)
- Equipment -> hasShakingSpeed -> "100 – 1500 rpm" (SRC-001)
- Equipment -> hasOxygenOptodeRange -> "0 – 100 %" (SRC-001)
- Equipment -> hasPHOptodeRange -> "pH 4 – 7.5" (SRC-001)
- BiostatSystem -> hasComponent -> ComAlarm (SRC-002)
- BiostatSystem -> connectsTo -> MFCS_SCADA (SRC-002)

7. **Sinónimos documentados**

- No establecido en el corpus suministrado (los fragmentos no listan sinónimos)

8. **Vacíos del corpus**

- No hay lista de conceptos a excluir explícitamente
- No hay mención de escalas 5 L / 10 L, equivalencias funcionales, fases de proceso, eventos o muestras
- No hay definiciones de "dominio específico" para biorreactores multi-escala
- No hay criterios para decidir qué queda fuera más allá de "ser pequeño" y "cubrir el área reclamada"
- No hay sinónimos ni relaciones jerárquicas

9. **Estado final**

- **Soportado / parcialmente soportado / no soportado:** Parcialmente soportado
  - Principios de limitación de alcance están soportados explícitamente
  - La lista concreta de conceptos a excluir no está soportada (no establecida en el corpus)
