---
name: security-sensitive-change
description: Plan, implement, or review software changes where authentication, authorization, tenant isolation, cookies, CORS, secrets, file handling, public endpoints, or another security boundary is central. Use for secure-by-default implementation and explicit security review. Do not trigger merely because ordinary code has some theoretical security relevance.
---

# Security-Sensitive Change

Treat security as part of the product contract while preserving the user's requested scope.

## Establish the boundary

Identify the protected assets, actors, trust boundaries, entry points, sensitive data, authorization decisions, and likely abuse cases. Inspect the actual language, framework, deployment model, and existing controls before recommending a pattern.

Use current official guidance that matches the installed version when framework behavior is consequential or unclear.

## Implement securely

- Deny access by default and enforce authorization on the trusted server side.
- Validate at trust boundaries and encode output for its destination.
- Preserve tenant isolation through queries, caches, jobs, storage, and logs.
- Keep credentials and secrets out of source, images, logs, errors, and client bundles.
- Use explicit cookie, origin, redirect, upload, and rate-limit rules appropriate to the deployment.
- Bound resource use, retries, timeouts, file sizes, and externally controlled work.
- Avoid weakening a control solely to make local development convenient; provide an explicit environment-aware configuration when needed.

Do not invent a security mechanism when a maintained framework capability is suitable. Before introducing a material dependency or changing a trust model, explain the benefits, risks, compatibility, operational impact, and migration implications.

## Verify

Test the relevant allowed and denied paths. Include cross-user or cross-tenant access, missing or malformed credentials, invalid input, replay or repeated actions, unsafe redirects or origins, upload boundaries, sensitive error output, and resource limits when applicable.

Broaden to an authorized local black-box or adversarial check only when requested, required by the repository, or proportionate to a genuinely high-risk change. Keep testing within systems under the user's control. Stop and report exploitable findings before considering the work shippable.

Report the threat or failure addressed, controls changed, evidence from actual checks, residual risk, and any unverified environment-dependent behavior.

