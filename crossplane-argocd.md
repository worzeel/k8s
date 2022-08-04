# crossplane

https://crossplane.io

## Installation

First install everything required - https://crossplane.io/docs/v1.9/getting-started/install-configure.html

1. ```kubectl create ns crossplane-system```
2. * ```helm repo add crossplane-stable https://charts.crossplane.io/stable```
3. * ```helm repo update```
4. ```helm install crossplane --namespace crossplane-system crossplane-stable/crossplane```

### Install CLI

* ```curl -sL https://raw.githubusercontent.com/crossplane/crossplane/master/install.sh | sh```

# ArgoCD

https://argoproj.github.io/cd/

## Installation

1. ```kubectl create ns argocd```
2. ```kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml```
3. ```kubectl -n argocd get secret argocd-initial-admin-secret -o jsonpath="{.data.password}" | base64 -d; echo```
4. ```kubectl port-forward svc/argocd-server -n argocd 50443:443```
5. ```argocd login localhost:50443```
   Login with admin:<password from above>
6. ```argocd account update-password```
