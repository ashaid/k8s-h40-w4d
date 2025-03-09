## Prerequisites

- Minikube installed
- kubectl installed and configured

## Getting Started

1. Clone this repository:

   ```bash
   git clone https://github.com/yourusername/k8s-starter.git
   cd k8s-starter
   ```

2. Start Minikube:

   ```bash
   minikube start
   ```

3. Apply the basic Nginx deployment:

   ```bash
   kubectl apply -f manifests/simple-nginx.yaml
   ```

4. Check that your pods are running:

   ```bash
   kubectl get pods
   ```

5. Get the URL to access your deployment:
   ```bash
   minikube service nginx-service --url
   ```

## ConfigMap Example

To test the ConfigMap example:

1. Apply the ConfigMap:

   ```bash
   kubectl apply -f manifests/configmap-example.yaml
   ```

2. Deploy Nginx with the ConfigMap mounted:

   ```bash
   kubectl apply -f manifests/nginx-configmap.yaml
   ```

3. Access the service:
   ```bash
   minikube service nginx-configmap-service --url
   ```
   
## Cleanup

When you're done:

```bash
minikube stop
```
