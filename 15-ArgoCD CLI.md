# Install ArgoCD CLI on Linux  


## Prerequisites  

- A Linux-based system.  
- `curl` installed on your system.  
  To install `curl`, run:  
  ```bash
  sudo apt update && sudo apt install -y curl


---

## Steps  

### 1. Download the ArgoCD CLI Binary  
Use `curl` to download the latest release of the **ArgoCD CLI** binary:  

```bash
curl -sSL -o argocd-linux-amd64 https://github.com/argoproj/argo-cd/releases/latest/download/argocd-linux-amd64
```

This command:  
- Downloads the binary file for the **ArgoCD CLI**.  
- Saves it as `argocd-linux-amd64` in the current directory.  

---

### 2. Install the ArgoCD CLI  
Use the `install` command to move the binary to `/usr/local/bin` with appropriate permissions:  

```bash
sudo install -m 555 argocd-linux-amd64 /usr/local/bin/argocd
```

This command:  
- Moves the binary to `/usr/local/bin/` so it’s accessible system-wide.  
- Sets the permissions to `555` (read and execute access for everyone).  

---

### 3. Clean Up  
Remove the downloaded binary to keep your system clean:  

```bash
rm argocd-linux-amd64
```

---

### 4. Verify the Installation  
Check if the **ArgoCD CLI** is installed correctly by running:  

```bash
argocd version
```

You should see the installed version of **ArgoCD CLI** displayed.

---

### 4.Retrive and Decode the password:

```bash
kubectl -n argocd get secret argocd-initial-admin-secret -o jsonpath='{.data.password}' | base64 -d
```

This will return the decoded password.

---

### 5. **Login to ArgoCD CLI**

Once you have the password, you can log in to the **ArgoCD** server using the following command:

```bash
argocd login <ARGOCD_SERVER> -u admin -p <password>
```

* `<ARGOCD_SERVER>`: Replace this with the address of your **ArgoCD** server (e.g., [`argocd.example.com`](http://argocd.example.com) or an IP address).
    
* `<password>`: Replace this with the decoded **admin password** retrieved in the previous step.


--- 


## Notes  
- The `argocd` command is now available globally on your system.  
- Make sure your PATH includes `/usr/local/bin` (it usually does by default).  

---

**Happy Automating with ArgoCD!** 🚀  
  



