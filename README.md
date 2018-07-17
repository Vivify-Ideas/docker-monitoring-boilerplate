# Docker monitoring boilerplate

This boilerplate allows you to monitor key metrics of Docker node and uptime of your web apps.

## Services list

- [Prometheus](https://prometheus.io/) - Prometheus is an open-source systems monitoring and alerting toolkit.
- [Node-Exporter](https://github.com/prometheus/node_exporter) - Prometheus exporter for hardware and OS metrics exposed by \*NIX kernels.
- [UptimeRobot-Exporter](https://github.com/masaruhoshi/uptimerobot-prometheus-exporter) - Prometheus exporter for UptimeRobot monitors.
- [cAdvisor](https://github.com/google/cadvisor) -
  cAdvisor (Container Advisor) provides container users an understanding of the resource usage and performance characteristics of their running containers.
- [Grafana](https://grafana.com/) - The leading open source software for time series analytics.

## How to start whole monitoring stack ?

Stack can be started using docker-compose with command `docker-compose up`

> Argument `-d` can be used to start in Detached mode (background)

## How to add built-in Datasource and Dashboards to Grafana ?

Normally when you start stack first time grafana will be empty. (No Datasources or Dashboards will be created).

To add Prometheus datasource and our 2 dashboards (you can find them in `grafana-dashboards` directory) you have to run `init` script.

> Init script is bash script so it can be executed with `./init`

## How to add 3rd party grafana Dashboards ?

Official & community built dashboards can be found [here](https://grafana.com/dashboards).
