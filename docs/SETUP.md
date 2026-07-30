# Setup - budget-navigator

Capacity Planners coordinate forecast error budget burn for shared platform dependencies, so runbooks prove they still match production.

1. **Infra first**: `cd terraform && terraform init && terraform apply`
2. `kubectl apply -k k8s/ -n budget-navigator`
3. `kubectl port-forward svc/budget-navigator 8080:80 -n budget-navigator`
4. `curl localhost:8080/healthz`

Env vars: `PORT=8080`, `LOG_LEVEL=info`

We treat observability as a first-class citizen with alerts tuned to what actually matters in an outage.
