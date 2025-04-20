# Deploy Node.js Docker Container to AWS Fargate with CI/CD Pipeline

This project demonstrates how to containerize a simple Node.js application using Docker and deploy it to **AWS ECS Fargate**, with a fully automated **CI/CD pipeline powered by GitHub Actions**.

---

##  Project Overview

### Tech Stack:
- **Node.js** (Express.js)
- **Docker**
- **Amazon ECS (Fargate)**
- **GitHub Actions** (for CI/CD)
- **DockerHub** (image repository)
- **AWS CLI** + ECS Task Definitions

---

##  Why This Project Matters

In the real-world DevOps environment, the ability to:
- **Containerize applications**
- **Push to a container registry**
- **Automate deployment to cloud services**
- **Use CI/CD for consistency and speed**

...is **essential**.

This project brings all of those concepts together in one hands-on example. It provides a real-world simulation of how modern apps are built, tested, and deployed in **cloud-native architectures**.

---

##  Features

- Lightweight Node.js app using Express
- Dockerfile to build container image
- ECS Task Definition for AWS Fargate
- GitHub Actions workflow:
  - Caches Docker layers to improve build speed
  - Builds and pushes Docker image to DockerHub
  - Deploys image to AWS ECS Fargate

---

# 
---

##  How It Works

### 1. **Dockerize the Node App**
The `Dockerfile` builds a lightweight image for the Node.js application.

### 2. **Push to GitHub**
When you push to GitHub, GitHub Actions triggers the workflow in `.github/workflows/deploy.yml`.

### 3. **CI/CD Pipeline (GitHub Actions)**
This workflow:
- Caches Docker layers for faster builds
- Logs in to Amazon ECR (Elastic Container Registry)
- Builds and tags the Docker image
- Pushes the image to ECR
- Updates the ECS service (Fargate) with the new image

All this happens **automatically** on every push to the `main` or `master` branch.

---

## Secrets Configuration in GitHub

Set these secrets in your repository settings under **Settings > Secrets and variables > Actions**:

- `AWS_ACCESS_KEY_ID`
- `AWS_SECRET_ACCESS_KEY`
- `AWS_REGION` (e.g., `us-east-1`)
- `ECR_REGISTRY` (e.g., `123456789012.dkr.ecr.us-east-1.amazonaws.com`)
- `ECR_REPOSITORY` (e.g., `node-app`)
- `ECS_SERVICE` (e.g., `node-app-service`)
- `ECS_CLUSTER` (e.g., `node-cluster`)
- `ECS_TASK_DEFINITION` (JSON file path or ARN)

---

## Why This Project Is Important

###  Real-World DevOps Practice
Learn how companies manage production-grade app deployments with containerized services.

###  Serverless Containers with Fargate
No need to manage EC2 instances. AWS Fargate simplifies container orchestration and scaling.

### CI/CD Automation
Reduces manual errors, increases deployment speed, and supports continuous delivery.



---

## Deployment Prerequisites

- AWS account with ECS Fargate, IAM roles, and ECR set up
- GitHub repository with the secrets configured
- Docker installed locally for development and testing

---

##  Testing Locally

```bash
docker build -t node-app .
docker run -p 3000:3000 node-app


