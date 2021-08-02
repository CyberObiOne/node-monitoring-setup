### Grafana

Grafana is a monitoring tool, where you can  create, explore and share all of your data through beautiful, flexible dashboards.

How to install Grafana?!

To install the latest OSS release:

```
sudo apt-get install -y apt-transport-https
sudo apt-get install -y software-properties-common wget
wget -q -O - https://packages.grafana.com/gpg.key | sudo apt-key add -
```
Add this repository for stable releases:

```
echo "deb https://packages.grafana.com/oss/deb stable main" | sudo tee -a /etc/apt/sources.list.d/grafana.list
```

After you add the repository:

```
sudo apt-get update
sudo apt-get install grafana
```

This starts the grafana-server process as the grafana user, which was created during the package installation.

To check that grafana started properly - 

```
sudo systemctl status grafana-server
```
