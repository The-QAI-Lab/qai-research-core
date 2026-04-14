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

## Core Skills
- Literature Review
- Gap Finder
- Experiment Design
- Protocol Writer
- Dataset Schema Designer
- Dataset QA
- Feature Engineering
- Statistical Analysis
- Paper Outliner
- Reviewer Mode

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

**Note:** This repository is a core part of the QAI Lab research infrastructure. For internal use only.