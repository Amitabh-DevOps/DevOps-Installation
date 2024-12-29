# Install AWS CLI

The AWS CLI allows you to interact with AWS services from the command line.

### Steps:

1. **Download the AWS CLI installer:**
    
    ```bash
    curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"
    ```
    
2. **Install unzip if not already installed:**
    
    ```bash
    sudo apt install -y unzip
    ```
    
3. **Unzip the installer:**
    
    ```bash
    unzip awscliv2.zip
    ```
    
4. **Run the installer:**
    
    ```bash
    sudo ./aws/install
    ```
    
5. **Verify the installation:**
    
    ```bash
    aws --version
    ```
    
6. **Configure AWS CLI:**
    
    ```bash
    aws configure
    ```
    
    Enter the following details:
    
    * AWS Access Key ID
        
    * AWS Secret Access Key
        
    * Default region
        
    * Default output format (e.g., JSON)
        

### Steps to Retrieve AWS Access Key ID and Secret Access Key:

1. **Log in to the AWS Management Console:**
    
    * Go to [AWS Console](https://aws.amazon.com/console/).
        
2. **Navigate to the IAM Dashboard:**
    
    * Click on **Services** and search for **IAM** (Identity and Access Management).
        
3. **Create a New IAM User:**
    
    * Select **Users** from the left menu and click **Add Users**.
        
    * Provide a username and select **Programmatic Access** as the access type.
        
4. **Assign Permissions:**
    
    * Choose an existing policy (e.g., `AdministratorAccess`) or create a custom policy.
        
5. **Review and Create:**
    
    * Review the settings and click **Create User**.
        
6. **Download the Credentials:**
    
    * Save the **Access Key ID** and **Secret Access Key** securely, and copy them to paste during the `aws configure` setup process.
        

