## ConfigMaps

Flow:
1. Create Secret
2. Inject into pod

> create

**Imperative way**

$ kubectl create secret generic db-secret --from-literal=DB_Host=sql01 --from-literal=DB_User=root --from-literal=DB_Password=password123

$ kubectl create secret generic app-config --from-file=secret.properties

**Declarative way**

$ kubectl create -f secret.yml

> get

$ kubectl get db-secret

> get values in base64 format

$ k get secret db-secret -o yaml

> describe

$ kubectl describe secret db-secret

