# Dataset Schema Designer Skill

A reasoning module for defining structured, FAIR-compliant, and standards-driven dataset schemas. Explicitly surfaces required/optional fields, metadata, provenance, versioning, schema risks, harmonization considerations, and downstream analysis implications. Produces machine-readable QA Validation Block for downstream skills.

- **Purpose:** Produce explicit, auditable dataset field definitions, types, metadata, provenance, and validation rules for reproducible research and downstream QA/analysis.
- **When to Use:** Before data collection, during protocol development, or for schema review and harmonization, with Protocol Handoff Block available.
- **When Not to Use:** If research goals or data collection plan are missing or ambiguous.
- **Related Standards/Assets:** `shared/dataset-schema-templates.md`, `standards/output-contracts.md`, `skills/protocol-writer/skill.md`, `skills/dataset-qa/skill.md`
- **Upstream:** Protocol Writer (Protocol Handoff Block)
- **Downstream:** Dataset QA, Feature Engineering
- **Handoff Artifact:** QA Validation Block (structured for downstream skills)
- **Reasoning Features:** Field/metadata/provenance surfacing, schema risk identification, harmonization, downstream analysis implications, validation rule definition
