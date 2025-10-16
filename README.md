# Kubernetes-k8s
This Repository contains Kubernetes YML files and Commands for personal / Future and Refrence Use.

# Topics: <br/>
   1- Cluster <br/>
   2- Pod <br/>
   3- Deployment <br/>
   4- services <br/>
   5- Ingress <br/>
   6- ConfigMaps <br/>
   7- Secrets <br/>
   8- Persistent Volume <br/>
   9- Persistent Volume Claim <br/>
   10- Horizental Pod Autoscaling (HPA) <br/>
   11- Vertical pod Autoscaling (VPA) <br/>
   12- Namespace <br/>
   13- Cron Job <br/>


<h3>1- Cluster:</h3> <br/> 
A Cluster in Kubernetes is a group of machines (nodes) that work together to run containerized applications.
It consists of a control plane (manages the cluster) and worker nodes (run the applications). To create a cluster we write cluster.yml

<h3>2- Pod:</h3>
A Pod in Kubernetes is the smallest deployable unit that runs one or more containers together.
All containers inside a Pod share the same network (IP address) and storage (volumes). To create a pod we write pod.yml

<h3>3- Deployment:</h3>
A Deployment in Kubernetes is a controller that manages and maintains the desired number of Pod replicas.
It automatically handles updates, rollbacks, and scaling of Pods to keep your app running smoothly. To create a Deployment we write deployment.yml

<h3>4- Services:</h3>
A Service in Kubernetes is used to expose and connect Pods.
It provides a stable IP and DNS name so other apps or users can access the Pods even if their IPs change. To create a service we write service.yml

<h3>5- Ingress:</h3>
An Ingress in Kubernetes is used to manage external access to services, usually over HTTP or HTTPS.
It acts like a smart router, directing incoming traffic to the right service based on rules or URLs. To create a Ingress we write ingress.yml

<h3>6- configMaps:</h3>
A ConfigMap in Kubernetes is used to store non-confidential configuration data (like environment variables or settings).
It lets you separate configuration from code, so you can change app settings without rebuilding the image. To create a configMap we write configMaps.yml

<h3>7- Secrets:</h3>
A Secret in Kubernetes is used to store sensitive data like passwords, API keys, or tokens.
It keeps this data encrypted and secure, separate from your application code. To create a secret we write secret.yml

<h3>8- Presistent Volume (PV):</h3>
A Persistent Volume (PV) in Kubernetes is a piece of storage provisioned in the cluster (like a hard drive).
It allows data to persist even if a Pod is deleted or restarted. To create a Presistent Volume we write pv.yml

<h3>9- Presistent Volume Claim (PVC):</h3>
A Persistent Volume Claim (PVC) in Kubernetes is a request for storage made by a Pod.
It automatically binds to a suitable Persistent Volume (PV) that meets its storage requirements. To create a Presistent Volume Claim we write pvc.yml

<h3>10- Horizontal Pod Autoscaling (HPA):</h3>
Horizontal Pod Autoscaling (HPA) in Kubernetes automatically increases or decreases the number of Pods in a deployment.
It adjusts the Pod count based on CPU, memory, or custom metrics to match the app’s workload. To create a Horizontal Pod Autoscaling we create hpa.yml

<h3>11- Vertical Pod Autoscaling (VPA):</h3>
Vertical Pod Autoscaling (VPA) in Kubernetes automatically adjusts CPU and memory limits of Pods.
Instead of adding more Pods, it resizes existing ones to give them the right amount of resources. To create Vertical Pod Autoscaling we create vpa.yml

<h3>12- Namespace:</h3>
A Namespace in Kubernetes is used to divide a cluster into virtual environments.
It helps organize and isolate resources like Pods, Services, and Deployments within the same cluster. To create a Namespace we write namespace.yml

<h3>13- Cron Job:</h3>
A CronJob in Kubernetes is used to run tasks on a schedule, just like Linux cron.
It’s ideal for automated jobs like backups, report generation, or cleanup tasks at specific times. To create a Cron Job we write cronjob.yml



# Commands for Kubernetes

```bash
# Shows detailed information about a specific Pod (Pod Name) in the "mysql" namespace, including status, containers, events, and resource usage.
kubectl describe pod/Pod Name -n mysql
```

```bash
# Displays the logs/output of the specified Pod (Pod Name) in the "mysql" namespace.
kubectl logs pod/Pod Name -n mysql
```

```bash
# jab kubernetes ka cluster ma ya pounchti hai to wo isa binary ma convert kr ka store krta etcd ma yani mazeed secure kr deta.
echo -n "Admin123" | base64 
```

```bash
# Opens an interactive bash shell inside the specified Pod (Pod Name) in the given namespace.
kubectl exec -it pod name -n name space --bash
```

<h5>You have to install VPA (Vertical Pod Autoscalling) because ya pehla sa kubernetes ma install hoka nahi ata.</h5>

```bash
kubectl apply -f https://github.com/kubernetes/autoscaler/releases/latest/download/vertical-pod-autoscaler.yaml
```
