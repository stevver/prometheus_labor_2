# Prometheus Lab 2

## Teenused
- Prometheus: http://localhost:9090
- Node Exporter (mõõdikud): http://localhost:9100/metrics
- Docker Engine mõõdikud: http://localhost:9323/metrics
- cAdvisor: http://localhost:8080
- Alertmanager: http://localhost:9093
- Grafana: http://localhost:3000

## Stacki käivitamine
```bash
cd docker-compose/prometheus
docker compose up -d
```

## Prometheus konfiguratsiooni uuesti laadimine
```bash
curl -X POST http://localhost:9090/-/reload
```

## Märkused
- `alertmanager/alertmanager.yml` on `.gitignore`’is (sisaldab Slacki webhooki URL-i)
- Kasuta `alertmanager/alertmanager.yml.example` faili mallina
