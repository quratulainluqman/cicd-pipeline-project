# CI/CD Pipeline Project using Jenkins, Docker, Node.js, GitHub, Ubuntu WSL & VS Code

## Project Overview

This project demonstrates a complete CI/CD (Continuous Integration and Continuous Deployment) pipeline using:

* Node.js Application
* Docker Containers
* Jenkins Automation Server
* GitHub Repository Integration
* Ubuntu WSL Environment
* Visual Studio Code

The objective of this project was to automate the process of:

1. Building the application
2. Creating Docker images
3. Running Docker containers
4. Automating deployment using Jenkins Pipeline
5. Managing source code with Git and GitHub

---

# Technologies Used

| Technology | Purpose                       |
| ---------- | ----------------------------- |
| Node.js    | Backend Application           |
| Express.js | Web Framework                 |
| Docker     | Containerization              |
| Jenkins    | CI/CD Automation              |
| Git        | Version Control               |
| GitHub     | Remote Repository             |
| Ubuntu WSL | Linux Development Environment |
| VS Code    | Code Editor                   |

---

# Project Workflow

The workflow of this project follows these steps:

```text
Developer Code Changes
        ↓
Push Code to GitHub
        ↓
Jenkins Pulls Latest Code
        ↓
Docker Builds Image
        ↓
Old Container Stops
        ↓
New Container Runs Automatically
        ↓
Application Deploys Successfully
```

---

# Step-by-Step Project Setup

## Step 1 — Open Ubuntu WSL

The project development started inside Ubuntu WSL environment.

Commands used:

```bash
wsl
```

Verified current directory:

```bash
pwd
```

---

## Step 2 — Create Project Directory

Created a dedicated project folder:

```bash
mkdir cicd-project
cd cicd-project
```

---

## Step 3 — Open Project in VS Code

Opened the project workspace inside VS Code:

```bash
code .
```

This enabled development directly inside Ubuntu WSL environment.

---

## Step 4 — Create Node.js Application

Initialized a Node.js project:

```bash
npm init -y
```

Installed Express.js:

```bash
npm install express
```

Created:

```text
server.js
```

Application displays:

```text
CI/CD Pipeline Project Running Successfully!
```

---

## Step 5 — Run Node.js Application

Started the Node.js server:

```bash
node server.js
```

Application successfully ran on:

```text
http://localhost:3000
```

---

# Docker Setup

## Step 6 — Create Dockerfile

Created a Dockerfile for containerizing the application.

The Dockerfile performs:

* Base image setup
* Working directory creation
* Dependency installation
* Application copy
* Port exposure
* Application startup

---

## Step 7 — Build Docker Image

Built Docker image:

```bash
docker build -t cicd-node-app .
```

---

## Step 8 — Run Docker Container

Started Docker container:

```bash
docker run -d -p 3000:3000 --name cicd-container cicd-node-app
```

Verified running containers:

```bash
docker ps
```

---

# Git & GitHub Integration

## Step 9 — Initialize Git Repository

Initialized Git:

```bash
git init
```

Configured Git username and email:

```bash
git config --global user.name "Quratulain Luqman"
git config --global user.email "your-email@example.com"
```

---

## Step 10 — Commit Project Files

Added project files:

```bash
git add .
```

Committed files:

```bash
git commit -m "Initial CI/CD Node.js application setup"
```

---

## Step 11 — Push Project to GitHub

Connected GitHub repository:

```bash
git remote add origin https://github.com/quratulainluqman/cicd-pipeline-project.git
```

Pushed code:

```bash
git push -u origin main
```

---

# Jenkins Setup

## Step 12 — Run Jenkins using Docker

Started Jenkins container:

```bash
docker run -d --name jenkins -p 8080:8080 -p 50000:50000 \
-v jenkins_home:/var/jenkins_home jenkins/jenkins:lts
```

Verified Jenkins container:

```bash
docker ps
```

---

## Step 13 — Access Jenkins Dashboard

Opened Jenkins in browser:

```text
http://localhost:8080
```

Completed:

* Initial setup
* Plugin installation
* Admin user creation

---

# Jenkins Pipeline Setup

## Step 14 — Create Jenkinsfile

Created:

```text
Jenkinsfile
```

Pipeline stages include:

1. Clone Repository
2. Build Docker Image
3. Stop Old Container
4. Run New Container

---

## Step 15 — Configure Jenkins Pipeline Job

Created Jenkins Pipeline project.

Configured:

* GitHub repository URL
* Branch: main
* Pipeline script from SCM
* Jenkinsfile path

---

## Step 16 — Build CI/CD Pipeline

Triggered Jenkins build.

Jenkins successfully:

* Pulled latest code from GitHub
* Built Docker image
* Stopped old container
* Started updated container
* Deployed application automatically

---

# Final Result

The application was successfully deployed using a complete automated CI/CD pipeline.

Application running on:

```text
http://localhost:3000
```

Jenkins running on:

```text
http://localhost:8080
```

---

# Project Features

✅ Complete CI/CD Pipeline

✅ Dockerized Node.js Application

✅ Jenkins Automation

✅ GitHub Integration

✅ Automated Docker Deployment

✅ Ubuntu WSL Development Environment

✅ VS Code Integration

✅ Real DevOps Workflow

---

# Challenges Faced During Project

During the implementation of this project several real-world DevOps issues were encountered and resolved:

* WSL configuration issues
* Docker daemon permission issues
* Jenkins Git branch configuration problems
* GitHub authentication using Personal Access Token
* Docker socket permission errors
* Jenkins container access configuration
* Pipeline debugging and troubleshooting

These challenges helped in gaining practical DevOps troubleshooting experience.

---

# Future Improvements

Future enhancements planned for this project:

* Add Kubernetes deployment
* Integrate Docker Hub
* Add automated testing stage
* Add GitHub Webhooks
* Configure Nginx reverse proxy
* Deploy on cloud platforms such as AWS

---

# Project Screenshots

---

## Ubuntu WSL Project Initialization

![Ubuntu Setup](screenshots/ubuntu-wsl-project-initialization.png)

---

## VS Code DevOps Workspace Setup

![VS Code Workspace](screenshots/vscode-devops-workspace-setup.png)

---

## Jenkins Docker Container Setup

![Jenkins Docker](screenshots/jenkins-docker-container-setup.png)

---

## Running Docker Containers

![Docker Containers](screenshots/docker-running-containers.png)

---

## Jenkins Dashboard Setup

![Jenkins Dashboard](screenshots/jenkins-dashboard-setup.png)

---

## Node.js Application Running Successfully

![Node.js App](screenshots/nodejs-app-running.png)

---

# Conclusion

This project demonstrates a practical implementation of DevOps concepts using Jenkins, Docker, GitHub, Node.js, Ubuntu WSL, and VS Code.

The project helped in understanding:

* CI/CD workflows
* Docker containerization
* Jenkins pipeline automation
* GitHub integration
* DevOps troubleshooting
* Real deployment practices
