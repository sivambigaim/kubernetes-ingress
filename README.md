# kubernetes-ingress
**K3S Ingress using Traefik with Node Port**

Cluster: A set of servers managed by Kubernetes that run Pods.
Ingress: A Kubernetes Ingress exposes HTTP and HTTPS traffic from outside the Cluster to Services within the cluster.
Ingress Controller: An application that is responsible for fulfilling Ingress requests.
Service: A Kubernetes Service is an abstract way to expose an application running in a set of Pods. Implementations of a Service include NodePort and ClusterIP.
Pod: A group of one or more containers that share network and storage resources. Containers of a Pod are co-located and co-scheduled.
K3s: A lightweight Kubernetes distribution.
Container: A standardized unit of software that can run reliably on any server within the cloud.

Create deployment
kubectl create -f deployment.yaml

Create service
kubectl create -f service.yaml

Create ingress
kubectl create -f ingress.yaml

