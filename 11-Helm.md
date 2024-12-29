# Install Helm

### Prerequisites:

* Ensure Kubernetes is running (using KIND, Minikube, or any other method).
    
* Helm requires a Kubernetes cluster running version **1.18+**.
    
* Install Kubectl as well
    
* Verify your Kubernetes setup by running:
    
    ```bash
    kubectl version --client
    ```
    
* Ensure the cluster is accessible and kubectl is configured correctly:
    
    ```bash
    kubectl get nodes
    ```
    

Helm is a package manager for Kubernetes, which simplifies deploying and managing Kubernetes applications.

### Steps:

1. **Get the Helm shell file:**
    
    ```bash
    curl -fsSL -o get_helm.sh https://raw.githubusercontent.com/helm/helm/main/scripts/get-helm-3
    ```
    
2. **Change permission and run shell file:**
    
    ```bash
    chmod 700 get_helm.sh
    ./get_helm.sh
    ```
    
3. **Verify installation:**
    
    ```bash
    helm version
    ```
    

