# Validation and acceptance

Map acceptance criteria to concrete scenarios and exact candidate revisions. Report required/executed/passed scenarios separately from source coverage. A skipped, missing, flaky or mocked-away required scenario is not a pass.

Use the narrowest check that answers the current question and preserve passing evidence when source, tests, resolved dependencies and toolchain match. Run an equivalent suite once per validation candidate; repeat after a relevant change, failure or unresolved concern. Go race/coverage collection should share one execution rather than duplicate suites.

Runtime APIs, controllers, agents and CLIs need meaningful unit/contract tests, formatting, vet and build. Source-coverage targets are stated in AGENTS.md and require independent measured dimensions. Integration dependencies use ephemeral Testcontainers networks, dynamic ports, unique scoped fixtures, deterministic readiness and reliable teardown; do not depend on shared developer infrastructure.

Browser acceptance follows actor journeys through actual application artifacts and authoritative backend outcomes when those boundaries participate. Focused UI mocks are useful feedback, not proof of an integrated system. Include applicable negative validation, authentication/authorization, organization/project isolation, replay/concurrency, retry/cancellation, partial failure, i18n, accessibility and responsive behavior.

For the initial presentation-only website, verify all ten locale pages, static assets/styles, explicit and selected locale navigation, mobile menu/overflow, unknown-route 404 and absence of authenticated/API/customer-console routes. There is no backend/database dependency in that artifact, so Testcontainers and customer recovery acceptance do not apply to this publication. The legacy authenticated scaffold and future Go runtime keep their own qualification gaps.

Technical documentation stays in English and must pass a strict MkDocs build. Publishing workflows cannot run real recovery or request provider credentials. Actions and deployment inputs are immutable; artifacts exclude secrets, customer data, dependencies and filesystem metadata.

Provider acceptance uses deterministic adapters or safe sandboxes. Payment tests never create real charges; future Stripe webhooks need signature/timestamp validation, durable acceptance, duplicate/out-of-order handling and idempotent effects. A success redirect is not proof of payment. Hosted voluntary sponsorship links do not qualify product entitlements.

Only report publication after the deployment succeeds and verify the public URL. Domain routing, TLS, payment activation, CNCF submission and runtime recovery are distinct outcomes. No status label, document or implemented test suite substitutes for execution evidence.
