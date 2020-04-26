# Kubernetes

- [Administrate cluster](./admin.md)
- [Pods](./pod.md)
- [Services](./svc.md)

## Add and enable bash autocompletion for kubectl

    ```bash
    source <(kubectl completion bash)
    ```

## Apply one configuration yaml

    ```bash
    kubectl apply -f <yaml file>
    ```

## Get cluster info

    ```bash
    kubectl cluster-info
    ```

## See kubectl configuration

    ```bash
    kubectl config view
    ```
