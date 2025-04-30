# Node.js Docker Deployment & Kubernetes Network Policy

## Task1: Simple Node.js Application Deployment on Docker

### Description
This Node.js app listed on port 3000. It's containerized using Docker with a lightweight base image.

### Files:
- `Dockerfile`
- `app.js`
- `package.json`


### Setup & Execution:
1. Build the Docker image:
	`bash docker build -t my-done-app .`

### Run the Container:
	docker run -p 3000:3000 my-node-app


# Kubernetes Network Policy

### Description
This defines a NetworkPolicy tha restricts traffic for my-app-deployment as follow:
* Allow incoming traffic from pods in same namespace.
* Allow from a pod with app=trusted.
* Allow outgoing traffic to same namespace.
* Deny Everything else.

### Files:
- `my-app-deployment.yaml`
-  `my-app-service.yaml`
-  `cache-deploymnet.yaml`
-  `my-app-network-policy`


### Apply on Kubernetes:
kubectl appy -f k8s/
