# Multi-Environment DevOps Project (Jenkins + Docker + AWS EC2)

## 📌 Overview
This project demonstrates a simple DevOps implementation for deploying an application across **Development (DEV)**, **Testing (TEST)**, and **Production (PROD)** environments using **Jenkins, Docker, and AWS EC2**.  
Each environment has its own configuration, Docker deployment, and Jenkins pipeline to ensure proper isolation and controlled releases.

---

## 🛠️ Tech Stack
- Node.js (Express)
- Docker
- Jenkins (Declarative Pipelines)
- AWS EC2
- Git & GitHub

---

## 📂 Project Structure

---

## 🌍 Environments
| Environment | Branch | Port | Config File |
|-----------|--------|------|-------------|
| DEV | dev | 3000 | .env.dev |
| TEST | test | 3001 | .env.test |
| PROD | main | 3002 | .env.prod |

---

## ⚙️ Environment Configuration
Each environment uses its own `.env` file for configuration such as:
- Application environment
- Logging level
- Database URL
- Debug mode

Example:
NODE_ENV=development
LOG_LEVEL=debug
DB_URL=local-database

---

## 🐳 Docker
The application is containerized using Docker.  
Separate images are built for each environment and run with environment-specific configuration files.

---

## 🚀 CI/CD with Jenkins
This project uses **three Jenkins pipelines**:
- **DEV Pipeline** – Triggered on push to `dev` branch
- **TEST Pipeline** – Triggered on push to `test` branch
- **PROD Pipeline** – Triggered on merge to `main` branch with manual approval

Each pipeline performs:
- Code checkout
- Dependency installation
- Build & test
- Docker image creation
- Deployment to respective EC2 instance

---

## ☁️ Deployment
- Deployed on **AWS EC2**
- Docker containers run independently for DEV, TEST, and PROD
- Separate ports and configurations per environment

---

## 🌿 Branching Strategy
dev → test → main


---

## ✅ Verification
- Environment-specific configurations are loaded correctly
- Separate Jenkins pipelines for each environment
- Docker containers run independently
- Safe production deployment with manual approval

---

## 📘 Learning Outcomes
- Multi-environment DevOps architecture
- Jenkins declarative pipelines
- Docker-based deployments
- Environment isolation and configuration management
- AWS EC2 deployment

---

## 👤 Author
**Name:** SATTURI PRASHANTH GOUD  
**Role:** AWS DevOps Engineer  

---

## 📅 Date
10/05/2024
