## Prerequesites

- kubectl (https://v1-18.docs.kubernetes.io/docs/tasks/tools/install-kubectl/)
- minikube (https://minikube.sigs.k8s.io/docs/start/)

## Start k8s 

```bash
minikube start

kubectl create secret generic mongo-secret --from-literal=username=<username> --from-literal=password=<password>
# kubectl create secret generic mongo-secret --from-file=username=./username.txt --from-file=password=./password.txt

kubectl apply -f mongo-pv.yml
kubectl apply -f mongo.yml
kubectl apply -f server.yml
kubectl apply -f client.yml

# kubectl port-forward service/mongo 27017:27017 # This port forward is only needed if you want to inspect the database
kubectl port-forward service/server 3001:3001
kubectl port-forward service/client 8080:8080
```
