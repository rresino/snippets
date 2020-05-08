# Kubernetes - Minikube

## Start a new minikube cluster and set manually the k8s version

```bash
minikube start --kubernetes-version <k8s version>
```

## Run K8S dashboard

```bash
minikube dashboard
```

## Get url from K8S service

```bash
minikube service <service name> --url --namespace <namespace name>
```

## Drop current cluster

```bash
minikube delete
```

## Enable load balancer for minikube 

```bash
minikube tunnel
```

If minikube don't clean the tunnel network, you can force the clean up using:

```bash
minikube tunnel --cleanup
```

***

- [Home](/README.md)
- [Docker](/docker/README.md)
- [Git](/git/README.md)
- [Kubernetes](/k8s/README.md)
