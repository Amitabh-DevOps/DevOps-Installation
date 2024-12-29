# Install Docker

Docker simplifies application containerization. Here's how to install Docker on Ubuntu:

### Steps:

1. **Update the package index:**
    
    ```bash
    sudo apt update
    sudo apt upgrade -y
    ```
    
2. **Install dependencies:**
    
    ```bash
    sudo apt install -y apt-transport-https ca-certificates curl software-properties-common
    ```
    
3. **Add Docker’s official GPG key:**
    
    ```bash
    curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg
    ```
    
4. **Set up the Docker repository:**
    
    ```bash
    echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
    ```
    
5. **Install Docker:**
    
    ```bash
    sudo apt update
    sudo apt install -y docker-ce docker-ce-cli containerd.io
    ```
    
6. **Verify the installation:**
    
    ```bash
    docker --version
    ```
    
7. **Enable Docker to start on boot:**
    
    ```bash
    sudo systemctl enable docker
    ```
    
8. **Run Docker without sudo (optional):**
    
    ```bash
    sudo usermod -aG docker $USER
    newgrp docker
    ```
    

