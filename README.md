# Grafana Deployment on AWS ECS Fargate

This project demonstrates deploying **Grafana** (open-source monitoring dashboard) on **Amazon ECS Fargate**.  
The goal was to run Grafana as a containerized application in a **serverless environment**, exposing port `3000` for web access.

---

## 📌 Tools & Services
- **Amazon ECS** – Container orchestration service
- **AWS Fargate** – Serverless compute for running containers
- **Docker Hub** – Pulled the official Grafana image (`grafana/grafana`)
- **Amazon VPC** – Networking with public subnets & Internet Gateway
- **Security Groups** – Allowed inbound traffic on port `3000`
- **IAM Roles** – Task execution role for ECS

---

## 🚀 Deployment Summary
1. Created a VPC with **public subnets** and attached an **Internet Gateway**.
2. Configured a **Security Group** to allow inbound traffic on **port 3000**.
3. Defined an **ECS Task Definition** using the Docker image `grafana/grafana:latest`.
4. Created an **ECS Service** using the **Fargate** launch type.
5. Verified Grafana was accessible at `http://18.234.167.103:3000`.

---

## 📂 Repository Contents
- [`task-definitions/grafana-task-def.json`](task-definitions/grafana-task-def.json) → ECS Task Definition file  
- [`docs/ecs-service-steps.md`](docs/ecs-service-steps.md) → Detailed ECS deployment guide  

---

## 🔗 Accessing Grafana
- **Port:** 3000  
 

Once deployed, Grafana can be accessed via the public IP or Load Balancer DNS name.

