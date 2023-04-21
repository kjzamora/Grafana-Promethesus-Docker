# Grafana-Promethesus-Docker

## Create the following dir as root
mkdir -p promgrafnode/prometheus && \ mkdir -p promgrafnode/grafana/provisioning && \ touch promgrafnode/docker-compose.yml && \ touch promgrafnode/prometheus/prometheus.yml

## Update .yml Files
- Update the docker-compose.yml and the prometheus.yml files with the ones in this repo
- Update prometheus.yml
    - Install node-exporter on other host
        - Default node-exporter port is 9182
        - Node-exporter port for current host will be 9100
    - job-nmae: prometheus
        - runs on current host
    - job-name: cadvisor
        - Monitors docker containers on current host
    - job-name: node
        - runs node-exporter on docker host
    - job-name: myPC & otherPC
        - runs node-exporter on other network host

## Ports
Allow ports: 80, 8080, 9090 (prometheus), 3000 (grafana)

## Run docker containers as root
Nav to promgrafnode and run docker-compose up -d