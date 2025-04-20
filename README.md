# 🚀 Deploy Node.js Docker Container to AWS Fargate with CI/CD Pipeline

This project demonstrates how to containerize a simple Node.js application using Docker and deploy it to **AWS ECS Fargate**, with a fully automated **CI/CD pipeline powered by GitHub Actions**.

---

## 📌 Project Overview

### 🔧 Tech Stack:
- **Node.js** (Express.js)
- **Docker**
- **Amazon ECS (Fargate)**
- **GitHub Actions** (for CI/CD)
- **DockerHub** (image repository)
- **AWS CLI** + ECS Task Definitions

---

## 🧠 Why This Project Matters

In the real-world DevOps environment, the ability to:
- **Containerize applications**
- **Push to a container registry**
- **Automate deployment to cloud services**
- **Use CI/CD for consistency and speed**

...is **essential**.

This project brings all of those concepts together in one hands-on example. It provides a real-world simulation of how modern apps are built, tested, and deployed in **cloud-native architectures**.

---

## ✅ Features

- Lightweight Node.js app using Express
- Dockerfile to build container image
- ECS Task Definition for AWS Fargate
- GitHub Actions workflow:
  - Caches Docker layers to improve build speed
  - Builds and pushes Docker image to DockerHub
  - Deploys image to AWS ECS Fargate

---

## 🏗️ Project Structure

