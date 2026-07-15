# Docker Compose Capstone Project

## Project Overview

This project demonstrates how to containerize and deploy a multi-container application using Docker, Docker Compose, and AWS EC2.

The application consists of three services:

* **Frontend** (Nginx)
* **Backend** (Node.js)
* **MySQL Database**

All services are orchestrated using Docker Compose and deployed on an AWS EC2 instance.

---

## Tech Stack

* Docker
* Docker Compose
* Node.js
* Nginx
* MySQL 8
* AWS EC2
* Git & GitHub

---

## Project Structure

```text
docker-compose-capstone/
│
├── frontend/
│   ├── Dockerfile
│   └── index.html
│
├── backend/
│   ├── Dockerfile
│   ├── index.js
│   └── package.json
│
├── docker-compose.yml
├── README.md
```

---

## Services

### Frontend

* Nginx
* Exposes Port **80**

### Backend

* Node.js Application
* Exposes Port **5000**

### Database

* MySQL 8
* Exposes Port **3306**
* Persistent storage using Docker Volumes

---

## Docker Compose Architecture

```text
Browser
   |
   | HTTP (80)
   |
Frontend (Nginx)
   |
Backend (Node.js)
   |
MySQL Database
```

---

## Prerequisites

Before running this project, install:

* Docker
* Docker Compose
* Git

---

## Clone Repository

Using HTTPS

```bash
git clone https://github.com/Omiizx2003/docker-compose-capstone.git
```

Using SSH

```bash
git clone git@github.com:Omiizx2003/docker-compose-capstone.git
```

---

## Build Containers

```bash
docker compose build
```

---

## Run Containers

```bash
docker compose up -d
```

---

## Verify Running Containers

```bash
docker ps
```

Expected containers:

* frontend
* backend
* mysql

---

## Test Application

Frontend

```bash
curl http://localhost
```

Output

```text
Docker Capstone Project
```

Backend

```bash
curl http://localhost:5000
```

Output

```text
Backend Running
```

---

## Deploy on AWS EC2

### Install Docker

```bash
sudo dnf install docker -y
sudo systemctl enable docker
sudo systemctl start docker
sudo usermod -aG docker ec2-user
newgrp docker
```

### Install Git

```bash
sudo dnf install git -y
```

### Clone Repository

```bash
git clone git@github.com:Omiizx2003/docker-compose-capstone.git
```

### Start Application

```bash
cd docker-compose-capstone

docker compose up --build -d
```

---

## Verify on EC2

```bash
docker ps
```

Open in browser

```text
http://<EC2-PUBLIC-IP>
```

---

## Useful Docker Commands

View Containers

```bash
docker ps
```

View Images

```bash
docker images
```

View Logs

```bash
docker compose logs
```

Stop Containers

```bash
docker compose down
```

Restart Containers

```bash
docker compose restart
```

Rebuild Containers

```bash
docker compose up --build
```

---

## Features

* Multi-container deployment
* Docker Compose networking
* Persistent MySQL volume
* AWS EC2 deployment
* GitHub version control
* Simple frontend and backend communication

---

## Learning Outcomes

* Docker Fundamentals
* Writing Dockerfiles
* Docker Compose
* Container Networking
* Persistent Volumes
* AWS EC2 Deployment
* Linux Administration
* Git and GitHub

---

## Author

Omkar


