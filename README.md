# 🏎️ Circuit de Barcelona-Catalunya | Stealth Dashboard

Este proyecto despliega un **Dashboard Técnico** optimizado para la monitorización del Circuit de Barcelona-Catalunya. La infraestructura está diseñada bajo un modelo de **Alta Disponibilidad** utilizando contenedores Docker.

## 🛠️ Infraestructura y Balanceo de Carga

El sistema utiliza una arquitectura de clúster distribuida para asegurar la disponibilidad constante:

* **Nginx Load Balancer**: Actúa como punto de entrada único, distribuyendo el tráfico mediante un algoritmo de *Round Robin*.
* **Nodos Apache (2 Active)**: Dos servidores web independientes. Si uno falla, el balanceador redirige el tráfico al nodo activo automáticamente.
* **Live Telemetry**: Monitorización en tiempo real del estado del clúster.

## 🚀 Cómo poner las máquinas en funcionamiento

### 1. Clonar el repositorio
`ash
git clone [https://github.com/naipeer/montmelo-stealth-dashboard.git](https://github.com/naipeer/montmelo-stealth-dashboard.git)
cd montmelo-stealth-dashboard
2. Despliegue con Docker Compose
Levanta toda la infraestructura con un solo comando:

PowerShell
docker-compose up -d
3. Verificación del Balanceo
Observa cómo las peticiones saltan entre nodos (IPs .2 y .3) en tiempo real:

PowerShell
docker logs -f nginx_balancer
📊 Detalles del Dashboard
Trazado Técnico: Mapa detallado del circuito de Montmeló.

Calendario 2026: Fechas clave para MotoGP, F1 y ELMS.

Análisis Multimedia: Onboards técnicos de alta velocidad.

Desarrollado por: eric.alba.ramirez | Usuario Docker: naipeer
