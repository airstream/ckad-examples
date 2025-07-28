## taints-tolerations

> get

$ kubectl describe node node1 | grep Taint

> declarate taint node

$ kubectl taint node <node_name> key=value:effect

$ kubectl taint node node1 spray=mortein:NoSchedule

- NoExecute
- NoSchedule
- PreferNoSchedule

in yaml code:
```yaml
apiVersion: v1
kind: Pod
metadata:
  name: nginx
spec:
  containers:
  - name: nginx
    image: nginx
  tolerations:
  - key: "key1"
    operator: "Equal"
    value: "value1"
    effect: "NoSchedule"
```

$ kubectl get pods -o wide
