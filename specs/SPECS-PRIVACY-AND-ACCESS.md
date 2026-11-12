# Private scope, access and operational boundaries

This specification adapts useful isolation, API-access, identity and operational patterns without adopting another product's data model, token/header names, database, cloud or identity provider. The Go runtime is planned; these requirements are not evidence of implemented enforcement.

## Trusted scope

Organization and project are explicit Storm Harbor authorization boundaries. The canonical identifier contract must have one versioned owner. Deployment placement, cloud account/subscription/project and business authorization are separate dimensions; sharing a cloud account or network never grants access.

Resolve effective scope from authenticated identity plus authoritative membership and policy. YAML, browser state, request parameters and queue messages cannot independently select a trusted scope. Missing, malformed, revoked or conflicting context fails before persistence, cache, retrieval or provider calls. A user belonging to two organizations must not receive combined permissions accidentally.

Scope reads, writes, deletes, upserts, bulk operations, counts, existence checks, transactions and dependency traversals inside the operation before data crosses the adapter. Required scope arguments are not optional. Scoped uniqueness includes the canonical scope; pagination cursors bind scope and query shape. Global registries and cross-organization administration require explicitly owned ports and permission, never a bypass flag on ordinary methods.

## Private knowledge, files and background work

Cache keys include scope and relevant actor/policy versions; membership or policy changes invalidate decisions. Search/vector queries apply authorized filters before retrieval. Downloads, signed URLs, exports and evidence access are reauthorized for their scope. Jobs, retry records, leases, idempotency, dead letters and controller state preserve the same boundary.

AI/RAG/CLI integrations must prove isolation under colliding identifiers, concurrent context switches and revoked membership. Public fixtures remain synthetic. Retrieved knowledge cannot alter tool permissions, secret resolution or destination policy. Private results never become a shared corpus implicitly.

## Identity and workload permissions

Human authentication, organization/project authorization and provider workload identity are separate decisions. Every protected endpoint/tool declares its policy in reviewed route/resource metadata; substring matching against a URL is not an authorization rule. Adapters discard untrusted internal headers and propagate only validated context.

Use short-lived, narrowly scoped workload credentials where supported; target audience, capability, expiration and resource scope must match. A provider IAM grant does not establish a user's product permission. Identity integration is configurable; no mandatory api-auth, company registration, corporate email policy or custom platform API-key header is imported.

## Operations and resilience

Separate startup, liveness, dependency readiness and business recovery health. A live process is not necessarily a ready worker or recovered service. Shutdown stops new work, bounds in-flight completion and leaves unacknowledged work recoverable.

Use structured, sanitized events with service/revision, stable severity, correlation and outcomes. Production output is one JSON event per line without ANSI or unrestricted bodies; verbose authorization diagnostics remain development-only. Audits record security decisions separately. Correlation is not authorization or idempotency.

Prometheus/OTLP instruments have bounded labels and a reviewed Storm Harbor namespace; do not expose metrics anonymously or label them with customer IDs, secrets, resource URLs or knowledge queries. Runtime start counters are not durable restart history. Define request/dependency/controller/queue/recovery outcome metrics at their owning boundaries and keep provider SDKs behind adapters.

## Payment boundary

Voluntary sponsorship is separate from product subscriptions and recovery authorization. The receiving entity and existing Stripe account are owner choices; do not import another product's billing service or catalog. Future amounts use integer minor units and explicit currencies. Provider account and TEST/LIVE bindings remain separate.

A browser success redirect is not payment proof. If an application later depends on payment events, verify the raw-body signature and replay window, durably accept events, process idempotently and tolerate duplicates/out-of-order delivery. Unknown provider outcomes stay pending until authoritative reconciliation. Ordinary tests use provider test mode and never send real charges.

## Acceptance

Test one actor across two organizations/projects with distinct permissions; switched/concurrent context; revoked membership; guessed/colliding IDs; counts, bulk operations and traversals; cache invalidation; scoped jobs/idempotency; RAG/vector denial; files/exports/evidence; and explicit administrative authorization. Use isolated Testcontainers for applicable owned dependencies. Report actual results and absent foreign data/side effects, not only successful responses.
