# Verification and Delivery

Read this reference when an implementation changes behavior, is being productionized, or is being prepared for handoff or deployment.

## Verification strategy

Choose checks from the risk and changed surface:

- focused unit tests for business rules and failure decisions;
- integration tests for database, filesystem, network, queue, or service boundaries;
- contract tests for public APIs and external integrations;
- end-to-end tests for critical user journeys;
- type checks, lint, formatting, builds, and packaging checks used by the repository;
- manual or exploratory checks where automation would not provide proportionate value.

Test meaningful negative paths, including invalid data, dependency failure, authorization boundaries, retries, timeouts, partial progress, and shutdown when relevant.

Run focused checks during iteration. Broaden verification when the change affects shared contracts, dependencies, migrations, security boundaries, deployment, or multiple components.

Never claim a check passed unless it was actually run. Record the command, result, and any environmental reason a required check could not run.

## Container and operational delivery

When Docker is requested or part of the established delivery path, account for:

- deterministic builds and an appropriate base image;
- non-root execution where practical;
- minimal runtime contents and a useful `.dockerignore`;
- configuration and secrets supplied at runtime;
- correct port and filesystem behavior;
- health and readiness semantics;
- startup dependencies and migrations;
- logs to standard streams;
- signal handling and graceful shutdown;
- persistent data ownership and backup expectations;
- resource assumptions and operational limits.

Verify the built artifact through the same interface customers or operators will use when practical.

## Documentation and handoff

Documentation should let a new developer or agent quickly discover:

- what the system does and does not do;
- architecture, important boundaries, and main data flow;
- responsibilities of key directories and modules;
- setup, configuration, development, test, build, and deployment commands;
- database and persistent-data locations;
- external dependencies and operational assumptions;
- common failure modes and troubleshooting paths;
- important decisions, known limitations, and safe next steps.

Keep documentation factual, direct, current, and free of secrets or personal data. Prefer a concise map that links to deeper material over a single exhaustive document.

