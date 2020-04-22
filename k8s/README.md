# Kubernetes

## How to remove all the node of a cluster

0. Check if you ip was on "Master authorised networks" on k8s cluster. 

    - Click edit on cluster.
    - Check the "Master authorised networks".

1. First point to right k8s cluster

```bash
gcloud container clusters get-credentials <cluster name> --zone <gcp region> --project <gcp project>
```

2. Get the list of nodes.

```bash
kubectl get nodes
```

3. Drain/disable each node of cluster.

```bash
kubectl drain <node name>
kubectl drain <node name> --ignore-daemonsets
```

4. Delete fisically each node.

```bash
kubectl delete node <node name>
```

