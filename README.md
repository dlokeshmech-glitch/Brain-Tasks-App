# 🚀 DevOps CI/CD Project – Brain Tasks App

## 📌 Project Overview

This project demonstrates a complete CI/CD pipeline using AWS services. The application is containerized using Docker, built using AWS CodeBuild, stored in Amazon ECR, and deployed on Kubernetes (Docker Desktop).

---

## 🧱 Technologies Used

* GitHub (Version Control)
* AWS CodePipeline (CI/CD Orchestration)
* AWS CodeBuild (Build & Docker Image Creation)
* Amazon ECR (Container Registry)
* Docker (Containerization)
* Kubernetes (Deployment - Docker Desktop)
* AWS CloudWatch (Monitoring)

---

## 🔄 Pipeline Flow

GitHub → CodePipeline → CodeBuild → ECR → Kubernetes → Application

---

## ⚙️ Setup Instructions

### 1. Clone Repository

```
git clone https://github.com/dlokeshmech-glitch/Brain-Tasks-App
cd Brain-Tasks-App
```

### 2. Build & Push Docker Image (Handled by CodeBuild)

* Docker image is automatically built and pushed to ECR via CI pipeline

### 3. Deploy to Kubernetes

```
kubectl apply -f deployment.yaml
kubectl apply -f service.yaml
```

### 4. Access Application

```
kubectl get svc
```

---

## 🌐 Application URL

http://localhost:31036

---

## 📊 Monitoring

* AWS CloudWatch Logs used to monitor CodeBuild execution
* CodePipeline used to track CI/CD flow

---

## ☸️ Kubernetes Commands

```
kubectl get pods
kubectl get svc
```

---

## 🧩 Architecture

GitHub → CodePipeline → CodeBuild → ECR → Kubernetes

---

## ✅ CI/CD Verification

Whenever code is pushed to GitHub:

* CodePipeline triggers automatically
* CodeBuild builds Docker image
* Image is pushed to ECR
* Kubernetes pulls latest image and runs the application

---

## ⚠️ Note

* Deployment is triggered manually using:

```
kubectl rollout restart deployment brain-app
```

* For production, AWS EKS with automated deployment can be used.

---
