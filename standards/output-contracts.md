# Output Contracts

All skills must define explicit, auditable, and operational output structures. Outputs must be:
- Machine-readable (Markdown, tables, or JSON if justified)
- Human-auditable and reproducible
- Consistent with shared standards and templates
- Structured for direct downstream skill consumption (handoff blocks)

## Required Structure
- Section headers for each output part (e.g., Executive Summary, Assumptions, Tradeoffs, Citations, Limitations, Handoff Block)
- Explicit citation format (see `shared/citation-rules.md`)
- Error and limitation reporting (including uncertainty and missing data)
- Tradeoff matrices, risk registers, and decision tables where appropriate
- Handoff artifacts must be clearly labeled and machine-readable

## Minimum Rigor Requirements
- All claims must be cited
- Limitations and assumptions must be explicitly stated
- Uncertainty must be reported, not hidden
- Failure cases must be handled with explicit error sections
- Outputs must distinguish evidence-backed claims from inference or recommendation

## Example Output Contract
```
## Executive Summary
- ...

## Core Output (structured)
- ...

## Assumptions
- ...

## Unresolved Questions
- ...

## Tradeoff Matrix
| Option | Pros | Cons | Rationale |
|--------|------|------|-----------|
| ...    | ...  | ...  | ...       |

## Risks / Limitations
- ...

## Handoff Block (for downstream skill)
- ...

## Citations
- ...

## Errors (if any)
- ...
```
