# Install Grafana

Grafana visualizes data collected by Prometheus.

### Steps:

1. **Add Grafana’s repository:**
    
    ```bash
    sudo apt update
    sudo apt install -y software-properties-common
    wget -q -O - https://packages.grafana.com/gpg.key | sudo apt-key add -
    echo "deb https://packages.grafana.com/oss/deb stable main" | sudo tee /etc/apt/sources.list.d/grafana.list
    ```
    
2. **Install Grafana:**
    
    ```bash
    sudo apt update
    sudo apt install -y grafana
    ```
    
3. **Start and enable Grafana:**
    
    ```bash
    sudo systemctl start grafana-server
    sudo systemctl enable grafana-server
    ```
    
4. **Access Grafana:** Open a browser and navigate to `http://<your-ip>:3000`. Use default credentials (`admin/admin`).
    

