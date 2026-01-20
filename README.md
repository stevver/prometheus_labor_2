# Prometheus Lab 2

## Services (Host browser)
- Prometheus: http://localhost:9090
- Node Exporter: http://localhost:9100/metrics
- Docker Engine metrics: http://localhost:9323/metrics (if forwarded)
- cAdvisor: http://localhost:8080
- Alertmanager: http://localhost:9093
- Grafana: http://localhost:3000

## Start stack
cd docker-compose/prometheus
docker compose up -d

## Reload Prometheus config
curl -X POST http://localhost:9090/-/reload

## Notes
- alertmanager/alertmanager.yml is ignored (contains Slack webhook)
- Use alertmanager/alertmanager.yml.example as a template
