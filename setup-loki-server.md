#### Prerequisites
- docker
#### step 1: 

```
  cd /opt/
  wget https://raw.githubusercontent.com/grafana/loki/v1.6.0/cmd/loki/loki-local-config.yaml -O loki-config.yaml
  docker run -v $(pwd):/mnt/config -p 3100:3100 grafana/loki:1.6.0 -config.file=/opt/loki-config.yaml
```
