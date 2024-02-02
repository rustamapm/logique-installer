# How to Install ArgoCD & Istio
This step running on VM Bastion and already pull logique-installer Repository

### Connect GKE Cluster

```yaml
- gcloud container clusters get-credentials logique-cluster --region asia-southeast2 --project logique-devops
```

### Install ArgoCD

```yaml
- cd logique-installer/argocd
- kubectl apply -f argocd.yaml
```


### Istio

```yaml
- cd logique-installer/istio/istio-1.20.2
- export PATH=$PWD/bin:$PATH
- istioctl install -f istio.yaml
```