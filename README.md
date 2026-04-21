#  CI/CD Multi-Container Deployment with Docker Compose

This project demonstrates a real-world CI/CD pipeline for deploying a multi-container Node.js application using Docker Compose on AWS EC2.

Any change pushed to GitHub is automatically built, pushed to Docker Hub, and deployed to the server without manual intervention.

---

##  Project Overview

This project deploys a Node.js REST API connected to a MongoDB database using Docker Compose.

Both services run in separate containers and are orchestrated using Docker Compose. The deployment process is fully automated using GitHub Actions and AWS EC2.

---

##  Architecture

GitHub → GitHub Actions → Docker Hub → AWS EC2 → Docker Compose → App + MongoDB

---

##  Tech Stack

* Node.js
* MongoDB
* Docker
* Docker Compose
* GitHub Actions
* Docker Hub
* AWS EC2
* CI/CD Pipeline

---

##  CI/CD Workflow

1. Developer pushes code to GitHub
2. GitHub Actions builds Docker image
3. Image is pushed to Docker Hub
4. AWS EC2 pulls latest image
5. Docker Compose redeploys the full stack
6. Application is updated automatically

---

##  Docker Compose Services

* **app** → Node.js REST API
* **mongo** → MongoDB database

The app connects to MongoDB using the service name as hostname.

---

## Testing

curl http://localhost:3000/tasks

Returns tasks from MongoDB, confirming both containers are running successfully.

---

##  Skills Demonstrated

* CI/CD pipeline design and automation
* Docker Compose multi-container architecture
* AWS EC2 deployment
* MongoDB container integration
* GitHub Actions workflows
* Docker Hub image registry
* Container networking
