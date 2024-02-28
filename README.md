## helloworld example with k8s ingress
### setup ingress controller
kubectl apply -f https://raw.githubusercontent.com/kubernetes/ingress-nginx/controller-v1.1.0/deploy/static/provider/cloud/deploy.yaml
### setup ingress object
kubectl apply -f minimal-ing.yaml
### setup helloworld deployment and service
kubectl create -f minimal-helloworld.yaml