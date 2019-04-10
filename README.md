# N2Container
# Setting up on local machine with minikube
## Prerequisites

- minikube installed (https://github.com/kubernetes/minikube/releases)
- kubectl installed (https://kubernetes.io/docs/tasks/tools/install-kubectl/#install-kubectl)

## Set up

### Start Cluster

```
minikube start
```

### Check status

```
minikube status
```

Should return 

```
minikube: Running
cluster: Running
kubectl: Correctly Configured: pointing to minikube-vm at 192.168.99.102
```

Services can be reached at this ip address after successful deployment

### Setup Services

cd into folder /deploy/local_minikube/

```bash
kubectl apply -f mongo_small.yaml
kubectl apply -f vinnsl-service.yaml
kubectl apply -f vinnsl-nn-ui.yaml
kubectl apply -f mongo-storage-service.yaml
kubectl apply -f vinnsl-storage-service.yaml
kubectl apply -f vinnsl-nn-worker.yaml
kubectl apply -f vinnsl-nn-worker-python.yaml
kubectl apply -f vinnsl-nn-worker-js.yaml
```

### Enable Service Discovery with Ingress

```
kubectl apply -f ingress.yaml
```

### Check status with Dashboard

```
minikube dashboard
```

This commands opens the dashboard and lets you check the status of the services. This can take a few minutes.

## Usage

```
kubectl get pods
```
