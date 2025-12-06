# Cloudnative Postgres

See docs here: [https://cloudnative-pg.io/](https://cloudnative-pg.io/)

```bash
flux reconcile --kubeconfig ../kubeconfig kustomization --with-source controllers -n flux-system
```

## Deploy a postgres DB cluster

Create a `kustomization.yaml` and add the `./cluster` folder as a resource-path.

Make sure to configure any changes as a patch.

The operator will create secrets you can use to read user, auto-created passwords and connect-strings from.
