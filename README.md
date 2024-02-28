## helloworld example with k8s ingress
### setup ingress controller
kubectl apply -f https://raw.githubusercontent.com/kubernetes/ingress-nginx/controller-v1.1.0/deploy/static/provider/cloud/deploy.yaml
### setup ingress object
kubectl apply -f minimal-ing.yaml
### setup helloworld deployment and service
kubectl create -f minimal-helloworld.yaml

### to see the helloworld webpage
You find the external IP of ingress-nginx-controller  
$ kubectl get svc -A
  
And access it with the below on the browser  
http://<external_ip>/testpath