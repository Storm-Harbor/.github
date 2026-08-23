<div align="center">
  <img src="./assets/storm-harbor-banner.svg" width="100%" alt="Storm Harbor — Recovery stops being a promise." />
</div>

<div align="center">
  <a href="https://github.com/Storm-Harbor/storm-harbor-app/blob/develop/LICENSE"><img alt="License: Apache 2.0" src="https://img.shields.io/badge/license-Apache%202.0-326CE5?style=flat-square"></a>
  <a href="https://github.com/Storm-Harbor/storm-harbor-control-plane/actions/workflows/disaster-recovery-simulation.yml"><img alt="DR simulation workflow" src="https://img.shields.io/github/actions/workflow/status/Storm-Harbor/storm-harbor-control-plane/disaster-recovery-simulation.yml?branch=main&style=flat-square&label=DR%20simulation"></a>
  <img alt="Project status: safe simulation" src="https://img.shields.io/badge/status-safe%20simulation-0B7285?style=flat-square">
</div>

<br />

**Storm Harbor** is an open-source continuous disaster-recovery readiness platform. It connects code, cloud, clusters, backups, and policy into a continuously reconciled view of what can recover — and what stands in the way.

Repositories describe intent. APIs expose actual state. Backups live elsewhere. Evidence is scattered across pipelines and tickets. Storm Harbor brings those signals together to answer one operational question:

> **Can this service recover now, within its agreed RTO and RPO?**

## From signals to recovery proof

| | Stage | Outcome |
|:--:|---|---|
| **01** | **Observe** | Discover authorized repositories, cloud assets, clusters, backups, and policies. |
| **02** | **Assess** | Connect dependencies and compare current state with criticality, RTO, and RPO. |
| **03** | **Exercise** | Freeze an immutable plan and run it through approvals, guardrails, and health gates. |
| **04** | **Prove** | Preserve signed results outside the recovered failure domain. |

## Federated by design

Storm Harbor does not replace the tools that already own your infrastructure. Each domain remains authoritative while the control plane builds a current operational model with provenance and freshness.

```text
 Authoritative sources              Storm Harbor                 Recovery & proof

 GitHub · Terraform ───────┐     ┌────────────────────┐     ┌── GCP foundation
 Google Cloud APIs ────────┼────►│ Discover · Assess  │────►├── Databases · GKE
 Kubernetes · FluxCD ──────┤     │ Orchestrate · Prove│     ├── Workloads
 Policies · Backups ───────┘     └────────────────────┘     └── Signed evidence
                                         │
                         runs outside the recovery target
```

### The principles behind the platform

| | |
|---|---|
| **Federated authority**<br/>Git, cloud APIs, vaults, and evidence stores retain ownership of their domains. | **Ephemeral identity**<br/>OIDC and workload identity replace persistent cloud keys. |
| **Fail closed**<br/>Missing evidence, stale data, or policy failure never appears healthy. | **Evidence first**<br/>Inputs, decisions, actors, actions, timing, and outcomes remain linked and auditable. |

## Explore Storm Harbor

| Repository | What you will find |
|---|---|
| [**storm-harbor-control-plane**](https://github.com/Storm-Harbor/storm-harbor-control-plane) | Architecture, contracts, safe recovery simulations, evidence, technical documentation, and the delivery roadmap. |
| [**storm-harbor-app**](https://github.com/Storm-Harbor/storm-harbor-app) | The multilingual product website, identity flows, and the emerging customer control-plane experience. |

Start with the [product overview](https://github.com/Storm-Harbor/storm-harbor-control-plane/blob/main/docs/product/overview.md), continue through the [control-plane architecture](https://github.com/Storm-Harbor/storm-harbor-control-plane/blob/main/docs/architecture/control-plane.md), or inspect the [roadmap](https://github.com/Storm-Harbor/storm-harbor-control-plane/blob/main/docs/roadmap.md).

> [!IMPORTANT]
> **Storm Harbor is currently an architecture and safe-simulation scaffold, not a production recovery engine.** The existing workflows exercise contracts, ordering, guardrails, and evidence without cloud credentials or changes to external resources. Real operations remain gated by the published security and readiness criteria.

## Build with us

We are shaping the contracts, safeguards, and operating model before enabling privileged recovery. Contributions that improve the architecture, threat model, adapter boundaries, simulations, evidence, documentation, or developer experience are welcome.

- Read the [contribution expectations](https://github.com/Storm-Harbor/storm-harbor-control-plane#contributing).
- Explore [open issues](https://github.com/Storm-Harbor/storm-harbor-control-plane/issues).
- Review the [security architecture](https://github.com/Storm-Harbor/storm-harbor-control-plane/blob/main/docs/architecture/security.md).

<div align="center">
  <sub>Open source under Apache 2.0 · GCP-first · Built by <a href="https://ioterax.com">iot.EraX</a></sub>
</div>
