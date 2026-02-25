# kubernetes

## Common options and flags

```

alias k=kubectl
echo 'alias k=kubectl' >>~/.bashrc

```

# Cluster Information

### Displays information about the control plane and services.
```
kubectl cluster-info 
```
### Lists all worker nodes in the cluster.
```
kubectl get nodes

```

### Shows verbose details and status of a specific node

```
kubectl describe node <node_name>

```

#  Pod Management

### Lists all pods in the current namespace

```

kubectl get pods

```
### Lists pods with additional details like node name and IP addresses.

```
kubectl get pods -o wide

```

### Provides detailed information, events, and status of a pod.

```

kubectl describe pod <pod_name>

```

### View the standard output/logs from a container in a pod to diagnose application errors

```
kubectl logs <pod-name>

```

### Follow (stream) the logs in real-time for continuous monitoring of application activity.

```
kubectl logs -f <pod-name>
```

### Open an interactive shell inside a running container for real-time inspection, testing configurations, or manual debugging (e.g., checking files or network connectivity).


```
kubectl exec -it <pod-name> -- sh
```

### Show labels in the output columns:

```
kubectl get pods --show-labels

```

### Get detailed information for a specific selection:

```
kubectl describe pods -l environment=production

```


### Access logs from all pods matching a label

```
kubectl logs -l 'app=my-app,tier=backend'

```
### Display real-time CPU and memory usage of a specific pod (requires the Metrics Server to be installed).

```
kubectl top pod <pod-name>
```

### Access an application running in a pod from your local machine via a specific local port (e.g., 8080), useful for local testing and debugging without exposing the service externally.

```
kubectl port-forward <pod-name> 8080:80
```

### Manually delete a specific pod. In a production environment managed by a Deployment, a new, healthy pod will automatically be created to replace it (auto-healing).

```
kubectl delete pod <pod-name>
```