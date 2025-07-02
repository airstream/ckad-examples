## pod-definition.yml
### get
$ kubectl get pods

$ kubectl get pods -o wide

### create
$ kubectl run --help

$ kubectl run nginx --image=nginx

$ kubectl run nginx --image=nginx --dry-run=client -o yaml > pod-definition.yml

$ kubectl create -f pod-definition.yml

### delete
$ kubectl delete pods myapp-pod

### info
$ kubectl describe pods myapp-pod
