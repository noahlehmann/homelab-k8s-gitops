# Wireguard

See docs here: [https://github.com/wg-easy/wg-easy/wiki/Using-WireGuard-Easy-with-Kubernetes](https://github.com/wg-easy/wg-easy/wiki/Using-WireGuard-Easy-with-Kubernetes)

```bash
flux reconcile --kubeconfig ../kubeconfig kustomization --with-source wireguard -n flux-system
```