# Project Overview

This guide details the setup for a Docker-based monitoring solution utilizing Prometheus and Grafana. This setup allows for tracking the performance of various services running within Docker containers.

## Prerequisites

- Docker and Docker Compose installed on your machine.
- Basic knowledge of Docker and containerization.

## Services Configuration

The project comprises the following services:

- **Node Exporter**: Collects hardware and OS metrics exposed by *NIX kernels.
- **Prometheus**: Monitoring system and time series database.
- **Grafana**: Analytic and monitoring platform.

## Getting Started

### 1. Build and Run Docker Containers

To build and start the Docker containers for the first time or apply updates:

```bash
docker compose up --build
```

### 2. Run Docker Containers in Detached Mode

To run the containers in the background:

```bash
docker compose up -d
```

## Accessing Applications and Tools

### Prometheus Monitoring Tool

Access the Prometheus interface to view metrics and setup alerts:

- **URL**: [http://localhost:9090](http://localhost:9090)

### Node Exporter

Verify that Node Exporter is collecting and exposing system and hardware metrics correctly:

- **URL**: [http://127.0.0.1:9100/metrics](http://127.0.0.1:9100/metrics)

### Grafana Dashboard

Log into Grafana to create visualizations from the collected metrics:

- **URL**: [http://localhost:3000](http://localhost:3000)
- **Default Credentials**
  - **Username**: admin
  - **Password**: admin

### Managing Docker Containers

#### Restart a Specific Container

If you need to apply changes or updates to a container like Grafana, use the following command:

```bash
docker-compose restart grafana
```

#### Inspecting Containers

To find the IP address of a specific container, such as the Node Exporter:

```bash
docker inspect -f '{{range.NetworkSettings.Networks}}{{.IPAddress}}{{end}}' node-exporter
```

Ensure to replace `admin` with secure passwords and configurations as per your organization's standards before deployment.

