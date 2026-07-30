# budget-navigator

> Capacity Planners coordinate forecast error budget burn for shared platform dependencies, so runbooks prove they still match production.

**Domain:** sre | **Complexity:** intermediate | **Stack:** Go, Prometheus, Grafana, Chaos Mesh, Argo Rollouts, OTel

| | |
|---|---|
| Use case | Capacity Planners coordinate forecast error budget burn for shared platform dependencies, so runbooks prove they still match production. |
| Pain point | Teams discover runbooks are stale during the incident, not before it. |
| Success metric | Warn 30 minutes before projected budget exhaustion and auto-freeze risky deploys. |
| Cost | $0/mo on Render |

## Why this exists

Teams discover runbooks are stale during the incident, not before it.. Capacity Planners coordinate forecast error budget burn for shared platform dependencies, so runbooks prove they still match production.

> This production platform is designed for reliability, error budgets, and repeatable recovery drills. For this implementation, the service is designed to remove the operational friction behind Capacity Planners coordinate forecast error budget burn for shared platform dependencies, so runbooks prove they still match production..

## What this product does

This project ships a production-oriented service that exposes health, readiness, observability, and domain-specific endpoints for Capacity Planners coordinate forecast error budget burn for shared platform dependencies, so runbooks prove they still match production.. The implementation is intended to be deployed behind Kubernetes with secure defaults, CI validation, and rollback-ready manifests.

## Quick start

```bash
docker build -t budget-navigator:local .
docker run -p 8080:8080 budget-navigator:local
curl http://localhost:8080/healthz
```

## Architecture

```
GitHub CI -> Container Registry -> Kubernetes -> Go -> Operators / SRE
```

See `docs/ARCHITECTURE.md`

## Infrastructure

Full spec: `terraform/INFRA_REQUIREMENTS.md`

TL;DR: K8s cluster, 2-10 pods HPA, $0 on Render

## Docs

- `docs/ARCHITECTURE.md` - components, tradeoffs
- `docs/DESIGN_DISCUSSION.md` - how we decided to build this
- `docs/DEPLOYMENT.md` - GitOps, rollback
- `docs/SECURITY.md` - threat model
- `docs/TROUBLESHOOTING.md` - 3am runbook
- `terraform/INFRA_REQUIREMENTS.md` - **infra: CPU/RAM/storage/cost**

Interview prep: `interview/`
