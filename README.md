# 🏎️ Circuit de Barcelona-Catalunya | Stealth Dashboard

Este proyecto despliega un **Dashboard Técnico** optimizado para la monitorización del Circuit de Barcelona-Catalunya. La infraestructura está diseñada bajo un modelo de **Alta Disponibilidad** utilizando contenedores Docker.

---

## 🛠️ Infraestructura y Balanceo de Carga

El sistema utiliza una arquitectura de clúster distribuida para asegurar la disponibilidad constante:

* **Nginx Load Balancer**: Actúa como punto de entrada único, distribuyendo el tráfico mediante un algoritmo de **Round Robin**.
* **Nodos Apache (2 Active)**: Dos servidores web independientes que sirven el contenido de forma alterna.
* **Live Telemetry**: Monitorización en tiempo real del estado del clúster mediante indicadores visuales.

---

## 🚀 Cómo poner las máquinas en funcionamiento

### 1. Clonar el repositorio

git clone https://github.com/Eric-Alba/montmelo-stealth-dashboard.git
cd montmelo-stealth-dashboard

### 2. Despliegue con Docker Compose

docker-compose up -d

### 3. Verificación del Balanceo
Observa en tiempo real cómo Nginx reparte las peticiones entre los nodos:

docker logs -f nginx_balancer


---

## 📊 Detalles del Dashboard

- **Trazado Técnico**: Mapa detallado del circuito de Montmeló.
- **Calendario 2026**: Fechas clave para MotoGP, F1 y 24h de Barcelona.
- **Análisis Multimedia**: Onboards técnicos de alta velocidad.

---

## 👨‍💻 Desarrollo

- **Developer**: eric.alba.ramirez
- **Docker User**: naipeer
