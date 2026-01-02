# Speedtest Tracker

See docs here: [https://docs.speedtest-tracker.dev/](https://docs.speedtest-tracker.dev/)

```bash
flux reconcile --kubeconfig ../kubeconfig kustomization --with-source speedtest -n flux-system
```

```bash
flux reconcile --kubeconfig ../kubeconfig helmrelease --with-source postgres-cluster -n speedtest
```