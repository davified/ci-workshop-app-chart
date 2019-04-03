# Helm chart for `ci-workshop-app`

This is the helm chart for https://github.com/ThoughtWorksInc/ci-workshop-app

### Steps to release app on minikube
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

### Resources

- https://docs.bitnami.com/kubernetes/how-to/create-your-first-helm-chart/
- https://helm.sh/docs/chart_template_guide/