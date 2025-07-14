## rs-definition.yml
> create

$ kubectl create -f rs-definition.yml

> get

$ kubectl get replicaset

> delete

$ kubectl delete replicaset myapp-replicaset

> scale 

> replace if change replica number, example from 3 to 6

$ kubectl replace -f rs-definition.yml

$ kubectl scale -replicas=6 -f myapp-replicaset
