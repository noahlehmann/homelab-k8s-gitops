# Wireguard

See docs here: [https://github.com/wg-easy/wg-easy/wiki/Using-WireGuard-Easy-with-Kubernetes](https://github.com/wg-easy/wg-easy/wiki/Using-WireGuard-Easy-with-Kubernetes)

```bash
flux reconcile --kubeconfig ../kubeconfig kustomization --with-source wireguard -n flux-system
```

## App Password

See: [https://github.com/wg-easy/wg-easy/blob/v14/How_to_generate_an_bcrypt_hash.md](https://github.com/wg-easy/wg-easy/blob/v14/How_to_generate_an_bcrypt_hash.md)

```bash
docker run ghcr.io/wg-easy/wg-easy:14 wgpw YOUR_PASSWORD
```
