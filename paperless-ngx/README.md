# Paperless-ngx

https://docs.paperless-ngx.com/setup/

## Reconcile

```bash
flux --kubeconfig ../kubeconfig reconcile kustomization --with-source paperless-ngx -n flux-system
```