# Exercise 10: Multi-Node Kubernetes Cluster with Multiple Applications and Replicasets

## Objective
Deploy two Flask applications on a three-node Minikube Kubernetes cluster using Docker images, Deployments, Services, replicas, and pod anti-affinity.

## Applications
- **Product Catalog:** Provides a `/products` endpoint that returns product details in JSON format.
- **Shopping Cart:** Provides `GET /cart` to retrieve cart items and `POST /cart` to add items.

## Technologies Used
- Docker
- Kubernetes
- Minikube
- Python
- Flask
- YAML

## Kubernetes Configuration
- Cluster: `devops-multinode`
- Nodes: 3
- Product Catalog replicas: 2
- Shopping Cart replicas: 3
- Services: NodePort
- Pod anti-affinity: Configured to spread replicas across different nodes.

## Files
- `product_catalog.py`
- `shopping_cart.py`
- `Dockerfile.product`
- `Dockerfile.shopping`
- `product-catalog-deployment.yaml`
- `shopping-cart-deployment.yaml`
- `product-catalog-service.yaml`
- `shopping-cart-service.yaml`

## Verification
- Both Docker images were built and loaded into Minikube.
- All five application pods were observed in the Running state.
- Both Kubernetes Services were created.
- The Product Catalog endpoint returned the product list.
- The Shopping Cart GET endpoint returned an empty cart initially.
- A POST request successfully added a Laptop item to the cart.

## Note
The Shopping Cart stores items in memory, so its data is not persistent across pod restarts and may differ between replicas.

## Conclusion
The two Flask applications were successfully deployed and tested on a three-node Minikube cluster using Kubernetes Deployments and NodePort Services.