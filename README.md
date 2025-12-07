# homelab-k8s-gitops

```bash
flux bootstrap github \
  --token-auth \
  --owner=noahlehmann \
  --cluster-domain cluster.local \
  --repository=homelab-k8s-gitops \
  --branch=main \
  --path=clusters/homelab \
  --personal \
  --kubeconfig kubeconfig
```

## SOPS

### Key Generation

Generate the key.

```bash
age-keygen -o age.agekey
```

### SOPS Configuration

Create the secret with the default sops secret name in the `flux-system` namespace.

```bash
cat age.agekey |
kubectl create secret generic sops-age \
    --kubeconfig ./kubeconfig \
    --namespace=flux-system \
    --from-file=age.agekey=/dev/stdin
```

Encrypt files with public key like follows:

```bash
sops --encrypt --in-place --config clusters/homelab/sops/.sops.yaml <path-to-file>
```

Or edit files in place (if key is still available):

```bash
SOPS_EDITOR=nano SOPS_AGE_KEY_FILE=age.agekey sops <path-to-secret>
```
