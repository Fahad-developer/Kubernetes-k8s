# Kubernetes-k8s
This Repository contains Kubernetes YML files and Commands for personal / Future and Refrence Use.

#Topics: <br/>
   1- Cluster <br/>
   2- Pod <br/>
   3- Deployment <br/>
   4- services <br/>
   5- Ingress <br/>
   6- ConfigMaps <br/>
   7- Secrets <br/>
   8- Persistent Volume <br/>
   9- Persistent Volume Claim <br/>
   10- Horizental Pod Autoscaling (HPA)


<h3>1- Cluster</h3> <br/>
A Cluster in Kubernetes is a group of machines (nodes) that work together to run containerized applications.
It consists of a control plane (manages the cluster) and worker nodes (run the applications).

# Commands for Kubernetes

kubectl describe pod/Pod Name -n mysql
kubectl logs pod/Pod Name -n mysql

echo -n "Admin123" | base64    => jab kubernetes ka cluster ma ya pounchti hai to wo isa binary ma convert kr ka store krta etcd ma yani mazeed secure kr deta.


kubectl exec -it pod name -n name space --bash

<h5>You have to install VPA (Vertical Pod Autoscalling) because ya pehla sa kubernetes ma install hoka nahi ata.</h5>
<h5>Command: </h5> kubectl apply -f https://github.com/kubernetes/autoscaler/releases/latest/download/vertical-pod-autoscaler.yaml

