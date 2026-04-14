# Protocol Writer Skill

A reasoning module for generating detailed, reproducible, and standards-compliant protocols that tie operational steps directly to experimental design rationale. Surfaces operational failure points, includes checkpoints and deviations tracking, and produces structured handoff artifacts for dataset planning and QA.

- **Purpose:** Produce step-by-step, auditable protocols for IRB submission, preregistration, or study documentation, based on structured experiment designs and rationale.
- **When to Use:** After experiment design is finalized and Protocol + Schema Handoff Block is available, for regulatory, ethical, or operational documentation.
- **When Not to Use:** If experiment plan is missing, ambiguous, or lacks variable/control definitions.
- **Related Standards/Assets:** `shared/experiment-templates.md`, `standards/output-contracts.md`, `skills/experiment-design/skill.md`
- **Upstream:** Experiment Design (Protocol + Schema Handoff Block)
- **Downstream:** Dataset Schema Designer, Dataset QA
- **Handoff Artifact:** Protocol Handoff Block (structured for downstream skills)
- **Reasoning Features:** Step-to-design traceability, operational failure point surfacing, checkpoints, deviations tracking, explicit documentation requirements
