# Contributing to Storm Harbor

Storm Harbor is an independent open-source, declarative multicloud recovery project. Any organization can contribute without publishing its private infrastructure or knowledge. Technical documentation and contribution discussions are maintained in English; the product website supports 25 locales.

Start with a scoped issue in the owning repository and link the implementation pull request to it. Describe the behavior, compatibility impact and relevant validation. Keep public fixtures synthetic and do not upload private repositories, knowledge bases, credentials, customer inventories or recovery evidence.

New runtime applications, APIs, controllers/operators, agents, CLIs and SDKs use Go 1.26.x. Website browser assets/build tools and the existing transitional simulations are documented exceptions pending migration. Keep cloud, identity and AI integrations behind versioned contracts.

Validate the relevant change once per equivalent test suite. Go implementations need formatting, vet, build and meaningful tests with race/coverage collected together; preserve complementary contract, integration and E2E validation. Resource/schema upgrades require compatibility fixtures. Documentation must pass a strict MkDocs build. Website changes must preserve all configured locale catalogs and exclude authenticated routes from Pages artifacts.

Real-operation changes must explain authorization, organization/project isolation, minimum ephemeral permissions, idempotency, approvals, cancellation, rollback/cleanup and expected evidence. AI output never grants execution authority. Follow the [platform contract](https://storm-harbor.github.io/storm-harbor-control-plane/architecture/platform-contract/).

Maintainers review contributions for scope, clarity, security and compatibility. Sponsorship grants no automatic merge rights or access to private project data. See [MAINTAINERS.md](MAINTAINERS.md) and [SECURITY.md](SECURITY.md).

## Branch and promotion flow

The default branch is `develop`; production is `master`. Create an issue branch from the fetched, updated `master`, name it `<issue>-feat-<english-slug>` or `<issue>-fix-<english-slug>`, and open its PR against `develop`. Maintainers merge manually. Promote accepted changes in a separate same-repository `develop` → `master` PR; feature/fix branches cannot target `master` directly. Production publication follows the promoted revision and successful checks. Do not force-push or delete long-lived branches.
