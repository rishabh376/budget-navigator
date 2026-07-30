# FAQ - budget-navigator

**Q: What problem does this actually solve?**
A: Capacity Planners coordinate forecast error budget burn for shared platform dependencies, so runbooks prove they still match production.

Pain point: Teams discover runbooks are stale during the incident, not before it.

**Q: Free to run?**
A: Yep. Render - $0/mo. See `terraform/INFRA_REQUIREMENTS.md`

**Q: Production ready?**
A: Yes - SLOs, security hardening, DR runbook, Helm, Terraform, monitoring.

**Q: Stack?**
A: Go, Prometheus, Grafana, Chaos Mesh, Argo Rollouts, OTel

**Q: What infra do I need?**
A: `terraform/INFRA_REQUIREMENTS.md` has the full breakdown - CPU/RAM/storage/network/cost.
