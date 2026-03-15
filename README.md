Multi-Service Docker Application

A containerized web application demonstrating a multi-service architecture using Docker and Docker Compose.

The application includes a frontend UI, backend API, reverse proxy, and database, each running in its own container.

Architecture

User Request → NGINX Reverse Proxy → Backend API → Database

NGINX routes incoming requests and connects the frontend with the backend service.

Tech Stack

Frontend

HTML

NGINX

Backend

Python

Flask

Infrastructure

Docker

Docker Compose

Database

PostgreSQL

Project Structure

frontend/

Dockerfile – Builds the frontend container

src/index.html – Application UI

backend/

Dockerfile – Builds the backend container

app.py – Flask API server

requirements.txt – Python dependencies

nginx/

Dockerfile – Builds the NGINX container

nginx.conf – Reverse proxy configuration

scripts/

init-db.sql – Database initialization script

Root Files

docker-compose.yml – Runs all services together

README.md – Project documentation

Run the Project

Prerequisites

Docker

Docker Compose

Start the application:

docker compose up --build

Open in browser:

http://localhost

Click Call Backend API to test the backend connection.

DevOps Concepts Demonstrated

Containerization with Docker

Multi-container architecture

Reverse proxy using NGINX

Backend API service

Database initialization with SQL scripts

Service orchestration with Docker Compose

Author

Developed by Aathe
