# What

Kubernetes manifests for deploying 7 Days to Die.

# How to deploy

```
cd k8s
kubectl kustomize . | kubectl apply -f -
```

If you want to change the game configuration, edit `k8s/config/serverconfig.xml` please.

# Use mods

Copy mods under `/7dtd/mods` via `kubectl cp` or something during the game conainer running and restart.
