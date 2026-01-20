# Prometheus Lab 1

## Host browser
- Prometheus: http://localhost:9090
- Node Exporter metrics: http://localhost:9100/metrics
- Python app: http://localhost:5000
- Python metrics: http://localhost:5001/metrics

## Run Prometheus + Node Exporter
cd docker-compose/prometheus
docker compose up -d

## Python instrumentation
cd instrumentation
python3 -m venv venv
source venv/bin/activate
pip install prometheus_client
python3 httpserver_test.py

## Prometheus config reload
curl -X POST http://localhost:9090/-/reload
