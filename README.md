# Monitoreo con Prometheus + Grafana

Proyecto de monitorización de infraestructura Linux usando Docker, Prometheus, Grafana y Node Exporter.

## Objetivo

Desplegar un stack de observabilidad completo para monitorizar métricas de sistema (CPU, memoria, disco, red) de uno o varios servidores Linux, con visualización en dashboards.

## Tecnologías

- Docker / Docker Compose
- Prometheus
- Grafana
- Node Exporter

## Requisitos e instalación

### 1. Sistema base

Ubuntu Server 22.04/24.04 LTS.

### 2. Instalar Docker

\`\`\`bash
sudo apt update
sudo apt install -y ca-certificates curl gnupg
sudo install -m 0755 -d /etc/apt/keyrings
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg
echo "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu $(. /etc/os-release && echo $VERSION_CODENAME) stable" | sudo tee /etc/apt/sources.list.d/docker.list
sudo apt update
sudo apt install -y docker-ce docker-ce-cli containerd.io docker-compose-plugin
sudo usermod -aG docker $USER
\`\`\`

Verifica la instalación:

\`\`\`bash
docker --version
docker compose version
\`\`\`

## Estado del proyecto

- [x] Fase 0: Estructura inicial del repositorio
- [x] Fase 1: Instalación de Docker
- [x] Fase 2: Docker Compose (Prometheus, Grafana, Node Exporter)
- [x] Fase 3: Configuración de Prometheus
- [x] Fase 4: Conexión y dashboards en Grafana
- [x] Fase 5: Provisioning de Grafana como código
- [x] Fase 6: Alertas con Prometheus + Alertmanager
