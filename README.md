# 🚀 EcomTelemetry - OpenTelemetry Demo E-Commerce Application

## 📝 Project Overview

EcomTelemetry is an open-source, microservices-based **e-commerce** application, inspired by the **OpenTelemetry Demo** project. It demonstrates **observability**, **scalability**, and **automation** best practices for deploying and managing modern cloud-native applications on AWS using Kubernetes.

This project showcases a complete **CI/CD workflow**, **infrastructure provisioning**, and **GitOps** deployment strategies—making it a comprehensive example for **DevOps engineers** and **cloud practitioners**.

---

## ✨ Key Features

✅ Microservices architecture deployed on **Kubernetes (EKS)**  
✅ **Infrastructure as Code (IaC)** with **Terraform** for AWS provisioning  
✅ Automated **CI/CD pipelines** via **GitHub Actions** and **Argo CD (GitOps)**  
✅ **Custom domain mapping** with AWS Route 53  
✅ **End-to-End automation** from code commit to deployment  
✅ Comprehensive **observability** inspired by OpenTelemetry  
✅ Fully documented **architecture diagrams**, **screenshots**, and **demo videos**

---

## 🏗️ Project Architecture

A high-level **Project Architecture Diagram** provides an overview of system design and component interactions.

📌 **Project Architecture Diagram:**  
![Project Architecture Diagram](./assets/project-architecture.png)

---

## ☁️ Infrastructure Setup Using Terraform

The complete infrastructure setup for this project has been implemented using the following GitHub repository:

🔗 **[Terraform AWS EKS Repository](#)** *(Insert your repository link here)*

This repo includes all necessary **Terraform code** to provision AWS resources:  
✅ Elastic Kubernetes Service (**EKS**)  
✅ Virtual Private Cloud (**VPC**)  
✅ IAM roles & policies  
✅ Security Groups  
✅ S3 buckets  
✅ DynamoDB (for state locking)

📌 **Terraform Infrastructure Setup Screenshots:**  
- [VPC & Subnets Provisioning](./assets/vpc-subnets.png)  
- [EKS Cluster Creation](./assets/eks-cluster.png)  
- [IAM Roles & Policies](./assets/iam-roles.png)  
- [S3 Backend Configuration](./assets/s3-backend.png)

---

## 💡 Open Source Acknowledgement

This project is **inspired by OpenTelemetry**, and full credit goes to the **OpenTelemetry team** and **Abhishek Veermalla**.  
Abhishek worked hard to create the necessary files for this project, explained them in detail, and demonstrated their usage.  
Please check out his GitHub profile for more insightful content and projects:  
👉 **[Abhishek Veermalla's GitHub](https://github.com/iam-veeramalla)**

---

## 🚀 Deployment Details

The application is accessed via the **frontendproxy service**, mapped to a **custom domain** using **AWS Route 53**.

### 🔧 Domain & DNS Configuration:  
- Domain mapping and DNS setup have been thoroughly documented with screenshots and videos for clarity.

📌 **Route 53 & DNS Configuration Screenshots:**  
- [Route 53 Hosted Zone Setup](./assets/route53-hosted-zone.png)  
- [DNS Records for Domain Mapping](./assets/dns-records.png)  
- [FrontendProxy Service Exposure](./assets/frontendproxy-service.png)

Deployment was carried out using the **`complete-deploy.yaml`**, containing manifests for all **microservices** and **Kubernetes components**.

---

## 🗺️ Project Services Architecture

📌 **Services Architecture Diagram:**  
![Services Architecture Diagram](./assets/services-architecture.png)

---

## 🔄 CI/CD Pipeline and GitOps Implementation

I implemented an automated **CI/CD pipeline** leveraging **GitHub Actions** and **Argo CD**, specifically managing the deployment of the `productcatalog` microservice.

### ⚙️ CI/CD Workflow Details:
✅ On **push** or **pull_request** events:  
- GitHub Actions build a **Docker image**  
- Push it to **DockerHub** (or ECR)  
- Update the **image tag** in the Git repo  
- Argo CD detects changes, syncs, and performs a **rolling update**

📌 **CI/CD Pipeline Screenshots:**  
- [GitHub Actions Workflow Run](./assets/github-actions-workflow.png)  
- [Docker Image Build & Push](./assets/docker-image-push.png)  
- [Argo CD Sync Operation](./assets/argo-cd-sync.png)  
- [Rolling Update in Progress](./assets/rolling-update.png)

---

## 🛠️ Tech Stack

| Category                 | Tools & Technologies   |
|--------------------------|------------------------|
| ☁️ Cloud Provider        | AWS                   |
| 🚢 Orchestration         | Kubernetes (EKS)      |
| ⚙️ IaC                  | Terraform             |
| 🔄 CI/CD                | GitHub Actions, Argo CD |
| 🐳 Containers           | Docker                |
| 🔍 Observability         | OpenTelemetry         |
| 🌐 DNS/Domain            | AWS Route 53          |
| 📦 Artifact Registry     | DockerHub / ECR       |
| 🔧 Version Control       | GitHub                |

---

## 🌟 Project Highlights

✅ Designed and deployed a **highly available microservices-based application** on AWS EKS  
✅ Developed **infrastructure automation** using Terraform  
✅ Implemented **GitOps** workflows with Argo CD for automated deployments  
✅ Automated CI/CD pipelines with GitHub Actions, including Docker image build, push, and Argo CD sync  
✅ Configured **custom domain and DNS routing** using AWS Route 53  
✅ Delivered complete documentation, diagrams, screenshots, and videos for **easy reproducibility**

---

## 🔗 Repository Access & Portfolio

The complete project, along with detailed documentation, architecture diagrams, screenshots, and demo videos, will be available at:  
➡️ **GitHub Profile:** [Insert GitHub URL]  
➡️ **Portfolio Website:** [Insert Portfolio URL]  

Repository links will be shared in my **CV**.

---

## 📸 Screenshots & Demo Videos

Screenshots and video assets are available in the `/assets` folder (or as per your repo structure):  
🖼️ **Infrastructure Setup**  
🖼️ **CI/CD Pipelines**  
🖼️ **DNS/Route 53 Configuration**  
📹 **Video Walkthroughs**

---

##  Thank you :)
