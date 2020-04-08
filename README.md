### Run Prometheus, Alertmanager, Grafana via Docker

```

```
For example, in windows
```
docker-compose up
```


### Grafana

#### References

[Github Grafana datasource for Prometheus Alertmanager](https://github.com/camptocamp/grafana-prometheus-alertmanager-datasource)


#### Environment

Plugins provisioned
```
# Intalled using environment variables
camptocamp-prometheus-alertmanager-datasource
```

Data Sources

| Description             | Type                                          | Access |
| ----------------------- | --------------------------------------------- | ------ |
| Prometheus              | prometheus                                    | proxy  |
| Prometheus AlertManager | camptocamp-prometheus-alertmanager-datasource | proxy  |
