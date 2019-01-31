
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

    `git clone git@github.com:hbm/monitoring.git`

1. Go into the newly created folder

    `cd monitoring`

1. Start the containers

    `docker-compose up -d`

1. Make sure all containers are running

    `docker-compose ps`

1. Go to http://localhost:3000 to access Grafana. Username is `admin` and password is also `admin`.

1. On the main screen click on the "Docker Prometheus Monitoring" dashboard.

1. In the end if you want to shut down everything run

    `docker-compose down`

## Where are my other services?

1. node_exporter: http://localhost:9100
1. cadvisor: http://localhost:8080
1. prometheus: http://localhost:9090

## Development

As you can see everything is configured via `.yml` files.

`docker-compose.yml`

If you want to add another service, e.g. backend application (Go, PHP, Python, Node.js, Java, etc.) or database/cache (PostgreSQL, Redis, etc.) this is where to add it.

`prometheus/prometheus.yml`

Do you want to add another scrape target? Change the scraping frequency? Do it here.

`grafana/...`

Change the datasource for Grafana or install a new dashboard.