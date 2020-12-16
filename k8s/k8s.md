## Prerequesites

- kubectl (https://v1-18.docs.kubernetes.io/docs/tasks/tools/install-kubectl/)
- minikube (https://minikube.sigs.k8s.io/docs/start/)

## Start k8s 

```
minikube start

kubectl apply -f .\client.yml
kubectl apply -f .\server.yml
kubectl apply -f .\mongo-pv.yml
kubectl apply -f .\mongo.yml

kubectl port-forward service/server 3001:3001
kubectl port-forward service/client 8080:8080
```
