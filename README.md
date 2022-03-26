# argocd-examples

## Setup ArgoCD

```sh
helm repo add argo https://argoproj.github.io/argo-helm
helm repo update
kubectl create ns argocd
helm upgrade --install --namespace argocd argocd argo/argo-cd -f argocd-install/values.yaml -f argocd-install/github-personal-access-token.yaml
helm upgrade --install --namespace argocd argo-rollouts argo/argo-rollouts
```

## Preview Pull Requests

1. Create a Pull Request
1. Watch ArgoCD deploy a new application from the PR
1. Merge PR
1. ArgoCD deletes the PR application?
