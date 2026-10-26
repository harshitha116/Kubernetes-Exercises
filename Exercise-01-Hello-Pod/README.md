
# Exercise 1: Kubernetes Hello Pod

## Objective
Deploy an Nginx Pod on Kubernetes using Minikube.

## Commands Used

```bash
kubectl run hello-k8s --image=nginx --port=80
kubectl get pods
kubectl expose pod hello-k8s --type=NodePort --port=80
minikube service hello-k8s
```

## Result
Successfully deployed Nginx on Minikube and opened
the Nginx welcome page in the browser.
