# Literature Review Skill

## Purpose
Systematically synthesize academic literature for a defined research topic, producing structured, citable, auditable, and reasoning-rich outputs for downstream research workflows.

## Scope
- Academic papers, systematic reviews, and preprints
- Outputs evidence clusters, consensus/disagreement maps, limitation statements, and explicit handoff blocks
- Upstream: Entry point
- Downstream: Gap Finder, Experiment Design

## When to Use
- At the start of a research project
- When preparing manuscript backgrounds or grant proposals
- For identifying field trends, consensus, and research gaps

## When Not to Use
- For non-peer-reviewed or non-academic sources
- When a simple search or summary is sufficient

## Required Inputs
- Research topic or question (explicit, unambiguous)
- Scope constraints (years, journals, inclusion/exclusion criteria)

## Optional Inputs
- Specific databases or sources
- Output format preference (Markdown, table)

## Workflow
1. Parse and clarify research topic and scope; request clarification if ambiguous
2. Retrieve and filter relevant literature using explicit inclusion/exclusion criteria
3. Organize findings by methodological family, theme, and chronology
4. Cluster evidence, identify consensus and disagreement, and score evidence strength
5. Summarize findings in structured Markdown sections
6. Generate a complete, standards-compliant citation list
7. Explicitly state limitations, uncertainties, and recurring gaps
8. Produce a Gap Handoff Block for downstream skills

## Output Contract
- Executive Summary
- Evidence Clusters (by methodology/theme)
- Consensus/Disagreement Map
- Evidence Strength Table
- Limitations and Uncertainties (explicit section)
- Gap Handoff Block (structured for Gap Finder and Paper Outliner)
- Citations (APA 7th or domain standard, see `shared/citation-rules.md`)
- Errors (if any)

## Assumption Handling
- Explicitly list assumptions about literature coverage, inclusion/exclusion, and evidence strength
- Surface weak or unvalidated assumptions

## Uncertainty Handling
- Report what is known, inferred, or unresolved
- Highlight areas of high uncertainty or disagreement

## Tradeoff Analysis
- Discuss tradeoffs in methodological approaches or evidence weighting
- Present decision logic for evidence clustering

## Alternative Generation
- Where appropriate, present alternative interpretations or thematic clusters

## Failure Awareness
- Warn if evidence is weak, consensus is lacking, or coverage is incomplete
- Report ambiguous or missing data explicitly

## Handoff Artifacts
- Gap Handoff Block: machine-readable summary of gaps, limitations, and open questions for downstream skills

## Evidence Discipline
- Distinguish evidence-backed claims, domain assumptions, and recommendations
- All claims must be cited

## Quality Checks
- All claims are cited and traceable
- Output is structured, non-generic, and standards-compliant
- Limitations, uncertainties, and assumptions are explicit
- Output is suitable for direct use by Gap Finder and Paper Outliner

## Failure Modes
- Overly broad, shallow, or generic summaries
- Missing or inconsistent citations
- Failure to report limitations, uncertainty, or assumptions
- Inadequate handling of ambiguous input
- Failure to produce a usable Gap Handoff Block

## Domain Adaptation Notes
- For biomechanics: emphasize methods, populations, sensor types, and recurring measurement limitations
- For computer vision: emphasize datasets, algorithms, benchmarks, and reproducibility
- For rehabilitation: emphasize interventions, outcomes, and patient populations
- For neuroperformance: emphasize cognitive/behavioral domains and measurement modalities

## Example Invocation Patterns
- "Summarize recent literature on ACL injury prevention in athletes (2018-2024, peer-reviewed only). Include evidence clusters and a Gap Handoff Block."
- "Produce a structured review of wearable sensor accuracy in sports performance, citing all sources, and map consensus/disagreement."
- "Synthesize findings on gait analysis methods in rehabilitation, with explicit limitations, uncertainties, and handoff for gap analysis."
