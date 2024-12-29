# Install Kubectl

Kubectl is a command-line tool for interacting with Kubernetes clusters.

### Steps:

1. **Download the latest Kubectl binary:**
    
    ```bash
    curl -LO "https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl"
    ```
    
2. **Make the binary executable:**
    
    ```bash
    chmod +x kubectl
    ```
    
3. **Move the binary to a directory in your PATH:**
    
    ```bash
    sudo mv kubectl /usr/local/bin/
    ```
    
4. **Verify installation:**
    
    ```bash
    kubectl version --client
    ```
    

