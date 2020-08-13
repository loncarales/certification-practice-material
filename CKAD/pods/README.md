# Practice Test - PODs

## Exercises

**How many PODs exist on the system?**

> in the current(default) namespace

`kubectl get pods`

**Create a new pod with the NGINX image**

> Image name: nginx

`kubectl run nginx --image=nginx`

**How many pods are created now?**

`kubectl get pods --no-headers | wc -l`

**What is the image used to create the new pods?**

`kubectl describe pod <pod_name>`

**Which nodes are these pods placed on?**

`kubectl get pods -o wide`

**How many containers are part of the pod 'webapp'?**

`kubectl describe pod webapp`

**Delete the 'webapp' Pod.**

`kubectl delete pod webapp`

**Create a new pod with the name 'redis' and with the image 'redis123'**

Use a pod-definition YAML file. And yes the image name is wrong!

> Name: redis, Image Name: redis123

`kubectl run redis --image=redis123 --dry-run=client -o yaml > redis.yaml`

`kubectl create -f redis.yaml`

Now fix the image on the pod to 'redis'.

`kubectl apply -f redis.yaml`


