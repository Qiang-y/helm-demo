# Helm Nginx Deployment

This Helm chart deploys a simple Nginx application on Tencent Kubernetes Engine (TKE) with support for spot instances.

## Prerequisites

1. **Tencent Cloud TKE Super Node**: 
   - Log in to the [Tencent Cloud Console](https://console.cloud.tencent.com/tke2) and enable TKE Super Node with spot instance mode.

2. **Helm Installation**: 
   - Install Helm by following the official [Helm installation guide](https://helm.sh/docs/intro/install/).

## Deployment Methods

### Method 1: Local Deployment

1. Clone this repository :
   ```bash
   git clone https://github.com/Qiang-y/helm-demo.git
   ```

2. Install the Helm chart:
   ```bash
   helm install --generate-name ./nginx-demo
   ```

### Method 2: Repository Deployment

1. Add the Helm repository:
   ```bash
   helm repo add spot https://qiang-y.github.io/helm-demo/
   ```

2. Search the chart from the repository:
   ```bash
   helm search repo spot/nginx-demo
   ```

3. Install the chart directly from the repository:
   ```bash
   helm install <release-name> spot/nginx-demo
   ```

## Configuration

Modify the `values.yaml` file to customize the deployment, such as setting the number of replicas or enabling spot instances.

## License

This project is licensed under the MIT License.