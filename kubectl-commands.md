# 🟢 1️⃣ Cluster Information Commands

### 🔹 Check cluster info

```bash
kubectl cluster-info
```

### 🔹 Check nodes

```bash
kubectl get nodes
```

### 🔹 Detailed node info

```bash
kubectl describe node <node-name>
```

---

# 🟢 2️⃣ Get Resources (Very Important)

General syntax:

```bash
kubectl get <resource>
```

### Common resources:

```bash
kubectl get pods
kubectl get pods -A
kubectl get svc
kubectl get deployments
kubectl get replicaSets
kubectl get namespaces
kubectl get configmaps
kubectl get secrets
kubectl get ingress
kubectl get all
```

---

# 🟢 3️⃣ Describe Resources (Debugging Tool)

```bash
kubectl describe pod <pod-name>
kubectl describe deployment <name>
kubectl describe svc <name>
```

Shows:

* Events
* Errors
* Scheduling issues
* Image pull errors

---

# 🟢 4️⃣ Create / Apply Resources

### Apply YAML file

```bash
kubectl apply -f file.yaml
```

### Create namespace

```bash
kubectl create namespace dev
```

### Create deployment (quick test)

```bash
kubectl create deployment nginx --image=nginx
```

---

# 🟢 5️⃣ Delete Resources

```bash
kubectl delete pod <name>
kubectl delete deployment <name>
kubectl delete svc <name>
kubectl delete -f file.yaml
kubectl delete namespace dev
```

---

# 🟢 6️⃣ Logs & Debugging (Very Important)

### Check logs

```bash
kubectl logs <pod-name>
```

### Follow logs (like tail -f)

```bash
kubectl logs -f <pod-name>
```

### Logs from specific container

```bash
kubectl logs <pod> -c <container-name>
```

---

# 🟢 7️⃣ Execute Inside Pod

```bash
kubectl exec -it <pod-name> -- bash
```

or

```bash
kubectl exec -it <pod-name> -- sh
```

Used for:

* Debugging
* Checking files
* Testing connectivity

---

# 🟢 8️⃣ Port Forward (Testing Locally)

```bash
kubectl port-forward pod/<pod-name> 8080:80
```

Access in browser:

```
localhost:8080
```

---

# 🟢 9️⃣ Scale Deployment

```bash
kubectl scale deployment nginx --replicas=3
```

---

# 🟢 🔟 Rolling Update & Restart

### Restart deployment

```bash
kubectl rollout restart deployment nginx
```

### Check rollout status

```bash
kubectl rollout status deployment nginx
```

### Rollback

```bash
kubectl rollout undo deployment nginx
```

---

# 🟢 1️⃣1️⃣ Resource Usage (Metrics Server Required)

```bash
kubectl top nodes
kubectl top pods
```

---

# 🟢 1️⃣2️⃣ Namespace Commands

```bash
kubectl get ns
kubectl config set-context --current --namespace=dev
```

---

# 🟢 1️⃣3️⃣ Config & Context

```bash
kubectl config view
kubectl config get-contexts
kubectl config use-context <context-name>
```

---

# 🟢 1️⃣4️⃣ View YAML of Running Resource

```bash
kubectl get pod <pod-name> -o yaml
```

Very powerful for learning.

---

# 🟢 1️⃣5️⃣ Edit Resource Live

```bash
kubectl edit deployment nginx
```

---

# 🟢 1️⃣6️⃣ Watch Mode (Real-Time)

```bash
kubectl get pods -w
```

---

# 🔥 Most Important Commands for DevOps Interviews

If someone asks most used kubectl commands:

* get
* describe
* apply
* delete
* logs
* exec
* scale
* rollout
* port-forward
* config

---

# 🏆 10 Commands You Must Master

```bash
kubectl get pods -A
kubectl describe pod <name>
kubectl logs -f <pod>
kubectl exec -it <pod> -- bash
kubectl apply -f file.yaml
kubectl delete -f file.yaml
kubectl scale deployment <name> --replicas=3
kubectl rollout restart deployment <name>
kubectl get nodes
kubectl config get-contexts
```

If you master these → you're comfortable with Kubernetes.

---
