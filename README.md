# argocd-examples

## Setup ArgoCD

```sh
helm repo add argo https://argoproj.github.io/argo-helm
helm repo update
kubectl create ns argocd
helm upgrade --install --namespace argocd argocd argo/argo-cd -f argocd-install/values.yaml
helm upgrade --install --namespace argocd argo-rollouts argo/argo-rollouts
```
