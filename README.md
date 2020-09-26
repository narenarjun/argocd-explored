# ArgoCD Explored 

[Argo CD](https://argoproj.github.io/argo-cd/) is a declarative, GitOps continuous delivery tool for Kubernetes.

This repos contains a sample test done to feel the argos working and magics. 

First we need to install argoCD resources in the k8s cluster of our choice.

ArgoCD resources  should be installed in `argocd` namespace, so let's first create a argocd namespace.  


```
kubectl apply -f ./install/crt-namespace.yaml 
```
now, let's install the argoCD resources in the argocd namespace.

```
kubectl apply -f ./install/agro-install.yaml -n argocd
```

ArgoCD is configured to target the namespace `app-deploy`, so we must have this namespace already in existance.

```
kubectl create -n app-deploy
```