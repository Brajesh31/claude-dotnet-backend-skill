# ASP.NET Core API Design

## Contract
- Use resource-oriented routes and consistent HTTP semantics.
- Validate input at the boundary and return stable problem details.
- Use DTOs rather than exposing persistence entities.
- Define pagination, filtering, sorting, and maximum page sizes.
- Version APIs when compatibility requirements justify it.

## Application structure
A practical separation:
- API: routing, authentication, request/response mapping.
- Application: use cases, orchestration, validation.
- Domain: invariants and business rules.
- Infrastructure: database, messaging, external services.

Do not add layers without a concrete reason. A small service can remain simpler.

## Reliability
- Propagate cancellation tokens.
- Apply timeouts to outbound calls.
- Use bounded retries only for transient failures and idempotent operations.
- Use idempotency keys for retryable write workflows where duplicates are harmful.
