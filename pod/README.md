## pod-definition.yml
### get
$ kubectl get pods

$ kubectl get pods -o wide

### create
$ kubectl run --help

$ kubectl run nginx --image=nginx

$ kubectl run nginx --image=nginx --dry-run=client -o yaml > pod-definition.yml

$ kubectl create -f pod-definition.yml

### edit
>If you are not given a pod definition file

$ kubectl get pod -o yaml > pod-definition.yml

>To modify the properties of the pod, you can utilize the

$ kubectl edit pod 

>Editable properties:
> - spec.containers[*].image
> - spec.initContainers[*].image
> - spec.activeDeadlineSeconds
> - spec.tolerations
> - spec.terminationGracePeriodSeconds



### delete
$ kubectl delete pods myapp-pod

### info
$ kubectl describe pods myapp-pod
