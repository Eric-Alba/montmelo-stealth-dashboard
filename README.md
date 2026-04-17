# 🏎️ Circuit de Barcelona-Catalunya | Stealth Dashboard

Este proyecto despliega un **Dashboard Técnico** optimizado para la monitorización del Circuit de Barcelona-Catalunya. La infraestructura está diseñada bajo un modelo de **Alta Disponibilidad** utilizando contenedores Docker.

---

## 📸 Evidències de Funcionament

### 1. Web Funcionant
Aquesta captura mostra el Dashboard actiu amb el mapa i la telemetria:
![Web Funcionant](<img width="1919" height="981" alt="image" src="https://github.com/user-attachments/assets/e10cd367-61c6-4322-b07f-4159f052b0b6" />)

### 2. Balanceig de Càrrega (HTTP Headers)
Aquí es pot veure com les capçaleres identifiquen quin backend està servint la petició (Apache 1 y Apache 2).
![Evidence Balanceig](<img width="1104" height="624" alt="image" src="https://github.com/user-attachments/assets/952aa7ad-c6c0-40ec-a185-395796ad2deb" />
)

### 3. Memòria Cau (Cache HIT/MISS)
Evidència que el sistema de cache està configurat correctament.
![Evidence Cache](<img width="351" height="211" alt="image" src="https://github.com/user-attachments/assets/000360c9-00c1-4e26-8bbe-402d5d488985" />)

---

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

docker logs -f nginx_balancer


---

## 📊 Detalles del Dashboard

- **Trazado Técnico**: Mapa detallado del circuito de Montmeló.
- **Calendario 2026**: Fechas clave para MotoGP, F1 y ELMS.
- **Análisis Multimedia**: Onboards técnicos de alta velocidad.

---

## 👨‍💻 Desarrollo

- **Developer**: eric.alba.ramirez
- **Docker User**: naipeer
