# Estructura del proyecto

```text
LLM-driven-Ontology-Construction-for-Bioprocesses-/
│
├── docs/                                                       # Documentación académica y entregables
│   ├── presentation/                                           # Material para la presentación/artículo del proyecto
│   │   └── LLM-driven-Ontology-Construction-for-Bioprocesses.pptx
│   │
│   ├── important/                                              # Plantillas institucionales y material de apoyo
│   │
│   ├── proposal/                                               # Propuesta de proyecto
│   │   ├── references/                                         # Referencias del proyecto
│   │   └── LLMs4Ont.pdf
│   │
│   ├── deliverables/                                           # Evidencias organizadas por objetivo del proyecto
│   │   ├── objective-1/                                        # Alcance y preguntas de competencia
│   │   └── objective-2/                                        # Corpus y selección de LLMs
│   │
│   ├── state_of_the_art/                                       # Literatura y antecedentes científicos
│
├── ontology workflow/                                          # Representación visual del flujo de trabajo ontológico
│   ├── ontology workflow.drawio                                # Archivo fuente editable en draw.io
│   └── ontology workflow-Página-2.drawio.png                   # Exportación del diagrama
│
├── row_data/                                                   # Insumos del flujo de construcción ontológica
│   ├── corpus/                                                 # Material organizado por LLM y unidad ALC
│   │
│   └── promts/                                                 # Plantillas de prompts del flujo experimental
│
├── .gitignore                                                  # Archivos y carpetas excluidos del control de versiones
├── README.md                                                   # Descripción general, objetivos y tecnologías del proyecto
└── project_structure.md                                        # Este documento
```

## Organización funcional

- **`Docs/`** concentra las evidencias académicas: propuesta, revisión del estado del arte, rúbrica, entregables de los objetivos y material de presentación.
- **`ontology workflow/`** conserva el diagrama editable y su exportación; debe actualizarse cuando cambie el proceso metodológico.
- **`row_data/corpus/`** separa los insumos o resultados por LLM (`Claude_Sonnet`, `GPT-4o` y `Llama_3`) y por carpeta `ALC-01` a `ALC-08`, facilitando la comparación reproducible entre modelos.
- **`row_data/promts/`** contiene los prompts usados para planear el corpus y ejecutar la extracción condicionada por evidencia documental.

> **Nota sobre nomenclatura:** `row_data/` y `promts/` son los nombres actuales de las rutas versionadas. Aunque podrían interpretarse como `raw_data/` y `prompts/`, no deben renombrarse sin actualizar previamente los enlaces, scripts y documentación que los referencien.
