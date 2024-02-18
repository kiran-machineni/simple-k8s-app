# Kubernetes Setup and Deployment

## Setup Kubernetes
1. Ensure Kubernetes is set up on your system, either on a cloud platform or a local machine.
2. Refer to the `SETUP.md` file for detailed instructions on installing Kubernetes.

## Check Cluster Context
```bash
kubectl config get-contexts
```
## Clone Repository

```bash
git clone https://github.com/kiran-machineni/simple-k8s-app
cd simple-k8s-app
```

## Deploying app into cluster

### Deploying pod
```bash
kubectl apply -f ./deployments/nodejs-app-deployment.yaml
```
### Check deployments
```bash
kubectl get deployments
```
### Check pods
```bash
kubectl get pods
```

### Deploying Service
```bash
kubectl apply -f ./services/nodejs-app-service.yaml
```
### Check Service
```bash
kubectl get services
```

### Port forwarding to test App

```bash
kubectl port-forward service/nodejs-app-service 8080:80
```
### Test App
```bash
curl http://localhost:8080
```