# helm-journey

## Description
Helm is a package manager for Kubernetes that simplifies deploying and managing applications using pre-configured charts. Below are some basic commands to get started with Helm.

## Terms
- **Chart**: A Helm **chart** is a packaged application (like a Docker image).
- **Release**: A Helm **release** is an instance of a chart that’s deployed and running (like a Docker container).

## Prerequisites
You need a running Kubernetes cluster to use Helm. For local Kubernetes with Colima, use the following command:
``` 
colima start --with-kubernetes
 ```

## Commands

Add the Bitnami repository:
```
helm repo add bitnami https://charts.bitnami.com/bitnami
```

List Helm repositories:
```
helm repo list
```

Install a chart (e.g., WordPress):
```
helm install my-release oci://registry-1.docker.io/bitnamicharts/wordpress
```

List installed releases:
```
helm list
```

Uninstall a release:
```
helm uninstall my-release
```
