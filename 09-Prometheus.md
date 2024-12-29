# Install Prometheus

Prometheus is a monitoring and alerting toolkit.

### Steps:

1. **Download Prometheus:**
    
    ```bash
    wget https://github.com/prometheus/prometheus/releases/download/v2.50.0/prometheus-2.50.0.linux-amd64.tar.gz
    ```
    
2. **Extract the archive:**
    
    ```bash
    tar -xvzf prometheus-2.50.0.linux-amd64.tar.gz
    cd prometheus-2.50.0.linux-amd64
    ```
    
3. **Move binaries to** `/usr/local/bin`:
    
    ```bash
    sudo mv prometheus promtool /usr/local/bin/
    ```
    
4. **Create a Prometheus config directory:**
    
    ```bash
    sudo mkdir /etc/prometheus
    sudo mv prometheus.yml /etc/prometheus/
    ```
    
5. **Verify Prometheus installation:**
    
    ```css
    prometheus --version
    ```
    
6. **Start Prometheus:**
    
    ```bash
    prometheus --config.file=/etc/prometheus/prometheus.yml
    ```
    

