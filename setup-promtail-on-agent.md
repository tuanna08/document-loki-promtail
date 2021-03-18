#### step 1: use root

```
  cd /opt/
  wget https://github.com/grafana/loki/releases/download/v2.0.0/promtail-linux-amd64.zip
  wget https://github.com/tuanna08/document-loki-promtail/blob/main/promtail-local-config.yaml
  unzip promtail-linux-amd64.zip 
  
```
#### step 2: edit file promtail-local-config.yaml, set loki url server

#### step 3: create service systemd

```
  cd /opt/
  wget https://raw.githubusercontent.com/tuanna08/document-loki-promtail/main/loki_agent_promtail.service
  cp /opt/loki_agent_promtail.service /etc/systemd/system/loki_agent_promtail.service
  systemctl daemon-reload
  systemctl enable --now loki_agent_promtail.service
```
