
# Project Setup Guide

## Docker and Service Monitoring Setup

### 8. Build and Run Docker Containers
Build and start Docker containers:
```bash
docker-compose up --build
```

### 9. Run Docker Containers in Detached Mode
Run containers in the background:
```bash
docker-compose up -d
```

## Accessing Applications and Tools

### 10. Flask Application
Access the Flask application at:
[http://localhost:8000](http://localhost:8000)

### 11. Prometheus Monitoring Tool
Access Prometheus at:
[http://localhost:9090](http://localhost:9090)

### 12. Grafana
Login to Grafana at:
[http://localhost:3000](http://localhost:3000)
Default credentials are `admin` for both username and password.


### 9. Reestart the running Docker Container
Restart containers to effect the chnges:
```bash
docker-compose restart grafana
```
