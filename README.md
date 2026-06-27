# Notes
Initial setting up
```sh
kubectl apply -f homeLAB/gitOps/bootstrap/root-app.yaml
```

Vault first startup, keys generation
```sh
kubectl -n vault exec -it vault-0 -- vault operator init
```
Unseal (run 3 times)
```sh
kubectl exec -n vault -it vault-0 -c vault -- vault operator unseal
```