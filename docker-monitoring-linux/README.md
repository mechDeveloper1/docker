# docker monitoring on linux

## boot2docker.iso docker-machine

### create a new folder in C:\Users folder of your computer as this folder is shared with boot2docker machine 
`C:\Users\docker-monitoring\monitoring-linux\tmp\prometheus.yml`

## prometheus
https://prometheus.io/docs/prometheus/latest/installation/

### docker command to run prometheus
docker run -d -p 9090:9090 \
  -v //c/Users/docker-monitoring/monitoring-linux/tmp/prometheus.yml:/etc/prometheus/prometheus.yml \
  prom/prometheus
 
 
 ### monitoring docker container metrics using cadvisor (only linux host) 
 https://prometheus.io/docs/guides/cadvisor/
 
 
