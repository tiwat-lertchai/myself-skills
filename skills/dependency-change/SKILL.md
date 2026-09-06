---
name: dependency-change
description: Evaluate, add, remove, or upgrade a software dependency, framework, runtime, or experimental technology with explicit tradeoffs, compatibility checks, migration planning, and verification. Use when dependency manifests or lockfiles will change, or when comparing native code with a third-party solution. Do not use for ordinary implementation that only uses established dependencies.
---

# Dependency Change

Choose dependencies deliberately and avoid unrelated churn.

## Inspect first

- Read the current manifest, lockfile, runtime versions, package-manager configuration, and nearby usage.
- Determine whether the task actually requires a dependency change.
- Check whether a suitable standard-library capability or established project dependency already solves the problem clearly.
- Identify compatibility constraints, peer requirements, platform support, licenses, known vulnerabilities, and maintenance status from current authoritative sources.

## Compare options

For a material new dependency or technology, present the strongest reasonable options and explain:

- capability and complexity removed;
- readability and maintainability;
- maturity, adoption, and release health;
- security history and supply-chain exposure;
- bundle, image, runtime, performance, and operational cost;
- compatibility and migration effort;
- quality and longevity of documentation;
- limitations and exit strategy.

Recommend an option, but request direction before a choice that materially changes architecture, deployment, licensing, data compatibility, or long-term operational burden.

Do not add a dependency merely to save a few lines of understandable code. Do not reject a mature dependency merely because a native implementation is possible.

## Change safely

- Select the narrowest compatible version range consistent with repository conventions.
- Read release notes and migration guidance for consequential or major changes.
- Keep manifest and lockfile changes focused.
- Isolate experimental or high-risk evaluation from production work when practical, and define its success and stopping criteria.
- Update code, configuration, documentation, and migration notes affected by the change.

## Verify and report

Run the repository's applicable tests, type checks, lint checks, and production builds after a dependency or lockfile change. Add focused compatibility or behavior tests when the dependency boundary is important.

Report the selected version, rationale, alternatives considered, manifest and lockfile impact, vulnerabilities or compatibility constraints found, migration implications, verification commands and actual results, and remaining limitations. Never describe the change as fully verified when required infrastructure or credentials prevented relevant checks.

