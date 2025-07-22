## requests-limits
---
```yaml
apiVersion: v1
kind: Pod
metadata:
  name: myapp-pod-color
  labels:
    app: myapp-pod
spec:
  containers:
    - name: nginx-container
      image: nginx
      resources:
        requests:
          memory: "64Mi"
          cpu: "250m"
        limits:
          memory: "128Mi"
          cpu: "1"
```
