# Setup Docker Desktop
1. [Download Docker Desktop for Mac](https://docs.docker.com/desktop/install/mac-install/)
2. Drag and drop the docker desktop to /Applications folder

# Start Kubernetes Service
1. Open `Docker Dashboard`
2. Go to `Settings`
3. Click the `Kubernetes` tab in the sidebar
4. Click the checkbox next to the `Enable Kubernetes`

# Create Deployment
Assume #name is deployment name = hello-k8s

Create deployment with specify Docker Hub image
1. kubectl create deployment #name --image nginx

Show running pod
2. kubectl get pods

Expose ports
3. kubectl expose deployment #name --port=8080

Binding local network port to container network port
4. kubectl port-forward service/#name 8081:8080 &

Test connection
5. curl localhost:8081

# Run with Kubernetes Template
kubectl apply -f #file_name.yml

# Checking
## Machine Node
kubectl get nodes
kubectl describe node #node_name

## Machine Node Services
kubectl get services
kubectl describe node #service_name

## Deployment
kubectl get deployments
kubectl describe deployment #deployment_name

## POD
kubectl get pods
kubectl describe pod #pod_name
