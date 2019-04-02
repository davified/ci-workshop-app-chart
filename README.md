### Steps
```sh
# start kubernetes cluster locally
minikube start

helm init

# release helm chart
helm install --name ci-workshop-app .

# wait for pods to be ready:
watch kubectl get all

# to apply rolling updates:
helm upgrade ci-workshop-app .

# to get local k8s cluster ip
minikube ip

# 
minikube dashboard
```