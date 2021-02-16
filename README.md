# What

Kubernetes manifests for deploying 7 Days to Die.

# How to deploy

Before deploying, replace <ExternalIP> to your IP in `k8s/services/tcp.yaml.examble` and `k8s/services/udp.yaml.example` please.

```
cd k8s
kubectl kustomize . | kubectl apply -f -
```

If you want to change the game configuration, edit `k8s/config/serverconfig.xml`.

# Use mods

Copy mods under `/7dtd/mods` via `kubectl cp` or something during the game conainer running and restart.
