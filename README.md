# Grafana-Promethesus-Docker

## Create the following dir as root
mkdir -p promgrafnode/prometheus && \ mkdir -p promgrafnode/grafana/provisioning && \ touch promgrafnode/docker-compose.yml && \ touch promgrafnode/prometheus/prometheus.yml

## Update .yml Files
Update the docker-compose.yml and the prometheus.yml files with the ones in this repo

## Ports
Allow ports: 80, 8080, 9090 (prometheus)

## Run docker containers as root
Nav to promgrafnode and run docker-compose up -d