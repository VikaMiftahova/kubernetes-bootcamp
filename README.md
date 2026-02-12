# 💙 Run kubernetes-bootcamp on Minikube
### Prerequisites 
  **kubectl \
  minikube**

## :star: 1) Start a local cluster:
```
minikube start
kubectl get nodes
```
### :computer: 2) Get the manifests
```
git clone https://github.com/VikaMiftahova/kubernetes-bootcamp
cd kubernetes-bootcamp
```
### :anchor: 3) Create namespace
```
kubectl create namespace -n bootcamp
```
### :ship: 4) Apply manifests
```
kubectl apply -f configmap.yaml -n bootcamp
kubectl apply -f secret.yaml -n bootcamp
kubectl apply -f deployment.yaml -n bootcamp
kubectl apply -f service.yaml -n bootcamp
```
### :runner: 5) Check statuses
```
kubectl get pods -n bootcamp
kubectl get svc -n bootcamp
kubectl describe pod <pod-name> -n bootcamp
kubectl logs -l app=<label-if-present> -n bootcamp
```

