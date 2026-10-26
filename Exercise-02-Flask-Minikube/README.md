
# Exercise 2: Deploy Flask on Minikube

## Objective
Deploy a Python Flask application on Kubernetes using Minikube,
Docker, kubectl, and YAML.

## Files Created
- app.py
- Dockerfile
- flask-deployment.yaml

## Commands Used
```powershell
docker build -t flask-app:latest .\Exercise-02-Flask-Minikube
minikube image load flask-app:latest
kubectl apply -f .\Exercise-02-Flask-Minikube\flask-deployment.yaml
kubectl get deployments
kubectl get pods -l app=flask-app
minikube service flask-app-service --url
```

## Result
Successfully deployed the Flask application on Minikube.
The browser displayed:
"Hello from Flask on Kubernetes!"
