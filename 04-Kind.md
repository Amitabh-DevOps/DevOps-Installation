# Install Kubernetes (KIND)

KIND (Kubernetes IN Docker) runs Kubernetes clusters in Docker containers.

### Steps:

1. **Install Docker (if not already installed):** Refer to the Docker installation steps above.
    
2. **Download KIND binary:**
    
    ```bash
    curl -Lo ./kind https://kind.sigs.k8s.io/dl/v0.20.0/kind-linux-amd64
    ```
    
3. **Make the binary executable:**
    
    ```bash
    chmod +x ./kind
    sudo mv ./kind /usr/local/bin/kind
    ```
    
4. **Verify installation:**
    
    ```bash
    kind --version
    ```
    

