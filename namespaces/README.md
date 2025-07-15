## namespace-definition.yml
By default kubernetes use 3 namespaces: default, kube-system, kube-public

> get

$ kubectl get pods --namespace=dev

> create

$ kubectl create -f namespace-definition.yml

> define pod in **dev** namespace

using command

$ kubectl create -f pod-definition.yml --namespace=dev

using yaml define namespace under metadata, example:
```
...
metadata:
  name: myapp-pod
  namespace: dev
  labels:
    app: myapp
...
```

> permanently switch on dev namespace 

$ kubectl config set-context $(kubectl config current-context) --namespace=dev

> show information for all namespaces

$ kubectl get pods --all-namespaces

> limit namespaces resources with quota

$ kubectl create -f compute-quota.yml