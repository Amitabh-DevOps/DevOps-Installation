# Install Terraform

Terraform manages infrastructure as code (IaC).

### Steps:

1. **Download the Terraform binary:**
    
    ```bash
    curl -fsSL https://releases.hashicorp.com/terraform/1.5.7/terraform_1.5.7_linux_amd64.zip -o terraform.zip
    ```
    
2. **Install the unzip tool (if not installed):**
    
    ```bash
    sudo apt install -y unzip
    ```
    
3. **Extract and move the binary:**
    
    ```bash
    unzip terraform.zip
    sudo mv terraform /usr/local/bin/
    ```
    
4. **Verify installation:**
    
    ```bash
    terraform --version
    ```
    

