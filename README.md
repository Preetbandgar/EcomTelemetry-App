# 🚀 EcomTelemetry - OpenTelemetry E-Commerce Application

## 📝 Project Overview

EcomTelemetry is an open-source, microservices-based **e-commerce** application, inspired by the **OpenTelemetry Demo** project. It demonstrates **observability**, **scalability**, and **automation** best practices for deploying and managing modern cloud-native applications on AWS using Kubernetes.

This project showcases a complete **CI/CD workflow**, **infrastructure provisioning**, and **GitOps** deployment strategies—making it a comprehensive example for **DevOps engineers** and **cloud practitioners**.

## 🏗️ Project Architecture

A high-level **Project Architecture Diagram** provides an overview of system design and component interactions.

📌 **Project Architecture Diagram:**  
![Project Architecture Diagram](./assets/diagrams/architecture-diagram.png)

## 🛠️ Tech Stack

| Category                 | Tools & Technologies    |
|--------------------------|------------------------ |
| ☁️ Cloud Provider        | AWS                     |
| 🚢 Orchestration         | Kubernetes (EKS)        |
| ⚙️ IaC                   | Terraform               |
| 🔄 CI/CD                 | GitHub Actions, Argo CD |
| 🐳 Containers            | Docker                  |
| 🌐 DNS/Domain            | AWS Route 53            |
| 📦 Artifact Registry     | DockerHub               |
| 🔒 Security Scanning     | Trivy                   |
| 📝 Code Quality          | GolangCI-Lint           |

## ✨ Key Features

- Microservices architecture deployed on **Kubernetes (EKS)**
- **Infrastructure as Code (IaC)** with **Terraform** for AWS provisioning
- Automated **CI/CD pipelines** via **GitHub Actions** and **Argo CD (GitOps)**
- **Custom domain mapping** with AWS Route 53: [www.devopswithpritam.info](./assets/screenshots/Otel_demo_custom-domain.png)
- **End-to-End automation** from code commit to deployment

## ☁️ Infrastructure Setup Using Terraform

The complete infrastructure setup for this project has been implemented using the following GitHub repository:

🔗 [Terraform AWS EKS Repository](https://github.com/Preetbandgar/Terraform-aws-eks.git)

Terraform modules are used to provision:
- **EKS Cluster**
- **VPC**
- **IAM Roles**
- **Route 53 Custom Domain Configuration**
- **S3 + DynamoDB (Terraform Backend State Management)**

## 🔄 CI/CD Pipeline and GitOps Implementation

Implemented an automated **CI/CD pipeline** using **GitHub Actions** and **Argo CD**, specifically managing the deployment of the `productcatalog` microservice.

### ⚙️ CI/CD Workflow Stages:

| Stage                      | Description                                              |
|----------------------------|----------------------------------------------------------|
| **Build**                  | Compiles the application code                           |
| **Code-Quality**           | Runs code quality checks using **SonarQube**            |
| **Go-Code-Check**          | Performs Go code analysis for best practices            |
| **Docker**                 | Builds the Docker image of the microservice             |
| **Trivy-Docker-Image-Scan**| Scans Docker images for vulnerabilities using **Trivy** |
| **UpdateK8s**              | Updates the Kubernetes manifest files with the new image tag |
| **Argo CD Sync**           | Argo CD automatically detects changes, syncs, and triggers a **rolling update** of the microservice deployment |

📌 **CI/CD Pipeline Screenshots:**  
     - [GitHub Actions Workflow Run](https://github.com/Preetbandgar/EcomTelemetry-App/actions/runs/13877069831)  
     - [GolangCI-Lint Code Quality Check](https://github.com/Preetbandgar/EcomTelemetry-App/actions/runs/13877069831/job/38830720174)  
     - [Docker Image Build & Push](https://github.com/Preetbandgar/EcomTelemetry-App/actions/runs/13877069831/job/38830720176)  
     - [Trivy Image Scan Results](https://github.com/Preetbandgar/EcomTelemetry-App/actions/runs/13877069831/job/38830729444)  
     - [Kubernetes Manifest Update](https://github.com/Preetbandgar/EcomTelemetry-App/actions/runs/13877069831/job/38830732368)  
     - [Argo CD Sync Operation](./assets/screenshots/argo-cd-sync.png)  
     - [Rolling Update in Progress](./assets/screenshots/rolling-update.png)

## 🚀 Deployment Details

The application is accessed via the **frontendproxy service**, mapped to a **custom domain** using **AWS Route 53**:  
🌐 [www.devopswithpritam.info](./assets/screenshots/Otel_demo_custom-domain.png)

### 🔧 Domain & DNS Configuration:  
Domain mapping and DNS setup have been thoroughly documented with screenshots and a dedicated demo video.

📹 **[Video: Custom Domain Mapping Demo](./assets/videos/custom-domain-demo.mp4)**

📌 **Route 53 & DNS Configuration Screenshots:**  
- [Route 53 Hosted Zone Setup](./assets/screenshots/route53-hosted-zone.png)  
- [DNS Records for Domain Mapping](./assets/screenshots/dns-records.png)  
- [FrontendProxy Service Exposure](./assets/screenshots/frontendproxy-service.png)

Deployment was carried out using the **[`complete-deploy.yaml`](./assets/screenshots/complete_deploy.png)**, containing manifests for all **microservices** and **Kubernetes components**.

## 🌟 Project Highlights

- Designed and deployed a **highly available microservices-based application** on AWS EKS
- Developed **infrastructure automation** using Terraform
- Implemented **GitOps** workflows with Argo CD for automated deployments
- Automated CI/CD pipelines with GitHub Actions, including Docker image build, push, Trivy scans and Argo CD sync
- Configured **custom domain and DNS routing** using AWS Route 53: [www.devopswithpritam.info](./assets/screenshots/Otel_demo_custom-domain.png)

## 📸 Screenshots & Demo Videos

Screenshots and video assets are available in the `/assets` folder:  
- **Infrastructure Setup**  
- **CI/CD Pipelines**  
- **DNS/Route 53 Configuration**  
- **Video Walkthroughs** (including custom domain mapping)

## 💡 Open Source Acknowledgement

This project is **inspired by OpenTelemetry**, and full credit goes to the **OpenTelemetry team** and **Mr. Abhishek Veermalla**.  
Abhishek worked hard to create the necessary files for this project, explained them in detail, and demonstrated their usage.  
Please check out his GitHub profile for more insightful content and projects:  
👉 **[Abhishek's GitHub](https://github.com/iam-veeramalla)**

## 🙏 Thank You :)
