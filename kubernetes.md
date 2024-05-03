# Kubernetes

<!-- TOC -->
* [Kubernetes](#kubernetes)
  * [Applications used](#applications-used)
  * [Helpers](#helpers)
<!-- TOC -->


## Applications used
1. minikube: manage local k8s clusters
2. kubectl: controls a k8s cluster

## Installing using `asdf`

Install `asdf`

Update plugins list
```bash
asdf plugin update --all
```

Install `kubectl` 
```bash
asdf plugin add kubectl
```

Install `minikube`
```bash
asdf plugin add minikube
```

## Helpers

### Manage local cluster

Starts a local Kubernetes cluster
```bash
minikube start
```
Stops a local kubernetes cluster
```bash
minikube stop
```
Deletes a local kubernetes cluster
```bash
minikube delete
```
### Addons
Enable addons
```bash
minikube addons enable <addon>
```
Disable addons
```bash
minikube addons disable <addon>
```

Starts a dashboard to help to manage the cluster
```bash
minikube dashboard
```
Creates a deployment
```bash
kubectl create deployment <deployment-name> \
  --image=<image-path>
```
Exposes a pod
```bash
kubectl expose deployment <deployment-name> \
  --type=LoadBalancer \ 
  --port=8080
```

## Utilities

### Metrics

Enable metrics server
```bash
minikube addons enable metrics-server 
```

Disable metrics server
```bash
minikube addons disable metrics-server 
```

Pods metrics
```bash
kubectl top pods
```

Nodes metrics
```bash
kubectl top node
```
