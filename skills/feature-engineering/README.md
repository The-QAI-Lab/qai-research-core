# Feature Engineering Skill

A reasoning module for proposing, defining, and justifying explicit, standards-driven features for research data analysis and modeling. Separates raw, derived, domain-informed, and exploratory features; justifies feature families; identifies leakage risks; and produces a machine-readable Feature Handoff Block for downstream analysis.

- **Purpose:** Suggest and document features for modeling or analysis, with explicit calculations, rationale, and risk handling, enabling reproducible and interpretable analysis.
- **When to Use:** After dataset QA and Feature Risk Block are available, before statistical analysis or model building.
- **When Not to Use:** If dataset or schema is missing, ambiguous, or unreviewed.
- **Related Standards/Assets:** `skills/dataset-qa/skill.md`, `skills/statistical-analysis/skill.md`, `standards/output-contracts.md`
- **Upstream:** Dataset QA (Feature Risk Block)
- **Downstream:** Statistical Analysis, Paper Outliner
- **Handoff Artifact:** Feature Handoff Block (structured for downstream skills)
- **Reasoning Features:** Feature family separation, leakage risk identification, hypothesis/analysis linkage, validation/ablation suggestions, machine-readable handoff
