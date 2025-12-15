# Kube-Prom-Stack

```bash
flux --kubeconfig ../kubeconfig reconcile kustomization --with-source monitoring -n flux-system
```

```bash
flux --kubeconfig ../kubeconfig reconcile helmrelease --with-source kube-prom -n prometheus
```