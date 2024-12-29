# Install Minikube

Minikube is another lightweight Kubernetes option for local development.

### Steps:

1. **Download Minikube binary:**
    
    ```bash
    curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64
    ```
    
2. **Make the binary executable:**
    
    ```bash
    chmod +x minikube-linux-amd64
    ```
    
3. **Move the binary to a directory in your PATH:**
    
    ```bash
    sudo mv minikube-linux-amd64 /usr/local/bin/minikube
    ```
    
4. **Verify installation:**
    
    ```bash
    minikube version
    ```
    

