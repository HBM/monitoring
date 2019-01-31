
# Monitoring

A simple monitoring demonstration.

## How does it work?

The following tools are used

- [Prometheus](https://prometheus.io/) to scrape all endpoints and store the data
- [Grafana](https://grafana.com/) to visualize the data
- [node_exporter](https://github.com/prometheus/node_exporter) to export machine metrics (host metrics)
- [cAdvisor](https://github.com/google/cadvisor) to analyze containers

## How do I use it?

You need to have `docker-compose` on your system.

1. Clone the repository

    `git clone git@github.com:HBM/monitoring.git`

1. Go into the newly created folder

    `cd monitoring`

1. Start the containers

    `docker-compose up -d`

1. Go to []()

## Where are the other services?



grafana login: admin, admin

docker-compose up -d

cAdvisor: container metrics collector