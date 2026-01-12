# Kube-Prom-Stack

```bash
flux --kubeconfig ../kubeconfig reconcile kustomization --with-source monitoring -n flux-system
```

```bash
flux --kubeconfig ../kubeconfig reconcile helmrelease --with-source kube-prom -n prometheus
```

## Documentation

Kube-prom-stack: [https://github.com/prometheus-community/helm-charts/tree/main/charts/kube-prometheus-stack](https://github.com/prometheus-community/helm-charts/tree/main/charts/kube-prometheus-stack)

## Alertmanager

Reference: [https://prometheus.io/docs/alerting/alertmanager/](https://prometheus.io/docs/alerting/alertmanager/)

## Grafana

Helm Values: [https://github.com/grafana/helm-charts/blob/main/charts/grafana/values.yaml](https://github.com/grafana/helm-charts/blob/main/charts/grafana/values.yaml)