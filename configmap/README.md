## ConfigMaps

Flow:
1. Create ConfigMap
2. Inject into pod

> create

**Imperative way**

$ kubectl create configmap app-config --from-literar=NAME=test

$ kubectl create configmap app-configg --from-file=app_config.properties

**Declarative way**

$ kubectl create -f configmap.yml

> get

$ kubectl get configmaps

> describe

$ kubectl describe configmaps

