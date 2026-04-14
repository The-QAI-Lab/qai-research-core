# QAI Lab Research Core — Skills Index

This index catalogs all core research skills, their reasoning functions, handoff artifacts, dependencies, and integration points. Each skill is a structured reasoning module designed for rigorous, auditable research workflows and is portable across agent environments.

---

## Literature Review
- **Purpose:** Systematic, standards-driven synthesis of academic literature
- **Core Reasoning Function:** Cluster evidence by methodological family, identify consensus/disagreement, score evidence strength, surface recurring limitations
- **Inputs:** Research topic, scope, source constraints
- **Outputs:** Structured literature summaries, evidence clusters, consensus map, limitation statements, citation lists
- **Handoff Artifact:** Gap Handoff Block (for Gap Finder, Paper Outliner)
- **Upstream:** None (entry point)
- **Downstream:** Gap Finder, Experiment Design
- **Failure Risks:** Overreliance on weak sources, missing key dissent, shallow clustering
- **Related Standards:** citation-rules.md, paper-structures.md

## Gap Finder
- **Purpose:** Identify actionable research gaps and open questions
- **Core Reasoning Function:** Rank gaps by novelty, feasibility, impact, and data accessibility; distinguish true research gaps from implementation gaps
- **Inputs:** Literature summary or corpus, research area
- **Outputs:** Gap statements, prioritization matrix, candidate research questions, supporting citations
- **Handoff Artifact:** Experiment Framing Block (for Experiment Design, Paper Outliner)
- **Upstream:** Literature Review
- **Downstream:** Experiment Design
- **Failure Risks:** Prioritizing trivial gaps, missing feasibility constraints, unclear ranking logic
- **Related Standards:** research-glossary.md

## Experiment Design
- **Purpose:** Design robust, reproducible experiments with explicit variables and controls
- **Core Reasoning Function:** Generate primary and alternative designs, surface confounders, constraints, and validity threats, align analysis to design
- **Inputs:** Research question, gap statements, constraints
- **Outputs:** Experiment plans, variable/control definitions, risk register, analysis-to-design alignment check
- **Handoff Artifact:** Protocol + Schema Handoff Block (for Protocol Writer, Dataset Schema Designer)
- **Upstream:** Gap Finder, Literature Review
- **Downstream:** Protocol Writer, Dataset Schema Designer
- **Failure Risks:** Ignoring confounders, weak alternative path, missing risk register
- **Related Standards:** experiment-templates.md

## Protocol Writer
- **Purpose:** Generate detailed, standards-compliant experimental protocols
- **Core Reasoning Function:** Tie protocol steps to design rationale, identify operational failure points, specify documentation requirements
- **Inputs:** Experiment plan, methods, reporting standards
- **Outputs:** Protocol documents, compliance checklists, checkpoints, deviation tracking
- **Handoff Artifact:** Protocol Execution Block (for Dataset Schema Designer)
- **Upstream:** Experiment Design
- **Downstream:** Dataset Schema Designer
- **Failure Risks:** Omitted critical steps, unclear documentation, weak deviation handling
- **Related Standards:** output-contracts.md

## Dataset Schema Designer
- **Purpose:** Define structured, FAIR-compliant dataset schemas for research
- **Core Reasoning Function:** Specify required/optional fields, metadata, provenance, harmonization, validation rules, downstream analysis implications
- **Inputs:** Protocol details, data types, research goals
- **Outputs:** Dataset schema definitions, metadata, validation rules, harmonization notes
- **Handoff Artifact:** QA Validation Block (for Dataset QA)
- **Upstream:** Protocol Writer, Experiment Design
- **Downstream:** Dataset QA, Feature Engineering
- **Failure Risks:** Missing harmonization, weak validation, unclear provenance
- **Related Standards:** dataset-schema-templates.md

## Dataset QA
- **Purpose:** Assess dataset quality, completeness, and integrity
- **Core Reasoning Function:** Classify issues by severity/impact, separate blocking/non-blocking, identify root causes, remediation priority
- **Inputs:** Dataset sample, schema definition
- **Outputs:** QA reports, issue lists (with severity), remediation recommendations, risk register
- **Handoff Artifact:** Feature Risk Block (for Feature Engineering, Statistical Analysis)
- **Upstream:** Dataset Schema Designer
- **Downstream:** Feature Engineering
- **Failure Risks:** Missing critical issues, misclassifying severity, weak remediation logic
- **Related Standards:** review-rubric.md

## Feature Engineering
- **Purpose:** Propose and define features for analysis and modeling
- **Core Reasoning Function:** Separate raw/derived/domain/exploratory features, justify feature families, identify leakage risks, connect features to hypotheses
- **Inputs:** Dataset, QA report, research question
- **Outputs:** Feature lists (by type), calculation methods, rationale, validation/ablation suggestions
- **Handoff Artifact:** Feature Set Block (for Statistical Analysis)
- **Upstream:** Dataset QA, Dataset Schema Designer
- **Downstream:** Statistical Analysis
- **Failure Risks:** Feature leakage, unjustified features, missing validation
- **Related Standards:** statistical-analysis

## Statistical Analysis
- **Purpose:** Deliver high-rigor, auditable statistical analysis plans that explicitly connect hypotheses to tests, surface assumptions and uncertainties, analyze tradeoffs, and produce structured, machine-readable outputs for downstream research skills.
- **Core Reasoning Function:** Hypothesis-to-test linkage, explicit assumption and uncertainty reporting, tradeoff analysis, primary/fallback analysis, power/sample size concerns, interpretation cautions, exploratory vs. confirmatory distinction, structured handoff for downstream skills
- **Inputs:** Feature Set Block, dataset, hypotheses
- **Outputs:** Analysis plans, statistical test tables, reporting structure, interpretation cautions, Paper Claims Block (machine-readable)
- **Handoff Artifact:** Paper Claims Block (for Paper Outliner)
- **Upstream:** Feature Engineering
- **Downstream:** Paper Outliner
- **Failure Risks:** Unchecked assumptions, missing fallback, weak interpretation, missing Paper Claims Block
- **Related Standards:** paper-structures.md, output-contracts.md

## Paper Outliner
- **Purpose:** Produce high-rigor, structured outlines for research papers and manuscripts that explicitly align claims to evidence, surface missing evidence, suggest figure/table strategies, flag weak sections, and provide a publication readiness checkpoint.
- **Core Reasoning Function:** Claims-to-evidence linkage, missing evidence surfacing, figure/table strategy, weak section flagging, publication readiness checkpoint, structured handoff for downstream skills
- **Inputs:** Study results, analysis plan, target journal, Paper Claims Block
- **Outputs:** Paper outlines, section breakdowns, section notes, figure/table strategy, Reviewer Exposure Block (machine-readable), publication readiness checkpoint
- **Handoff Artifact:** Reviewer Exposure Block (for Reviewer Mode)
- **Upstream:** Statistical Analysis
- **Downstream:** Reviewer Mode
- **Failure Risks:** Misaligned claims, missing evidence, weak section structure, missing Reviewer Exposure Block
- **Related Standards:** paper-structures.md, output-contracts.md

## Reviewer Mode
- **Purpose:** Emulate rigorous, standards-driven peer review for manuscripts, protocols, or research outputs, surfacing fatal flaws, fixable weaknesses, and providing prioritized, actionable revision guidance.
- **Core Reasoning Function:** Fatal flaw/weakness distinction, prioritized revision guidance, rubric integration, Reviewer Exposure Block handling, explicit standards referencing
- **Inputs:** Manuscript, protocol, review rubric, Reviewer Exposure Block
- **Outputs:** Structured review reports, actionable feedback (fatal flaw/weakness distinction), rubric scores, revision priority ranking, Reviewer Exposure Block (machine-readable)
- **Handoff Artifact:** Revision Action Block (for authors, QA)
- **Upstream:** Paper Outliner, Protocol Writer
- **Downstream:** None (end of pipeline)
- **Failure Risks:** Overly generic feedback, missing fatal flaws, unclear revision priorities, missing Reviewer Exposure Block integration
- **Related Standards:** review-rubric.md, evaluation-checklist.md, output-contracts.md

---

See each skill folder in `skills/` for detailed specifications, operational examples, and validation tests.