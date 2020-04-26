# Kubernetes - Services

## How to create a service and expose it

    ```bash
    kubectl expose pod <pod name> --port <port to expose> --type LoadBalancer
    ```

## How to set up port forwarding (temporal) to one Pod

    ```bash
    kubectl port-forward <pod name> <external port>:<port of pod>
    ```
