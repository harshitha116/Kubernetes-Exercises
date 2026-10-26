
# Exercise 3: Scaling Flask with ReplicaSets

## Objective
Deploy a Flask flash-sale application and understand
ReplicaSets, scaling, and self-healing in Kubernetes.

## Files Created
- app.py
- Dockerfile
- flashsale-replicaset.yaml

## Commands Used
```powershell
kubectl apply -f .\Exercise-03-ReplicaSet-Scaling\flashsale-replicaset.yaml
kubectl get rs
kubectl get pods -l app=flashsale
kubectl scale rs flashsale-rs --replicas=5
kubectl delete pod YOUR-POD-NAME
kubectl get pods -l app=flashsale
kubectl get pods -o wide
```

## Result
Successfully scaled the ReplicaSet from 3 to 5 Pods.
After deleting one Pod, Kubernetes automatically
created a replacement and maintained 5 Pods.
