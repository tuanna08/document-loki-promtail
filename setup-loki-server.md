#### Prerequisites
- docker
#### step 1: 

```
  cd /opt/
  wget https://raw.githubusercontent.com/tuanna08/document-loki-promtail/main/loki-local-config.yaml -O loki-config.yaml
  docker run -v $(pwd):/mnt/config -p 3100:3100 grafana/loki:1.6.0 -config.file=/opt/loki-config.yaml
```
