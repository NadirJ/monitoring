# Dev Monitoring Stack

This repo contains a docker-compose.yml that can run Prometheus and Grafana on a localhost.


## Prerequisties
* Docker installed on hostmachine


## Running
Start the docker servcies using docker-compose. From the base directory of this repo run the following command.

```
    docker-compose up
```

After starting the docker services, you should be able to access the Grafana UI and the Prometheus UI

* Grafana: http://127.0.0.1:3000
* Prometheus: http://127.0.0.1:9090


## Adding Exporters to Prometheus
When you need to add exporters to Prometheus, modify the file [prometheus/prometheus.yml](prometheus/prometheus.yml)

After adding a scrape job you can restart prometheus by running

```
    docker-compose down
    docker-compose up
```