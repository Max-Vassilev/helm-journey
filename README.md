# helm-journey

- **Helm**: [Helm: https://www.youtube.com/watch?v=kJscDZfHXrQ](https://www.youtube.com/watch?v=kJscDZfHXrQ) 🎥
- **ArtifactHub**: [ArtifactHUB: https://artifacthub.io/](https://artifacthub.io/) 🔗

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

Install a chart (e.g., Nginx):
```
helm install my-release oci://registry-1.docker.io/bitnamicharts/nginx
```

List installed releases:
```
helm list
```
Accessing a deployed service (e.g., Nginx): To access the Nginx service deployed via Helm locally:
```
kubectl port-forward svc/my-release-nginx 8080:80
```

Now you can open http://localhost:8080 in your browser to see Nginx.

Uninstall a release:
```
helm uninstall my-release
```
