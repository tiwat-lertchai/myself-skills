---
name: evidence-research
description: Research a question using current, authoritative, and diverse sources; evaluate evidence quality, reconcile conflicting claims, and produce a traceable synthesis with citations. Use for literature reviews, market or policy research, technical investigations, fact-checking, and other evidence-backed reports. Do not use for simple lookups that need only one direct authoritative answer.
---

# Evidence Research

Produce a decision-useful answer whose important claims can be traced to suitable evidence. Match the depth of research to the stakes, breadth, uncertainty, and time available.

## Frame the question

Clarify the decision or outcome the research should support, the audience, scope, geography, time period, and required freshness. Define ambiguous terms and separate the main question into answerable subquestions when that improves coverage.

If a missing choice would materially change the research direction, ask for it. Otherwise state a reasonable assumption and continue.

## Build the evidence base

- Start with primary and authoritative sources: official documentation, laws and regulators, standards, original datasets, company filings, and peer-reviewed research.
- For technical claims about a language, framework, runtime, library, protocol, or platform, consult its official documentation first and cite the exact version and relevant page or section. Use official specifications, API references, release notes, migration guides, and maintainers' repositories when they are the most direct evidence. Confirm that documentation matches the version actually in scope rather than assuming the latest docs apply.
- Use strong secondary sources to add context, compare interpretations, and discover primary evidence.
- Include useful practitioner writing, independent blogs, Medium posts, community analyses, and expert commentary when they contribute firsthand experience, a reproducible method, a valuable synthesis, or a perspective missing from formal sources. Evaluate the author and the specific claim rather than rejecting or accepting a source based only on its publishing platform.
- Search from multiple angles, including terminology used by competing explanations and evidence that could disconfirm the leading conclusion.
- Prefer sources that match the relevant version, jurisdiction, population, and date. Treat search snippets, unattributed summaries, and AI-generated pages as discovery aids rather than evidence.
- Record enough provenance to cite the exact page, document, dataset, or section supporting each consequential claim.

Do not equate popularity with reliability. Evaluate who produced the evidence, their relevant expertise or firsthand access, how the evidence was obtained, whether links and methods are inspectable, whether the method fits the claim, what incentives or conflicts exist, and whether independent sources corroborate it. Use informal sources in proportion to what they can establish: they may strongly support lived experience, implementation details, emerging practice, or expert interpretation, but should not be presented as peer-reviewed or authoritative evidence when they are not.

When official documentation and community guidance differ, determine whether the difference comes from version drift, undocumented runtime behavior, platform constraints, or opinion. Treat official documentation as the baseline for the supported contract, while allowing reproducible source code, tests, issue discussions, or practitioner evidence to demonstrate actual behavior or documented gaps.

## Preserve references

When the research should remain auditable after delivery, preserve a source register and offline evidence package alongside the report. Read [references/source-preservation.md](references/source-preservation.md) before collecting the sources. Keep the live canonical URL in every citation even when an offline copy exists, and make the local copy supplementary rather than a silent replacement for the original.

Do not archive sources for a quick lookup unless requested or clearly useful. Never bypass access controls, paywalls, licensing restrictions, or technical protections to create a copy.

## Analyze, do not merely collect

Distinguish reported facts, source interpretations, and your own inference. Compare definitions, methods, sample sizes, assumptions, dates, and populations before combining results.

When sources disagree, identify the source of disagreement and explain which evidence is more applicable rather than silently choosing one. Quantify uncertainty when the evidence permits it; otherwise describe its direction and practical significance without inventing precision.

For numerical claims, check units, denominators, time windows, and whether values are nominal, real, estimated, or observed. Recalculate or inspect the underlying data when the conclusion depends on arithmetic.

Stop when additional searching is unlikely to change the conclusion or materially reduce an important uncertainty. Say when the available evidence is too weak to support a confident answer.

## Synthesize for the user

Lead with the answer and its confidence, then present the evidence and reasoning needed to evaluate it. Include meaningful counterevidence, limitations, and unresolved questions. Separate recommendations from findings and tie each recommendation to the user's goals and constraints.

Cite consequential factual claims near the text they support, linking to the most direct source available. Never cite a source as support for a claim it does not establish, and do not hide weak support behind a long bibliography.

Report:

- the conclusion or key findings;
- scope and important assumptions;
- strongest supporting and conflicting evidence;
- uncertainty, limitations, and evidence gaps;
- practical implications or next steps when requested;
- sources in a format appropriate to the deliverable;
- the location and capture date of any offline evidence package.

Do not claim a systematic review, exhaustive search, or causal conclusion unless the method and evidence actually justify it.
