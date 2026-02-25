# kubernetes

## Common options and flags

```

alias k=kubectl
echo 'alias k=kubectl' >>~/.bashrc

```

## Cluster Information

# Displays information about the control plane and services.
```
kubectl cluster-info 
```
# Lists all worker nodes in the cluster.
```
kubectl get nodes

```

# Shows verbose details and status of a specific node

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