# LLM-driven Ontology Construction for Bioprocesses 

## Contributing Members

**Team Participants**: 
|Name     |  Email   |  LinKedIn   |
|---------|-----------------|-----------------|
|[Anderson Daniel Pipicano Ruiz](https://github.com/[Pipicano25])| @Pipicano25 | [Anderson Daniel Pipicano Ruiz](https://www.linkedin.com/in/anderson-daniel-pipicano-ruiz/) |
|[Sandra Jimena Orozco Lagos](https://github.com/[Sandrajol]) | @Sandrajol | |

**Instructor**: 
|Name     |  Email   |  LinKedIn   |
|---------|-----------------|-----------------|
|[Alexander Astudillo](https://github.com/[AlexanderAstudillo])| @AlexanderAstudillo |  |

## Project Intro
The main goal of this project is to develop a multi-scale bioprocess ontology covering micro/mini
bioreactors, lab-scale, pilot-scale, and industrial-scale bioreactors, using at least three Large Language 
Models (LLMs) as ontology generation assistants. The ontology will provide a shared, machine
interpretable representation of key bioprocess entities and relations (e.g., bioreactor systems, process 
phases, sensors, actuators, operating variables, events), enabling consistent terminology and 
knowledge reuse across scales. 

First, the project will establish clear ontology requirements by defining the scope and writing a set of 
competency questions focused on cross-scale bioreactor scenarios. These questions will guide what 
the ontology must be able to represent and answer in practice, for instance, how to describe which 
variables are measured or controlled at each scale, how instruments differ between scales, and how 
equivalent concepts (such as dissolved oxygen measured by different technologies) should be mapped 
consistently. 

Second, the project will apply a comparative LLM-driven workflow. Using a curated bioprocess corpus 
(e.g., technical documentation, SOPs, variable dictionaries, and relevant scientific literature), three 
LLMs will be prompted under the same conditions to generate three candidate ontologies, each 
proposing concepts, taxonomies, and relations. These candidates will then be consolidated into a 
single OWL ontology through systematic harmonization: deduplication of overlapping concepts, 
normalization of naming conventions, resolution of synonyms, and alignment of relations and basic 
constraints (e.g., domain/range where appropriate). 

Finally, the ontology will incorporate explicit multi-scale modeling, including bioreactor scale as a first
class concept and representations of sensor/actuator availability and variable equivalences across 
scales. The resulting ontology will be iteratively validated and refined with domain experts, ensuring 
conceptual correctness, coherence, and practical utility. The final deliverables will include the expert
validated OWL ontology, brief documentation of scope and modeling decisions, and a change log 
summarizing the evolution from the LLM-generated candidates to the final version. 

## Project Objective
The main goal of this project is to develop a multi-scale bioprocess ontology (micro/mini, lab, pilot, industrial bioreactors) using at least three LLMs.

* Define the ontology scope and a set of competency questions focused on bioreactors across 
scales.
* Generate three candidate ontologies (one per LLM) from a curated bioprocess corpus. 
* Consolidate the candidates into a single OWL ontology, harmonizing concepts, relations, and 
terminology. 
* Include explicit modeling of bioreactor scale, sensor/actuator availability, and variable 
equivalences across scales. 
* Validate and refine the ontology with domain experts, delivering a final version and brief 
documentation.  

### Technologies
* Ontology engineering (OWL/RDF, Protégé, classes/properties/axioms)
* LLMs (prompting, evaluation, reproducibility)
* Python (e.g., parsing corpus, term extraction, normalization)
