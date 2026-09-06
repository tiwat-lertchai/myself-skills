# Prototype and Productionization

Read this reference when proving an uncertain approach or turning a prototype into maintained production code.

## Bound the prototype

Before implementation, state:

- the assumption or risk being tested;
- the smallest experiment that can test it;
- the observable pass or fail condition;
- what is intentionally omitted;
- whether the result is disposable, reference-only, or a candidate for retention.

A prototype may use temporary duplication, fixture data, narrow happy paths, or minimal structure when those choices are explicit and do not expose secrets or cause unsafe external effects. Keep it small enough to discard.

Stop when the question is answered. Report evidence, unexpected constraints, limitations, and the next decision. Do not silently broaden the prototype into the full product.

## Review before retaining

Do not assume prototype code must be rewritten, and do not assume it is production-ready. Evaluate each part:

- retain code that is clear, correct, testable, and operationally suitable;
- reshape code whose responsibilities or boundaries are unclear;
- replace shortcuts that affect correctness, data integrity, security, concurrency, performance, configuration, or failure recovery;
- remove or isolate temporary fixtures and hard-coded operational values;
- document decisions that future maintainers cannot infer from the code.

## Production baseline

As relevant to the product, establish:

- focused modules and stable interfaces;
- input validation and explicit error behavior;
- configuration separate from code and secrets outside source control;
- logging, metrics, and actionable health signals;
- graceful startup and shutdown;
- explicit retry, timeout, backoff, and terminal failure behavior;
- safe database migrations and rollback or recovery plans;
- meaningful automated tests;
- reproducible development, build, and runtime environments.

Avoid abstraction for its own sake. Extract behavior when doing so improves comprehension, testing, replacement, reuse, or migration.

