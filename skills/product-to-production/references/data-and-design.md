# Data, Experience, and System Design

Read this reference when a task requires database, API, UX, UI, or system architecture decisions.

## Domain and data

Begin with the domain rather than copying screens directly into tables. Determine:

- what each entity represents and who owns it;
- relationships, cardinality, required and optional attributes;
- identities, uniqueness, invariants, and validation rules;
- state transitions and data lifecycle;
- access boundaries and tenant isolation;
- personal, confidential, or regulated data;
- deletion, retention, history, and audit needs;
- expected queries, ordering, volume, and indexes;
- transaction and consistency boundaries;
- failure, reconciliation, migration, and rollback behavior.

Produce only the artifacts that improve the task: a domain model, data dictionary, ER diagram, schema, migration plan, or repository contract.

## Experience and interface

Design the user journey before polishing isolated screens. Account for relevant states:

- initial and default;
- loading and progress;
- empty and first-use;
- validation and recoverable error;
- unavailable dependency or partial failure;
- unauthorized and forbidden;
- disabled or read-only;
- success and confirmation.

Consider responsive behavior, accessibility, long or malformed data, localization, keyboard use, and destructive-action confirmation when relevant. Keep the visual language consistent with an existing product. For a new product, establish only the tokens and components needed for the first coherent experience.

## Architecture and contracts

Define responsibilities and boundaries before file structure. Make important flows visible:

- components and their ownership;
- requests, events, and data movement;
- public API and error contract;
- authentication and authorization boundaries;
- configuration and secret sources;
- synchronous and asynchronous work;
- observability and failure recovery;
- deployment units and persistent state.

Prefer the simplest architecture that satisfies current requirements and leaves known change points explicit. Avoid designing speculative extension points.

