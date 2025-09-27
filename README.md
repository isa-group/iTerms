# iTerms

**iTerms** is an approach designed to translate natural language Terms of Service (ToS) into the Terms of Service Language ([**TOSL**](https://w3id.org/tosl/)) model using LLMs. The core idea is to guide the construction of a knowledge graph through a structured, multi-phase process that progressively transforms unstructured legal text into a formal representation.

## Repository Structure
`data/`
A collection of real use cases and their expected labels derived from an actual agreement.
- `use_cases_elsevier.json`: original dataset divide in use cases in natural language.  
- `use_cases_elsevier_classifieds_expected.json`: expected labels and classifications used as ground truth for evaluation.

`experiment1/`
The first experimental cycle of the **iTerms** pipeline.  

- `phase1/`, `phase2/`, `phase3/`: represent the progressive stages of the pipeline (extraction, TOSL modeling, self-correction).  
- `iTerms_experiment1.ipynb`: main notebook orchestrating the full pipeline for this experiment.

`experiment2/`
The second experimental cycle, with variations in prompts, LLM configurations, or extraction strategies.  

- The structure is identical to `experiment1` to facilitate result comparisons.  
- `iTerms_experiment2.ipynb`: main notebook for the second experiment.


`experiment3/`
The third experimental cycle with variations in the extraction strategies.  

- In this case, `phase1/` is omitted because the output from previous experiments is reused or the pipeline is adapted.  
- `phase2/` and `phase3/` corresponding stages of the pipeline.  
- `iTerms_experiment3.ipynb`: main notebook for the third experiment.

`metamodel/`
Metamodel resources including a rule construction guide using TOSL and a simplified TOSL/ODRL ontology.

## Methodology

The iTerms approach follows a **multi-phase pipeline** that transforms legal text in natural language into formal ([**TOSL**](https://w3id.org/tosl/)) representations through three main phases:

1. **Metadata Extraction** – Identifies key elements (deontic modality, action, party, asset) required to build TOSL rules.  
2. **Initial Representation** – Uses LLMs to generate a knowledge graph in TOSL based on extracted metadata, ontology concepts, and modeling guidelines.  
3. **Auto-correction** – Checks and fixes syntactic or semantic errors in the TTL/TOSL representation, producing a final, valid graph.


## iTerms Example Use Case


