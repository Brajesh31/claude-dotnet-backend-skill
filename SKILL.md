---
name: dotnet-backend
description: Designs, implements, reviews, and troubleshoots maintainable .NET backend services and APIs.
---

# .NET Backend

Use this skill for ASP.NET Core APIs, background services, dependency injection, persistence, authentication, testing, observability, and deployment.

## Workflow
1. Identify the .NET SDK/runtime version, hosting model, existing architecture, and constraints.
2. Inspect the project before proposing structural changes.
3. Define API contracts, validation, error semantics, and authorization boundaries.
4. Keep controllers/endpoints thin; isolate business rules in application services or domain logic.
5. Use asynchronous I/O and cancellation tokens for request-bound work.
6. Add tests for success, validation, authorization, failure, and concurrency paths.
7. Review configuration, secrets, logging, health checks, and deployment readiness.

## Engineering rules
- Prefer supported LTS versions unless the project requires otherwise.
- Never hardcode secrets or log credentials, tokens, or sensitive payloads.
- Enforce authorization server-side, not only in the UI.
- Use EF Core migrations deliberately and review generated SQL for risky changes.
- Avoid swallowing exceptions or returning internal stack traces to clients.
- Document breaking API changes and migration steps.

See `references/api-design.md`, `references/security-review.md`, and `templates/service-design.md`.
