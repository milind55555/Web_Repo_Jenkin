🚀 CI/CD Pipeline Automation Using Jenkins
📌 Project Overview

This project demonstrates a complete CI/CD pipeline automation using Jenkins.

The pipeline automatically:

Pulls source code from GitHub

Builds the application

Creates a Docker image

Deploys a containerized static web application (index.html)

Exposes the application on a specified port

This project focuses on DevOps automation and continuous deployment practices.

🎯 Key Highlights

✅ Jenkins Pipeline (Declarative)

✅ Automated GitHub Integration

✅ Docker Image Build Automation

✅ Automated Container Deployment

✅ Zero Manual Deployment

✅ CI/CD Best Practices Implementation

🏗 Architecture

Developer Push → GitHub → Jenkins Pipeline Trigger →
Build Stage → Docker Image Creation →
Container Deployment → Application Live

🛠 Tech Stack
Layer	Technology
CI/CD	Jenkins
Containerization	Docker
SCM	GitHub
Deployment	Docker Container
Frontend	HTML
OS	Linux / WSL
📂 Project Structure
jenkins-automation-project/
│
├── Jenkinsfile
├── Dockerfile
├── index.html
└── README.md
🔄 Jenkins Pipeline Stages
1️⃣ Checkout Code

Pulls latest source from GitHub repository.

2️⃣ Build Docker Image

Builds Docker image from Dockerfile.

docker build -t my-web-app .
3️⃣ Stop Existing Container (If Running)
docker rm -f my-web-container || true
4️⃣ Deploy Container
docker run -d -p 8080:80 --name my-web-container my-web-app
🐳 Dockerfile Example
FROM nginx:latest
COPY index.html /usr/share/nginx/html/index.html
EXPOSE 80
🚀 How to Run Manually (Without Jenkins)
docker build -t my-web-app .
docker run -d -p 8080:80 my-web-app

Open:

http://localhost:8080
⚙ Jenkins Setup

Installed Jenkins locally

Configured pipeline project

Connected GitHub repository

Added Jenkinsfile

Enabled automatic build triggers

📈 What This Project Demonstrates

CI/CD automation

Infrastructure as Code

Container-based deployment

DevOps workflow understanding

Automated build & deployment lifecycle

Zero-downtime redeployment strategy

🔐 Best Practices Implemented

Declarative Jenkins Pipeline

Containerized deployment

Reproducible builds

Automated container replacement

Clean deployment workflow

💼 Resume Description

Designed and implemented a CI/CD pipeline using Jenkins to automate Docker image build and container deployment of a static web application. Integrated GitHub with Jenkins for automated builds and zero manual deployment.
