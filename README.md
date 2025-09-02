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

![Task Definition](https://github.com/user-attachments/assets/99d206c8-75c8-4edf-b6ac-0c2373c2a719)



4. Created an **ECS Service** using the **Fargate** launch type.

![ECS cluster](https://github.com/user-attachments/assets/341dede9-6395-4e82-9b85-66eb9371b659)



5. Verified Grafana was accessible at `http://18.234.167.103:3000`.

<img width="1908" height="891" alt="Grafana Docker image dep on ECS" src="https://github.com/user-attachments/assets/4390c899-c69b-4fc5-9380-3b15adb67391" />

---

## 📂 Repository Contents
- [`task-definitions/grafana-task-def.json`](task-definitions/grafana-task-def.json) → ECS Task Definition file  
- [`docs/ecs-service-steps.md`](docs/ecs-service-steps.md) → Detailed ECS deployment guide  

---

# Grafana Deployment on AWS ECS Fargate

![AWS](https://img.shields.io/badge/AWS-ECS-orange?logo=amazon-aws&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-Container-blue?logo=docker&logoColor=white)
![Grafana](https://img.shields.io/badge/Grafana-Monitoring-orange?logo=grafana&logoColor=white)
![Fargate](https://img.shields.io/badge/Fargate-Serverless-green?logo=amazon-aws&logoColor=white)


## 🔗 Accessing Grafana
- **Port:** 3000  
 

Once deployed, Grafana can be accessed via the public IP or Load Balancer DNS name.

