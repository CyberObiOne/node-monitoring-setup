### Settuping

To run Grafana with Prometheus and node exporter to track your node statictics you need:

1. Install  [Grafana](https://github.com/CyberObiOne/grafana/blob/main/Grafana.md)  on server
2. [Clone](https://github.com/CyberObiOne/grafana/tree/main/node_monitoring) repo with easy setup of prometheus and node exporter and execute install.sh
3. Check that prometheus and node exporter running on your server

```
systemctl status prometheus
systemctl status node_exporter.service
```
4. Login to Grafana IP:3000 with initial password admin/admin and update password with your own.
5. Add new [Prometheus Datasource](https://grafana.com/docs/grafana/latest/datasources/add-a-data-source/) Prometheus_server_IP:8090, save configuration.
6. [Import](https://grafana.com/docs/grafana/latest/dashboards/export-import/) grafana dashboard from [file](https://github.com/CyberObiOne/grafana/blob/main/statisctic.json)
You will get similar to this:
![image](https://user-images.githubusercontent.com/6951043/127872191-a0626094-2b65-4407-84be-19d170e12f4b.png)
7. Also you can configure [alerts](https://grafana.com/docs/grafana/latest/alerting/old-alerting/create-alerts/) and [notifications](https://grafana.com/docs/grafana/latest/alerting/old-alerting/notifications/)
