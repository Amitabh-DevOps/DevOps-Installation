# Install Jenkins

Jenkins is a CI/CD automation server.

### First Install JAVA on instance using :

```bash
sudo apt install openjdk-17-jdk
```

### Steps:

1. **Install dependencies**:
    
    ```css
     sudo apt-get install -y ca-certificates curl gnupg
    ```
    
2. **Add the Jenkins repository key**:
    
    ```css
     curl -fsSL https://pkg.jenkins.io/debian/jenkins.io-2023.key | sudo tee /usr/share/keyrings/jenkins-keyring.asc > /dev/null
    ```
    
3. **Add Jenkins to APT sources**:
    
    ```css
     echo deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc] https://pkg.jenkins.io/debian binary/ | sudo tee /etc/apt/sources.list.d/jenkins.list > /dev/null
    ```
    
4. **Install Jenkins**:
    
    ```css
     sudo apt-get update
     sudo apt-get install jenkins -y
    ```
    
5. **Enable Jenkins to start on boot**:
    
    ```css
     sudo systemctl enable jenkins
     sudo systemctl start jenkins
    ```
    
6. **Verify Jenkins status**:
    
    ```css
     sudo systemctl status jenkins
    ```
    
7. **Access Jenkins:** Open a browser and navigate to `http://<your-ip>:8080`. Use the password located in `/var/lib/jenkins/secrets/initialAdminPassword`.
    

