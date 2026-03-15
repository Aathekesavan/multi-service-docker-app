# Multi-Service Docker Application

A containerized web application demonstrating a multi-service architecture using Docker and Docker Compose.

This project includes a frontend UI, backend API, reverse proxy, and database, each running in its own container.

---

## Architecture

User Request
↓
NGINX Reverse Proxy
↓
Frontend (HTML UI)
↓
Backend API (Python Flask)
↓
PostgreSQL Database

NGINX routes incoming requests to the appropriate service.

---

## Tech Stack

Frontend
- HTML
- NGINX

Backend
- Python
- Flask

Infrastructure
- Docker
- Docker Compose

Database
- PostgreSQL

---

## Project Structure

multi-service-docker-app
│
├── frontend
│   ├── Dockerfile
│   └── src
│       └── index.html
├── backend
│   ├── Dockerfile
│   ├── app.py
│   ├── requirements.txt
│   └── .dockerignore
├── nginx
│   ├── Dockerfile
│   └── nginx.conf
├── scripts
│   └── init-db.sql
├── docker-compose.yml
├── .gitignore
└── README.md
## How It Works

1. The browser loads the frontend web page.
2. When the user clicks **Call Backend API**, a request is sent to `/api`.
3. NGINX receives the request and routes it to the backend container.
4. The Flask backend processes the request and returns a response.
5. The frontend displays the returned message.

---

## Running the Project

### Prerequisites

- Docker
- Docker Compose

### Run the application


docker compose up --build


Open the application in your browser:


http://localhost


Click **Call Backend API** to test the backend connection.

---

## Containers Used

| Container | Purpose |
|--------|--------|
| frontend | Serves the web UI |
| backend | Python Flask API |
| nginx | Reverse proxy and routing |
| postgres | Database service |

---

## DevOps Concepts Demonstrated

- Containerization with Docker
- Multi-service architecture
- Reverse proxy configuration
- Environment variable configuration
- Database initialization with SQL scripts
- Service orchestration using Docker Compose

---

## Author

Developed by **Aathe**
