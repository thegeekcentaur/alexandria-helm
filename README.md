# Decomposing Alexandria into microservices on k3d/kubernetes

This repository contains a sample set of commands to deploy the Alexandria services in a kubernetes-based environment.

# Create persistent volume and persistent volume claims
```
kubectl apply -f books-deployment.yaml
kubectl apply -f catalogs-deployment.yaml
kubectl apply -f users-deployment.yaml
kubectl apply -f mongo-deployment.yaml
kubectl apply -f books-service.yaml
kubectl apply -f catalogs-service.yaml
kubectl apply -f users-service.yaml
kubectl apply -f mongo-service.yaml
```

## Useful commands

Scaling out

```
# First list all deployments
kubectl get deployments

# Now, when we want to increase replicas for deployment "books-mgmt" to 3
kubectl scale --replicas=3 deployment books-mgmt
```