# argocd-examples

## Setup ArgoCD

```sh
helm repo add argo https://argoproj.github.io/argo-helm
helm repo update
kubectl create ns argocd
helm install --namespace argocd argocd argo/argo-cd
helm install --namespace argocd argo-rollouts argo/argo-rollouts
```
