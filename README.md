how to start

# Start minikube
minikube start

# Set docker env
eval $(minikube docker-env)

# Build image
docker build -t mynode:test

# Run in minikube
kubectl run hello-foo --image=mynode:test --image-pull-policy=Never

# Check that it's running
kubectl get pods
