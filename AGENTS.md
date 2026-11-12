# Storm Harbor engineering guidance

Storm Harbor is an independent, declarative multicloud recovery project. iot.EraX is its creator and an initial consumer, not a required identity, cloud or knowledge provider. Preserve private organization/project boundaries. The accepted scope includes AWS, Azure, DigitalOcean, Oracle Cloud and GCP through adapters, optional project-owned AI/RAG/CLI, YAML journeys and extensible resources/controllers.

Before planning or editing, review the applicable requirements in:

- [SPECS-CONTRACTS.md](specs/SPECS-CONTRACTS.md);
- [SPECS-DELIVERY.md](specs/SPECS-DELIVERY.md);
- [SPECS-ACCEPTANCE.md](specs/SPECS-ACCEPTANCE.md).

These adapt useful workspace engineering practices to Storm Harbor. They do not import another product's business domains, private libraries, cloud deployment, organization project numbers or account requirements.

## Language and architecture

Go 1.26.x is the official release line for new runtime applications, APIs, operators/controllers, agents, CLIs and SDKs. Browser HTML/CSS/JavaScript and frontend build tools are separate. Existing Next.js BFF/authentication and Node simulations remain transitional until a tested migration replaces them; do not claim the Go runtime already exists.

Use contract-first hexagonal boundaries, explicit mappings and versioned `storm-lib-*` contract owners. Keep vendor SDKs and private knowledge behind scoped adapters. Go expected failures use native typed errors with stable codes, categories, localization keys and safe arguments; outer adapters map transport and render text. Unknown failures fail closed without leaking internals. Configuration and AI output never grant authorization.

Technical documentation and repository-facing material are in English. The product website maintains all ten locale catalogs atomically; public errors and UI text use localization keys. Stable machine identifiers and provider/product names are not translated. Do not expose customer names, repositories, knowledge or operational evidence in examples; use synthetic fixtures unless explicit publication permission exists.

## Repository and delivery workflow

Identify the Git owner and preserve pre-existing changes before editing. This workspace contains independent repositories. Use the owning issue and [Storm Harbor Project #1](https://github.com/orgs/Storm-Harbor/projects/1), with native Issue Type, assignee, labels, Priority, Size, focused-hour Estimate, Workspace, Product and Status. Issues are the project items; linked PRs are not duplicate tasks.

Use English `feat-*` / `bug-*` issue titles, `<issue>-feat-<slug>` / `<issue>-fix-<slug>` branches and Conventional Commits. Preserve the current default branches (`develop` for the app; `main` for documentation/community); do not import another repository's branch names or promotion path without an approved migration. Reuse the issue branch throughout its scope.

The user reviews and merges pull requests manually. Do not merge or enable auto-merge on the user's behalf. Prepare concrete PRs and passing evidence before handing off; explain exact producer/consumer order. Independent website, documentation and community preparation may proceed together; published contract dependencies still gate consumers. Verify merged state, issue closure and project fields before setting Done.

Keep a concise durable checkpoint in the owning issue with exact revision, decisions, validation evidence, blockers and next action. GitHub owns lifecycle status; specifications do not duplicate a live board. Public content, domain configuration and payment setup are separate verifiable outcomes.

## Validation and publication

Use the narrowest relevant checks and run each equivalent suite once per candidate. Repeat only after relevant changes or failures. Keep complementary unit, contract, integration and browser/system acceptance. Use isolated Testcontainers for real runtime dependencies; use provider sandboxes and synthetic data, never real charges or customer environments in ordinary tests.

APIs and application frontends target 100% independently for statements, branches, functions and lines, with complete applicable E2E scenarios. Libraries/non-API workers retain a minimum 97% target. Qualification requires actual measurements; existing unmeasured scaffolds are not compliant merely because this policy exists. The public static website publication is a presentation-only bootstrap; it does not qualify or release the legacy authenticated application or future Go services. Record their gaps in their owning migration work.

Documentation-only changes require a strict documentation build rather than artificial runtime tests. Static website publication requires all locale catalogs, builds, public artifact checks and browser acceptance of the changed public journeys. No authenticated/API/customer-console routes may enter Pages artifacts. No production Node.js server is deployed by this website build.

Pin third-party actions and reusable workflows by full commit SHA. Preserve dependency lockfiles and pin runtime versions. Keep secrets out of source, YAML, output, logs, screenshots and checkpoints. AppleDouble `._*`, generated files and dependency copies must not be committed or published. Scope metadata cleanup to confirmed project/output directories and never traverse Git metadata.

Sponsors links must use a verified live destination; an informational funding page is not proof of payment activation. Stripe/account onboarding, payouts and approval remain separate from website publication. CNCF affiliation must not be claimed before actual acceptance and required agreements.
