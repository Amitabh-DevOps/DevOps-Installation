# eksctl Installation**

`eksctl` is a command-line tool that simplifies the creation and management of Kubernetes clusters on Amazon EKS.

#### Steps:

1. **Update the package index:**
    
    ```bash
    sudo apt update
    sudo apt upgrade -y
    ```
    
2. **Download eksctl binary:**
    
    ```bash
    curl -sL "https://github.com/weaveworks/eksctl/releases/latest/download/eksctl_$(uname -s)_amd64.tar.gz" -o eksctl.tar.gz
    ```
    
3. **Extract the binary:**
    
    ```bash
    tar -xzf eksctl.tar.gz
    ```
    
4. **Move the binary to a directory in your PATH:**
    
    ```bash
    sudo mv eksctl /usr/local/bin
    ```
    
5. **Verify the installation:**
    
    ```bash
    eksctl version
    ```
    

