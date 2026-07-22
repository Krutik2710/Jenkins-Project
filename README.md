# 🚀 Complete End-to-End Jenkins CI/CD Pipeline for Kubernetes

A production-inspired CI/CD pipeline built from scratch using **Jenkins**, **Maven**, **SonarQube**, **Trivy**, **Docker**, **ArgoCD**, **Kubernetes**, and **GitOps**.

This project demonstrates how modern DevOps pipelines automate the entire software delivery lifecycle—from source code commit to production deployment on Kubernetes.

---

# 📌 Project Overview

This project implements a complete Continuous Integration and Continuous Deployment (CI/CD) pipeline that automatically:

- Builds a Java Spring Boot application
- Performs code quality analysis
- Scans for vulnerabilities
- Builds Docker images
- Pushes images to Docker Hub
- Updates Kubernetes manifests
- Deploys automatically using ArgoCD

The objective was to simulate a production-grade DevOps workflow while learning how each tool integrates into the software delivery lifecycle.

---

# 🏗️ Architecture

<p align="center">

<img width="1386" height="565" alt="1783867455724" src="https://github.com/user-attachments/assets/ebf6bfb3-c63a-489e-b95b-f7523902e805" />


</p>

---

# ⚙️ Tech Stack

| Category | Technologies |
|-----------|--------------|
| CI | Jenkins |
| Build Tool | Maven |
| Code Quality | SonarQube |
| Security | Trivy |
| Containerization | Docker |
| Container Registry | Docker Hub |
| CD | ArgoCD |
| Orchestration | Kubernetes |
| SCM | GitHub |
| Language | Java (Spring Boot) |

---

# 🚀 Pipeline Workflow

```text
Developer

↓

Git Push

↓

GitHub Repository

↓

Jenkins Pipeline

↓

Git Checkout

↓

Maven Build

↓

Unit Tests

↓

SonarQube Analysis

↓

Trivy Security Scan

↓

Docker Build

↓

Docker Push

↓

Update Kubernetes Manifest

↓

Git Commit

↓

ArgoCD

↓

Kubernetes

↓

Application Deployment
```

---

# 🔄 CI/CD Flow

## Continuous Integration

Every Git push automatically triggers Jenkins.

Pipeline stages include:

- Checkout Source Code
- Maven Build
- Unit Testing
- SonarQube Analysis
- Quality Gate Validation
- Trivy Vulnerability Scan
- Docker Image Build
- Docker Image Push
- Kubernetes Manifest Update

---

## Continuous Delivery

After Jenkins updates the deployment manifest:

- Git repository changes
- ArgoCD detects the update
- Kubernetes performs Rolling Update
- Application is deployed automatically

No manual deployment is required.

---

# 📂 Repository Structure

```text
.
├── spring-boot-app/
│
├── kubernetes/
│
├── Jenkinsfile
│
├── Dockerfile
│
└── README.md
```

---

# 🔥 Jenkins Pipeline Stages

## 1️⃣ Checkout

Downloads the latest source code from GitHub.

---

## 2️⃣ Maven Build

Compiles the application and packages it into a deployable JAR.

---

## 3️⃣ Unit Tests

Runs application tests to validate functionality.

---

## 4️⃣ SonarQube Analysis

Performs static code analysis to detect:

- Bugs
- Code Smells
- Vulnerabilities
- Maintainability Issues

---

## 5️⃣ Quality Gate

Stops deployment if the code quality does not meet defined standards.

---

## 6️⃣ Trivy Scan

Scans:

- Source code
- Dependencies
- Docker image

for known vulnerabilities.

---

## 7️⃣ Docker Build

Creates a Docker image for the application.

---

## 8️⃣ Docker Push

Publishes the Docker image to Docker Hub.

---

## 9️⃣ GitOps Manifest Update

Automatically updates the Kubernetes Deployment with the latest image version.

---

## 🔟 ArgoCD Deployment

ArgoCD detects the Git change and synchronizes the Kubernetes cluster automatically.

---

# 🔒 Security

Pipeline includes automated security checks:

- Static Code Analysis
- Vulnerability Scanning
- Quality Gates
- Immutable Docker Images

---

# 📊 Key Features

✅ Fully Automated CI/CD

✅ Jenkins Declarative Pipeline

✅ Maven Build Automation

✅ SonarQube Code Analysis

✅ Trivy Vulnerability Scanning

✅ Docker Image Versioning

✅ GitOps Workflow

✅ Kubernetes Deployment

✅ Automatic Rolling Updates

---

# 💡 Challenges Solved

During implementation several real-world problems were encountered and resolved.

### Docker Agent Permission Issues

Configured Docker socket mounting inside Jenkins agents to allow Docker builds.

---

### SonarQube Integration

Configured authentication and Quality Gates to stop deployments on failed analysis.

---

### Docker Hub Authentication

Used Jenkins Credentials to securely authenticate with Docker Hub.

---

### GitOps Manifest Updates

Implemented automated Deployment manifest updates after every successful image build.

---

### ArgoCD Synchronization

Configured ArgoCD to continuously monitor Git and automatically deploy updated manifests.

---

# 📈 Pipeline Benefits

- Faster deployments
- Repeatable builds
- Automated quality checks
- Security validation
- Zero manual deployment
- GitOps workflow
- Improved release confidence

---

# 🚀 Future Improvements

- Jenkins Shared Libraries
- Helm Charts
- Kubernetes Secrets
- AWS EKS Deployment
- Terraform Infrastructure Provisioning
- Slack Notifications
- Blue/Green Deployment
- Canary Releases

---

# 🧠 Key Learnings

Through this project I gained hands-on experience with:

- Jenkins Pipeline Development
- Declarative Pipeline Syntax
- CI/CD Design
- Docker Automation
- SonarQube Integration
- Trivy Security Scanning
- GitOps Workflows
- ArgoCD Deployment
- Kubernetes Deployments
- Pipeline Troubleshooting

---

# 👨‍💻 Author

**Krutik Ukunde**

Cloud Infrastructure & DevOps Engineer

AWS Certified Solutions Architect – Associate

Certified Kubernetes Administrator (CKA)

Passionate about Cloud, DevOps, Kubernetes & Site Reliability Engineering

---

⭐ If you found this project useful, consider giving it a Star!
