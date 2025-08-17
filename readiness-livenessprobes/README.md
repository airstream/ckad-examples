## readiness-liveness probes

🟢 Readiness Probe

Purpose: Determines when a container is ready to accept traffic.

Effect: If the probe fails, the pod is removed from the Service’s endpoints, meaning it will not receive any traffic.

🔴 Liveness Probe

Purpose: Detects if a container is still running properly.
    
Effect: If the probe fails, Kubernetes restarts the container.

🧪 Probe Types (common to both)
* HTTP: Kubernetes sends an HTTP request to a specified endpoint.
* TCP: Kubernetes tries to establish a TCP connection on a port.
* Exec: Kubernetes runs a command inside the container.

ReadinessProbe
```yaml
apiVersion: v1
kind: Pod
metadata:
  name: readiness-example
spec:
  containers:
  - name: myapp
    image: myapp:latest
    ports:
    - containerPort: 8080
    readinessProbe:
      httpGet:
        path: /health/ready
        port: 8080
      initialDelaySeconds: 5
      periodSeconds: 10
```

LivenessProbe

```yaml
apiVersion: v1
kind: Pod
metadata:
  name: liveness-example
spec:
  containers:
  - name: myapp
    image: myapp:latest
    ports:
    - containerPort: 8080
    livenessProbe:
      httpGet:
        path: /health/live
        port: 8080
      initialDelaySeconds: 15
      periodSeconds: 20
      failureThreshold: 3
```
