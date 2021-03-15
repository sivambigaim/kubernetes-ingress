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

Get the traefik Load balancer service ip address using kubectl get svc -n kube-system
The output will be like below
NAME                 TYPE           CLUSTER-IP      EXTERNAL-IP                 PORT(S)                      AGE
kube-dns             ClusterIP      10.43.0.10      <none>                      53/UDP,53/TCP,9153/TCP       18d
metrics-server       ClusterIP      10.43.5.91      <none>                      443/TCP                      18d
traefik-prometheus   ClusterIP      10.43.157.167   <none>                      9100/TCP                     18d
traefik              LoadBalancer   10.43.207.20    10.200.3.69,10.200.46.112   80:32640/TCP,443:31113/TCP   18d

Using http://10.200.3.69/ will load the ngnix welcome page
