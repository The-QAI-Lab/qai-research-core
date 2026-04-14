# Dataset QA Skill

A reasoning module for assessing dataset quality, completeness, and integrity. Classifies issues by severity and impact, separates blocking from non-blocking issues, identifies likely root causes, and produces a machine-readable Feature Risk Block for downstream skills.

- **Purpose:** Review datasets for completeness, consistency, errors, standards compliance, and downstream risk, producing actionable QA reports and Feature Risk Blocks for analysis and feature engineering.
- **When to Use:** After data collection, before analysis, or during data harmonization, with QA Validation Block available.
- **When Not to Use:** If dataset schema is missing or ambiguous.
- **Related Standards/Assets:** `skills/dataset-schema-designer/skill.md`, `shared/review-rubric.md`, `standards/output-contracts.md`
- **Upstream:** Dataset Schema Designer (QA Validation Block)
- **Downstream:** Feature Engineering, Statistical Analysis
- **Handoff Artifact:** Feature Risk Block (structured for downstream skills)
- **Reasoning Features:** Issue severity/impact classification, root cause analysis, remediation priority, downstream risk surfacing, machine-readable handoff
