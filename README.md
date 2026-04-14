# QAI Lab Research Core

A modular, agent-agnostic research operating system for QAI Lab. This repository is the backbone for high-leverage, standards-driven research automation—enabling rigorous literature synthesis, gap identification, experiment design, dataset QA, analysis, and publication development.

## Purpose
To provide a reusable, auditable, and extensible system of research reasoning modules (skills) that operate consistently across agent environments (Copilot, Codex, Claude Code, Gemini, Kiro, OpenClaw, and others).

**This repository is distinct from:**
- `qai-research-domains`: domain-specific research assets and ontologies
- `qai-publication-suite`: manuscript production and submission tools
- `qai-experiment-ops`: experiment execution and data pipeline management

## What is a "Skill"?
A skill is a structured reasoning module—not just a workflow formatter. Each skill:
- Frames research problems and surfaces assumptions
- Evaluates evidence and generates multiple candidate paths
- Identifies tradeoffs, risks, and unresolved questions
- Produces explicit, auditable outputs for downstream skills
- Preserves uncertainty and decision logic for later review
- Follows shared standards for prompts, outputs, and evaluation
- Is portable across agent systems

## Expected Outputs
- Executive summaries and structured core outputs
- Explicit assumptions, limitations, and risk registers
- Tradeoff matrices and decision tables where relevant
- Machine-readable handoff blocks for downstream skills
- Evidence-backed claims, with clear distinction from inference or recommendation
- Error and limitation reporting

## Shared Standards
All skills reference and comply with:
- `standards/skill-spec-template.md`: skill definition format (with reasoning, tradeoff, and handoff requirements)
- `standards/output-contracts.md`: output structure, rigor, and downstream interoperability
- `standards/prompt-style-guide.md`: prompt writing for portability and reasoning depth
- `standards/evaluation-checklist.md`: review and validation for reasoning quality
- `shared/`: reusable research templates, rubrics, and glossaries

## Repository Structure
- `standards/`: Skill specs, prompt guides, output contracts, evaluation checklists
- `shared/`: Templates, rubrics, glossaries, reusable research assets
- `skills/`: Each core skill in its own folder (see SKILLS_INDEX.md)
- `examples/`: Domain-specific usage examples

## Core Skills and Academic Use Cases

This section explains how each core skill can be used by students, graduate researchers, academic labs, and technical research teams across STEM and academic fields. Each skill is designed to support rigorous, auditable research work in real-world academic and interdisciplinary settings.

### Literature Review
Synthesizes academic papers, clusters evidence by methodology, maps consensus and disagreement, and identifies recurring limitations. 

**Who might use this:**
- PhD students conducting systematic reviews
- Undergraduate or master's students preparing thesis backgrounds
- Faculty or lab teams scoping new research directions

**Example use cases:**
- A rehabilitation science student synthesizing RCTs on stroke interventions
- A computer vision researcher comparing segmentation methods across datasets
- A public health student summarizing intervention studies for a capstone

### Gap Finder
Moves from "what is known" to "what is missing" by identifying actionable research gaps, ranking them by novelty, feasibility, and impact, and generating candidate research questions.

**Who might use this:**
- Graduate students seeking thesis topics
- Faculty planning grant proposals
- Interdisciplinary teams mapping new research areas

**Example use cases:**
- Identifying under-studied populations in biomechanics
- Spotting missing validation studies in machine learning benchmarks
- Finding publishable directions for a psychology thesis

### Experiment Design
Turns research questions into structured, reproducible studies with explicit variables, controls, alternative designs, and tradeoff analysis.

**Who might use this:**
- Psychology students designing cognitive experiments
- Engineering students planning validation studies
- Biomechanics labs preparing pilot protocols

**Example use cases:**
- Designing a repeated-measures study for gait analysis
- Planning a pilot for a new wearable sensor in neuroperformance
- Structuring a validation study for a new computer vision algorithm

### Protocol Writer
Formalizes methods into reproducible, auditable procedures, distinguishing required vs. optional steps and surfacing operational risks.

**Who might use this:**
- Clinical researchers preparing IRB-ready protocols
- Lab managers writing SOPs
- Students preregistering studies

**Example use cases:**
- Drafting a protocol for a multi-site clinical trial
- Creating a preregistration-ready procedure for a cognitive science experiment
- Writing a standard operating procedure for a rehabilitation lab

### Dataset Schema Designer
Defines dataset fields, metadata, validation rules, provenance, and harmonization requirements for robust, FAIR-compliant data.

**Who might use this:**
- Biomedical engineers planning sensor datasets
- Clinical researchers designing spreadsheets for outcomes
- Environmental scientists harmonizing multi-site data

**Example use cases:**
- Creating a schema for a wearable sensor dataset in biomechanics
- Designing metadata and validation for a clinical outcomes spreadsheet
- Planning harmonization rules for a multi-site environmental study

### Dataset QA
Assesses dataset quality, detects missing data, inconsistencies, schema drift, harmonization issues, and readiness for analysis.

**Who might use this:**
- Public health researchers cleaning longitudinal datasets
- Biomechanics labs exporting motion capture data
- Clinical teams preparing outcomes tables for analysis

**Example use cases:**
- Detecting schema drift in a multi-year clinical registry
- Identifying harmonization issues in a multi-sensor motion capture export
- Flagging missing or inconsistent data in a public health survey

### Feature Engineering
Defines meaningful variables for analysis and modeling, separating raw, derived, domain-informed, and exploratory features, and surfacing leakage risks.

**Who might use this:**
- Machine learning researchers designing feature sets
- Psychology students deriving questionnaire measures
- Biomedical engineers extracting sensor features

**Example use cases:**
- Defining gait features for a biomechanics study
- Creating domain-informed variables for a cognitive science ML project
- Suggesting ablation strategies for a computer vision feature set

### Statistical Analysis
Connects hypotheses to statistical tests, clarifies assumptions, defines primary and fallback analysis plans, and distinguishes exploratory vs. confirmatory work.

**Who might use this:**
- Graduate students writing thesis analysis plans
- Labs interpreting pilot data
- Interdisciplinary teams planning confirmatory and exploratory analyses

**Example use cases:**
- Outlining a repeated-measures ANOVA for a rehabilitation study
- Planning fallback analysis for missing data in a neuroscience pilot
- Distinguishing exploratory from confirmatory analyses in a public health project

### Paper Outliner
Converts results and claims into a structured manuscript plan, aligning claims to evidence, surfacing missing evidence, and suggesting figure/table strategies.

**Who might use this:**
- Students planning thesis chapters
- Faculty teams preparing journal submissions
- Labs outlining conference papers

**Example use cases:**
- Structuring a manuscript for a multi-sensor soccer dataset study
- Planning figures and tables for a clinical trial report
- Outlining a conference paper for a computer vision benchmark

### Reviewer Mode
Emulates rigorous peer review, surfacing weak sections, unsupported claims, likely reviewer objections, and providing prioritized, actionable revision guidance.

**Who might use this:**
- Labs conducting pre-submission internal review
- Advisors and students critiquing dissertation chapters
- Research teams preparing for journal submission

**Example use cases:**
- Internal review of a rehabilitation manuscript before journal submission
- Critique and revision workflow for a dissertation chapter
- Reviewer-mode check for a multi-author environmental science paper

---


## Skill Pipeline and Reasoning Flow
Skills operate as a modular research reasoning pipeline, not just a sequence of formatters. Each skill produces explicit, machine-readable handoff artifacts for downstream skills, preserving assumptions, uncertainties, and tradeoffs at each stage. Example flows:
- `literature-review → gap-finder → experiment-design → protocol-writer → dataset-schema-designer → dataset-qa → feature-engineering → statistical-analysis → paper-outliner → reviewer-mode`
- Handoff blocks include: Gap Handoff Block, Experiment Framing Block, Protocol + Schema Handoff Block, QA Validation Block, Feature Set Block, Paper Claims Block, Reviewer Exposure Block, Revision Action Block
- See SKILLS_INDEX.md for detailed handoff logic and integration points.

## How to Use
1. Review standards in `standards/` and shared assets in `shared/`
2. Invoke skills via your agent environment, referencing `skills/`
3. Use domain examples in `examples/` for guidance
4. Inspect handoff blocks and reasoning artifacts for downstream use

## Adding a New Skill
- Follow the `standards/skill-spec-template.md` (reasoning, tradeoff, and handoff logic required)
- Place new skill in `skills/`
- Document and test per `CONTRIBUTING.md`
- Reference shared standards and assets

## How This Repo Should Evolve
- Skills must remain agent-agnostic, standards-compliant, and reasoning-driven
- All changes require peer review and changelog entry
- New skills should extend, not duplicate, existing logic
- Cross-skill consistency, explicit handoff, and interoperability are mandatory

## Roadmap
- Expand skill coverage for new research reasoning workflows
- Tighten cross-skill output and input alignment
- Integrate advanced evaluation and benchmarking
- Support new agent platforms and research domains

---

## Core Skills and Academic Use Cases

This section explains how each core skill can be used by students, graduate researchers, academic labs, and technical research teams across STEM and academic fields. Each skill is designed to support rigorous, auditable research work in real-world academic and interdisciplinary settings.

### Literature Review
Synthesizes academic papers, clusters evidence by methodology, maps consensus and disagreement, and identifies recurring limitations. 

**Who might use this:**
- PhD students conducting systematic reviews
- Undergraduate or master's students preparing thesis backgrounds
- Faculty or lab teams scoping new research directions

**Example use cases:**
- A rehabilitation science student synthesizing RCTs on stroke interventions
- A computer vision researcher comparing segmentation methods across datasets
- A public health student summarizing intervention studies for a capstone

### Gap Finder
Moves from "what is known" to "what is missing" by identifying actionable research gaps, ranking them by novelty, feasibility, and impact, and generating candidate research questions.

**Who might use this:**
- Graduate students seeking thesis topics
- Faculty planning grant proposals
- Interdisciplinary teams mapping new research areas

**Example use cases:**
- Identifying under-studied populations in biomechanics
- Spotting missing validation studies in machine learning benchmarks
- Finding publishable directions for a psychology thesis

### Experiment Design
Turns research questions into structured, reproducible studies with explicit variables, controls, alternative designs, and tradeoff analysis.

**Who might use this:**
- Psychology students designing cognitive experiments
- Engineering students planning validation studies
- Biomechanics labs preparing pilot protocols

**Example use cases:**
- Designing a repeated-measures study for gait analysis
- Planning a pilot for a new wearable sensor in neuroperformance
- Structuring a validation study for a new computer vision algorithm

### Protocol Writer
Formalizes methods into reproducible, auditable procedures, distinguishing required vs. optional steps and surfacing operational risks.

**Who might use this:**
- Clinical researchers preparing IRB-ready protocols
- Lab managers writing SOPs
- Students preregistering studies

**Example use cases:**
- Drafting a protocol for a multi-site clinical trial
- Creating a preregistration-ready procedure for a cognitive science experiment
- Writing a standard operating procedure for a rehabilitation lab

### Dataset Schema Designer
Defines dataset fields, metadata, validation rules, provenance, and harmonization requirements for robust, FAIR-compliant data.

**Who might use this:**
- Biomedical engineers planning sensor datasets
- Clinical researchers designing spreadsheets for outcomes
- Environmental scientists harmonizing multi-site data

**Example use cases:**
- Creating a schema for a wearable sensor dataset in biomechanics
- Designing metadata and validation for a clinical outcomes spreadsheet
- Planning harmonization rules for a multi-site environmental study

### Dataset QA
Assesses dataset quality, detects missing data, inconsistencies, schema drift, harmonization issues, and readiness for analysis.

**Who might use this:**
- Public health researchers cleaning longitudinal datasets
- Biomechanics labs exporting motion capture data
- Clinical teams preparing outcomes tables for analysis

**Example use cases:**
- Detecting schema drift in a multi-year clinical registry
- Identifying harmonization issues in a multi-sensor motion capture export
- Flagging missing or inconsistent data in a public health survey

### Feature Engineering
Defines meaningful variables for analysis and modeling, separating raw, derived, domain-informed, and exploratory features, and surfacing leakage risks.

**Who might use this:**
- Machine learning researchers designing feature sets
- Psychology students deriving questionnaire measures
- Biomedical engineers extracting sensor features

**Example use cases:**
- Defining gait features for a biomechanics study
- Creating domain-informed variables for a cognitive science ML project
- Suggesting ablation strategies for a computer vision feature set

### Statistical Analysis
Connects hypotheses to statistical tests, clarifies assumptions, defines primary and fallback analysis plans, and distinguishes exploratory vs. confirmatory work.

**Who might use this:**
- Graduate students writing thesis analysis plans
- Labs interpreting pilot data
- Interdisciplinary teams planning confirmatory and exploratory analyses

**Example use cases:**
- Outlining a repeated-measures ANOVA for a rehabilitation study
- Planning fallback analysis for missing data in a neuroscience pilot
- Distinguishing exploratory from confirmatory analyses in a public health project

### Paper Outliner
Converts results and claims into a structured manuscript plan, aligning claims to evidence, surfacing missing evidence, and suggesting figure/table strategies.

**Who might use this:**
- Students planning thesis chapters
- Faculty teams preparing journal submissions
- Labs outlining conference papers

**Example use cases:**
- Structuring a manuscript for a multi-sensor soccer dataset study
- Planning figures and tables for a clinical trial report
- Outlining a conference paper for a computer vision benchmark

### Reviewer Mode
Emulates rigorous peer review, surfacing weak sections, unsupported claims, likely reviewer objections, and providing prioritized, actionable revision guidance.

**Who might use this:**
- Labs conducting pre-submission internal review
- Advisors and students critiquing dissertation chapters
- Research teams preparing for journal submission

**Example use cases:**
- Internal review of a rehabilitation manuscript before journal submission
- Critique and revision workflow for a dissertation chapter
- Reviewer-mode check for a multi-author environmental science paper

---

**Note:** This repository is a core part of the QAI Lab research infrastructure. For internal use only.