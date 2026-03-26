# KeepAlive - Uptime Monitoring & Host Health Dashboard

[![GitHub](https://img.shields.io/badge/GitHub-KeepAlive-blue?style=flat&logo=github)](https://github.com/follen99/KeepAlive)

![KeepAlive Dashboard](assets/dashboard.png)

Applicazione web moderna per monitorare la disponibilità e la salute di host/servizi remoti. Realizzata con **Flask**, **SQLite**, e **APScheduler** per eseguire check periodici automatici in background. Ideale per mantenere sotto controllo infrastrutture, siti web e servizi critici con uptime tracking e storico delle risposte.

**Tech Stack:** Python 3.9+ | Flask | SQLAlchemy | APScheduler | HTML/CSS | SQLite | Docker


## Uso con Docker Compose (consigliato)

Prima crea la cartella persistente del database:

```bash
mkdir -p instance
```

Avvio in background:

```bash
docker compose up -d --build
```

Log in tempo reale:

```bash
docker compose logs -f
```

Stop dei servizi:

```bash
docker compose down
```

L'app sarà disponibile su:

```text
http://localhost:5000
```