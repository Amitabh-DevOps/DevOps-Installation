# Steps to Install ArgoCD:**

1. **Create the ArgoCD Namespace:**
    
    ```bash
    kubectl create ns argocd
    ```
    
2. **Install ArgoCD:** Apply the ArgoCD manifests to install it:
    
    ```bash
    kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml
    ```
    
3. **Verify ArgoCD Installation:** Check the pods in the `argocd` namespace to ensure they are running:
    
    ```bash
    kubectl get pods -n argocd
    ```
    
4. **Accessing the ArgoCD UI:** By default, the ArgoCD server is exposed as a `ClusterIP` service. To access the UI:
    
    * **Option 1: Port Forwarding**  
        Forward the port to your local machine:
        
        ```bash
        kubectl port-forward svc/argocd-server -n argocd 8080:443
        ```
        
        Access the UI at:  
        [https://localhost:8080](https://localhost:8080/)
        
    * **Option 2: Change Service to NodePort**  
        Update the ArgoCD server service to `NodePort`:
        
        ```bash
        kubectl edit svc argocd-server -n argocd
        ```
        
        Change `type: ClusterIP` to `type: NodePort`.  
        Access ArgoCD at:  
        `http://<node-ip>:<node-port>`
        

