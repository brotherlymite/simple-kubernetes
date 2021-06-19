## A simple deployment of TomCat application server on Kubernetes

For simplicity here we have deployed TomCat application server using the official docker image and have used only a single pod.
### Steps:
- Install Kubectl and Minikube
- Take the directives from the `deployment.yaml` file and apply it to our cluster `kubectl apply -f ./deployment.yaml`
- Expose the pod to the external world as service `kubectl expose deployment simple-kubernetes --type=NodePort`
- You can find out which port it was created on using `minikube service simple-kubernetes --url` which will return the URL including the port number through which we could access our service.
