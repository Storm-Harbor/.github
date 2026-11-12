<div align="center">
  <img src="./assets/storm-harbor-banner-v2.svg" width="100%" alt="Storm Harbor — Recovery stops being a promise." />
</div>

**Storm Harbor** is an open-source, declarative recovery control plane for private projects and multicloud environments. Discover dependencies, evaluate readiness, plan and exercise recovery, then restore environments through authorized, auditable reconciliation.

[Product website](https://storm-harbor.github.io/storm-harbor-app/) · [English documentation](https://storm-harbor.github.io/storm-harbor-control-plane/) · [Roadmap](https://storm-harbor.github.io/storm-harbor-control-plane/roadmap/) · [Support the project](https://storm-harbor.github.io/storm-harbor-control-plane/community/sponsorship/)

## Your environment remains yours

Any organization can connect explicitly authorized private repositories and infrastructure without making projects public. iot.EraX is the creator and an initial consumer; its identity, cloud and knowledge services are optional integrations.

Cloud adapters target **AWS, Azure, DigitalOcean, Oracle Cloud and GCP**. A journey can span providers, with explicit compatibility checks for data, identity, networking and service recovery. No managed service is assumed portable simply because its resource has a common name.

## A declarative journey

**Configure → discover → inventory → plan → validate → simulate → approve → recover → verify → reconcile.**

Versioned YAML drives the guided interface and CLI. The control plane observes actual state and reconciles it with declared intent, freezes the exact execution plan and records evidence outside the recovered failure domain.

- **Go 1.26.x** for runtime applications, APIs, operators/controllers, agents, CLIs and SDKs.
- **Extensible resources and controllers**, including native Kubernetes CRDs through the Kubernetes adapter.
- **Project-owned AI/RAG/CLI**, with private knowledge and authorized minimal results; no mandatory AI service.
- **Private organization/project scopes**, short-lived permissions, approval gates, idempotency and interruptible execution.

The public product website supports ten locales. Technical documentation is maintained in English.

## Current status

**Storm Harbor currently provides documentation, a GCP-specific configuration example and safe Node.js simulations.** The Go runtime, production cloud adapters, extension registry and installable Kubernetes CRDs are planned. The Next.js authentication/BFF scaffold is transitional; the public website is deployed as static content without a Node.js production server.

No cloud credentials or external infrastructure mutations are performed by the existing mock workflows. The project is not currently affiliated with CNCF. See the evidence-based [CNCF readiness plan](https://storm-harbor.github.io/storm-harbor-control-plane/community/cncf-readiness/).

## Repositories and community

| Repository | Responsibility |
| --- | --- |
| [storm-harbor-control-plane](https://github.com/Storm-Harbor/storm-harbor-control-plane) | English technical documentation, architecture, schemas and safe simulation contracts |
| [storm-harbor-app](https://github.com/Storm-Harbor/storm-harbor-app) | Multilingual public website and transitional application scaffold |
| [.github](https://github.com/Storm-Harbor/.github) | Organization profile, maintainers, contribution/conduct/security policies and funding information |

Read the [contribution guide](https://github.com/Storm-Harbor/.github/blob/main/CONTRIBUTING.md), [maintainer roster](https://github.com/Storm-Harbor/.github/blob/main/MAINTAINERS.md) and [security policy](https://github.com/Storm-Harbor/.github/blob/main/SECURITY.md). Public contributions and fixtures must not disclose customer repositories, knowledge or operational evidence.

Open source under Apache 2.0 · Created by [iot.EraX](https://ioterax.com)
