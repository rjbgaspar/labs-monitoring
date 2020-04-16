### Run Prometheus, Alertmanager, promtail, Grafana, cAdvisor, node-exporter, Fluentd, loki, via Docker

```

```
For example, in windows
```
docker-compose up
```


## Grafana

### References
[Prometheus](https://prometheus.io/)
[Alertmanager | Prometheus](https://prometheus.io/docs/alerting/alertmanager/)
[Github Grafana datasource for Prometheus Alertmanager](https://github.com/camptocamp/grafana-prometheus-alertmanager-datasource)
[fluentd](https://www.fluentd.org/)

##### Dashboards
[Node Exporter Server Metrics by Knut Ytterhaug](https://grafana.com/grafana/dashboards/1860)<br/> 
[Node Exporter Full by idealista](https://grafana.com/grafana/dashboards/1860)<br/> 
[JVM (Micrometer)](https://grafana.com/grafana/dashboards/4701)<br/> 
[Prometheus AlertManager by daixiang0](https://grafana.com/grafana/dashboards/8010)<br/> 
[Alertmanager Grafana dashboard](https://grafana.com/grafana/dashboards/9578)

### Environment
Plugins provisioned
```
# Provisioned using environment variables
camptocamp-prometheus-alertmanager-datasource
```

##### Data Sources

| Description             | Type                                          | Access |
| ----------------------- | --------------------------------------------- | ------ |
| Prometheus              | prometheus                                    | proxy  |
| Prometheus AlertManager | camptocamp-prometheus-alertmanager-datasource | proxy  |


##### Dashboards

Using environment variables in provisioned dashboard json file is not supported.<br/> 
Replaced all instances of ${ENV_VAR_NAME} for the desired value.

| Description                                                                                   | Id   | File version                           | Date       | Replace                                                    |
| --------------------------------------------------------------------------------------------- | ----:| -------------------------------------- | ---------- | ---------------------------------------------------------- |
| [Node Exporter Server Metrics by Knut Ytterhaug](https://grafana.com/grafana/dashboards/1860) |  405 | node-exporter-server-metrics_rev8.json | 2020-04-16 | ${DS_PROMETHEUS} with Prometheus                           |
| [Node Exporter Full by idealista](https://grafana.com/grafana/dashboards/1860)                | 1860 | node-exporter-full_rev16.json          | 2020-04-16 | ${DS_PROMETHEUS} with Prometheus                           |
| [JVM (Micrometer)](https://grafana.com/grafana/dashboards/4701)                               | 4701 | jvm-micrometer_rev9.json               | 2020-04-08 | ${DS_PROMETHEUS} with Prometheus                           |
| [Prometheus AlertManager by daixiang0](https://grafana.com/grafana/dashboards/8010)           | 8010 | prometheus-alertmanager_rev1.json      | 2020-04-08 | ${DS_PROMETHEUS_ALERTMANAGER} with Prometheus AlertManager |