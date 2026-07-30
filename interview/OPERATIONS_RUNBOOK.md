# Operations Runbook - budget-navigator

Capacity Planners coordinate forecast error budget burn for shared platform dependencies, so runbooks prove they still match production.

**On-call? Read this first.**

## Deploy
```
kubectl apply -k k8s/ -n budget-navigator
kubectl rollout status deploy/budget-navigator -n budget-navigator
```

## Rollback (when things go red)
```
./scripts/rollback.sh
# usually < 30sec
```

## Scale up NOW
```
kubectl scale deploy/budget-navigator --replicas=10 -n budget-navigator
```

## Logs
```
kubectl logs -l app=budget-navigator -n budget-navigator -f --tail=200
```

## Crashloop?
```
kubectl describe pod -l app=budget-navigator -n budget-navigator
kubectl logs <pod> --previous -n budget-navigator
```
90% of the time: missing env var in ConfigMap.

## Metrics
`curl localhost:8080/metrics` or Grafana dashboard in `monitoring/`

## DR / Failover
See `docs/DISASTER_RECOVERY.md` - RTO 15m

We actually tested this. 11 min.
