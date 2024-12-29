# Deploy Prometheus and Grafana Using Helm

Using Helm makes it much easier to deploy complex applications like Prometheus and Grafana in Kubernetes.

### Prerequisites:

* Ensure Kubernetes is running (using KIND, Minikube, or any other method).
    
* Install Helm (see the Helm installation steps above).
    

### Steps:

1. **Add the Helm repository for Prometheus and Grafana:**
    
    ```bash
    helm repo add prometheus-community https://prometheus-community.github.io/helm-charts
    helm repo add grafana https://grafana.github.io/helm-charts
    helm repo update
    ```
    
2. **Create a namespace for monitoring tools:**
    
    ```bash
    kubectl create namespace monitoring
    ```
    
3. **Install Prometheus using Helm:**
    
    ```bash
    helm install prometheus prometheus-community/prometheus --namespace monitoring
    ```
    
4. **Verify Prometheus installation:**
    
    ```bash
    kubectl get pods -n monitoring
    ```
    
5. **Install Grafana using Helm:**
    
    ```bash
    helm install grafana grafana/grafana --namespace monitoring
    ```
    
6. **Verify Grafana installation:**
    
    ```bash
    kubectl get pods -n monitoring
    ```
    
7. **Access Grafana:**
    
    * Forward the Grafana service port to [localhost](http://localhost):
        
        ```bash
        kubectl port-forward svc/grafana 3000:80 -n monitoring
        ```
        
    * Open your browser and go to [`http://localhost:3000`](http://localhost:3000). Use default credentials (`admin/admin`).
        

