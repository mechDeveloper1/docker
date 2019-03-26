# docker monitoring on linux

## boot2docker.iso docker-machine

### configure Docker to expose Prometheus-compatible metrics on port 9323

To configure the Docker daemon as a Prometheus target, you need to specify the metrics-address. The best way to do this is via the daemon.json, which is located at one of the following locations by default. If the file does not exist, create it.

Linux: `/etc/docker/daemon.json`
Windows Server: `C:\ProgramData\docker\config\daemon.json`
Docker Desktop for Mac / Docker Desktop for Windows: Click the Docker icon in the toolbar, select Preferences, then select Daemon. Click Advanced.
If the file is currently empty, paste the following:

`{
  "metrics-addr" : "127.0.0.1:9323",
  "experimental" : true
}`

Save the file, or in the case of Docker Desktop for Mac or Docker Desktop for Windows, save the configuration. Restart Docker.

Docker now exposes Prometheus-compatible metrics on port 9323.

### Setps to configure boot2docker machine for docker to expose metrics on port 9323
`docker-machine ssh default`



### create a new folder in C:\Users folder of your computer as this folder is shared with boot2docker machine 
`C:\Users\docker-monitoring\monitoring-linux\tmp\prometheus.yml`


## prometheus
https://prometheus.io/docs/prometheus/latest/installation/

### docker command to run prometheus
`docker run -d -p 9090:9090 \
  -v //c/Users/docker-monitoring/monitoring-linux/tmp/prometheus.yml:/etc/prometheus/prometheus.yml \
  prom/prometheus`
 
## cadvisor
### monitoring docker container metrics using cadvisor (only linux host) 
https://prometheus.io/docs/guides/cadvisor/
 
## cadvisor (works only on linux)
https://github.com/google/cadvisor
 
 `docker run \
  --publish=8080:8080 \
  --detach=true \
  --name=cadvisor \
  google/cadvisor:latest`
  
## visualization with grafana
http://docs.grafana.org/installation/docker/
  
`docker run -d -p 3000:3000 grafana/grafana`

access grafana on browser  http://<docker-machine ip>:3000
default username admin
default password admin

add datasource prometheus

HTTP url http://192.168.99.100:9090

click Save & Test

now we can create grafana dashboards with the data coming from prometheus
