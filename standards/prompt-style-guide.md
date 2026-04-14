# Prompt Style Guide

All prompts in this repository must:
- Be portable across Copilot, Codex, Claude Code, Gemini, Kiro, OpenClaw, and similar agent systems
- Use explicit, unambiguous, and operational instructions
- Require structured outputs (sections, tables, lists, handoff blocks) as defined in output contracts
- Reference shared standards and templates by file name
- Avoid model-specific syntax or assumptions
- Require reasoning, assumption surfacing, tradeoff analysis, and uncertainty reporting where appropriate

## Formatting
- Use Markdown for all prompts and outputs
- Label all sections and outputs clearly
- Specify required input and output formats
- Require explicit error, limitation, and uncertainty reporting
- Require handoff artifacts for downstream skills

## Examples
- "Summarize the following literature using the structure in `shared/paper-structures.md`, cluster by methodology, and cite all sources. Include a Gap Handoff Block."
- "List at least 3 research gaps, each with supporting citations, using the format in `standards/output-contracts.md`. Include a prioritization matrix and Experiment Framing Block."

## Common Pitfalls
- Overly broad or vague prompts
- Model-specific or non-portable instructions
- Unstructured or freeform outputs
- Failure to reference shared standards
- Prompts that do not require reasoning, tradeoff, or handoff logic
