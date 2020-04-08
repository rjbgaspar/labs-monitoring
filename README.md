### Run Prometheus, Alertmanager, Grafana via Docker

```

```
For example, in windows
```
docker-compose up
```


## Grafana

### References

[Github Grafana datasource for Prometheus Alertmanager](https://github.com/camptocamp/grafana-prometheus-alertmanager-datasource)

##### Dashboards
[JVM (Micrometer)](https://grafana.com/grafana/dashboards/4701)<br/> 
[Prometheus AlertManagerby daixiang0](https://grafana.com/grafana/dashboards/8010/)<br/> 
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

| Description                                                     | Id   | Date       | Replace                          |
| --------------------------------------------------------------- | ----:| ---------- | -------------------------------  |
| [JVM (Micrometer)](https://grafana.com/grafana/dashboards/4701) | 4701 | 2020-04-08 | ${DS_PROMETHEUS} with Prometheus |

