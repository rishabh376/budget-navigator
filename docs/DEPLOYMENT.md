# Deployment - budget-navigator

**Use case:** Capacity Planners coordinate forecast error budget burn for shared platform dependencies, so runbooks prove they still match production.

## Infra requirements
→ `terraform/INFRA_REQUIREMENTS.md` - CPU/RAM/storage/network/cost breakdown

## GitOps
Flux watches `main` and reconciles changes automatically.

## Rollback
```
./scripts/rollback.sh
kubectl rollout undo deploy/budget-navigator -n budget-navigator
```
Usually < 30 sec.

## Cost
Render - $0/mo

Reliability and safety go hand-in-hand: SLO guardrails, incident runbooks, and control-plane failure mode analysis.
