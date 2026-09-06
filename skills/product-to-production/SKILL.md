---
name: product-to-production
description: Take a substantial software product, application, service, or feature from problem definition and data or UX design through a bounded prototype, maintainable implementation, verification, packaging, and documentation. Use for greenfield builds, end-to-end features, prototype-to-production work, or delivery-readiness audits. Do not use for tiny isolated edits that do not need lifecycle planning.
---

# Product to Production

Deliver the requested outcome through only the stages it actually needs. Scale the process to the task's scope and risk; do not turn it into ceremony.

## Choose the working mode

- **Greenfield:** Start from the problem, users, data, and operating constraints.
- **Existing project:** Inspect the current system first. Preserve sound decisions and fill only relevant gaps.
- **Prototype only:** Prove the riskiest assumption and stop with evidence, limitations, and a clear next decision.
- **Productionize:** Evaluate a working prototype, retain suitable parts, and replace shortcuts that affect correctness, security, operation, or maintenance.
- **Delivery audit:** Assess an implementation against its requirements, risks, verification, packaging, and documentation without expanding the product scope.

## Core workflow

1. Establish the problem, intended users, smallest useful outcome, non-goals, constraints, and observable acceptance criteria. For greenfield or ambiguous product work, read [references/product-discovery.md](references/product-discovery.md).
2. Model domain data, user journeys, system boundaries, and external contracts before committing to architecture that depends on them. Read [references/data-and-design.md](references/data-and-design.md) when the task includes database, API, UX, or architectural design.
3. Inspect the environment and existing project conventions. Prefer an established suitable pattern to inventing a new one.
4. Use a bounded prototype when an important technical or product assumption remains uncertain. State what it proves, what it omits, and the condition for stopping. Read [references/prototype-and-production.md](references/prototype-and-production.md).
5. Review the proof against its acceptance criteria. Surface discovered requirements and tradeoffs instead of silently expanding scope.
6. Productionize only after the approach is sufficiently supported. Favor clear responsibilities, explicit behavior, testable boundaries, and ordinary constructs.
7. Verify behavior in proportion to risk and prepare the requested delivery artifacts. Read [references/verification-and-delivery.md](references/verification-and-delivery.md).

## Decision principles

- Diagnose and inspect before proposing a broad fix.
- Keep code that is already clear and correct. Do not rewrite merely for stylistic uniformity.
- Flag surprising behavior or architecture before making a broad or difficult-to-reverse change.
- Extract a function, module, or interface when it materially improves comprehension, testing, reuse, replacement, or migration.
- Prefer suitable language and standard-library capabilities when they remain readable and maintainable.
- Reuse established project dependencies when appropriate.
- Before introducing a material dependency or technology, explain its benefit and its maintenance, compatibility, security, licensing, runtime, deployment, and migration costs. Request direction when the choice materially changes architecture or operational burden.
- Treat retry counts, delays, timeouts, backoff, failure behavior, and shutdown behavior as product requirements. Do not invent fixed values when they are consequential.
- Complete already-authorized, reversible investigation before asking a blocking question. Ask when the answer could materially change the outcome.

## Completion

Report the outcome, important decisions and tradeoffs, affected files or systems, resulting behavior, actual verification commands and results, unresolved limitations, and relevant operational or documentation changes.

