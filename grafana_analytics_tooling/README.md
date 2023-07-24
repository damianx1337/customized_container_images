Contains analytics tools for Grafana:
- mimirtool (v2.9.0)
- adaptive-cli (https://grafana.com/docs/grafana-cloud/data-configuration/metrics/manage-metrics-costs-via-adaptive-metrics/?pg=prometheus-cardinality-optimization&plcmt=resources#use-the-adaptive-metrics-cli)

$: kubectl apply -f pod.yaml
$: kubectl -n default exec -it grafana-analytics-pod grafana-analytics -- /bin/bash
