# 🚀 EcomTelemetry - OpenTelemetry E-Commerce Application

## 📝 Project Overview

EcomTelemetry is an open-source, microservices-based **e-commerce** application, inspired by the **OpenTelemetry Demo** project. It demonstrates **observability**, **scalability**, and **automation** best practices for deploying and managing modern cloud-native applications on AWS using Kubernetes.

This project showcases a complete **CI/CD workflow**, **infrastructure provisioning**, and **GitOps** deployment strategies—making it a comprehensive example for **DevOps engineers** and **cloud practitioners**.

## 🏗️ Project Architecture

A high-level **Project Architecture Diagram** provides an overview of system design and component interactions.

📌 **Project Architecture Diagram:**  
![Project Architecture Diagram](./assets/diagrams/architecture-diagram.png)

## 🛠️ Tech Stack

| Category | Tools & Technologies |
|----------|----------------------|
| ☁️ Cloud Provider | AWS |
| 🚢 Orchestration | Kubernetes (EKS) |
| ⚙️ IaC | Terraform |
| 🔄 CI/CD | GitHub Actions, Argo CD |
| 🐳 Containers | Docker |
| 🌐 DNS/Domain | AWS Route 53 |
| 📦 Artifact Registry | DockerHub |
| 🔒 Docker Image Scan | Trivy |
| 📝 Code Quality | GolangCI-Lint |

## ✨ Key Features

- Microservices architecture deployed on **Kubernetes (EKS)**
- **Infrastructure as Code (IaC)** with **Terraform** for AWS provisioning
- Automated **CI/CD pipelines** via **GitHub Actions** and **Argo CD (GitOps)**
- **Custom domain mapping** with AWS Route 53: [www.devopswithpritam.info](https://www.devopswithpritam.info)
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

Implemented an automated **CI/CD pipeline** using **GitHub Actions** and **Argo CD**, specifically managing the deployment of the [`productcatalog`](https://github.com/Preetbandgar/EcomTelemetry-App/tree/main/kubernetes/productcatalog) microservice.

### ⚙️ CI/CD Workflow Stages:

| Stage | Description |
|-------|-------------|
| **Build** | Compiles the application code |
| **Code-Quality** | Runs code quality checks using **SonarQube** |
| **Go-Code-Check** | Performs Go code analysis for best practices |
| **Docker** | Builds the Docker image of the microservice |
| **Trivy-Docker-Image-Scan** | Scans Docker images for vulnerabilities using **Trivy** |
| **UpdateK8s** | Updates the Kubernetes manifest files with the new image tag |
| **Argo CD Sync** | Argo CD automatically detects changes, syncs, and triggers a **rolling update** of the microservice deployment |

📌 **CI/CD Pipeline Workflow Links & Screenshots:**
- [GitHub Actions Workflow Run](https://github.com/Preetbandgar/EcomTelemetry-App/actions/runs/13877069831)
- [SonarQube Code-Quality Check](./assets/screenshots/Sonarqube_Code_Quality.png)
- [GolangCI-Lint Go-Code-Check](https://github.com/Preetbandgar/EcomTelemetry-App/actions/runs/13877069831/job/38830720174)
- [Docker Image Build & Push](https://github.com/Preetbandgar/EcomTelemetry-App/actions/runs/13877069831/job/38830720176)
- [Trivy Docker Image Scan Results](https://github.com/Preetbandgar/EcomTelemetry-App/actions/runs/13877069831/job/38830729444)
- [Kubernetes Manifest Update](https://github.com/Preetbandgar/EcomTelemetry-App/actions/runs/13877069831/job/38830732368)

### 📌 Argo CD Sync and Deployment Status:

- **Argo CD Sync Operation**  
  ![Argo CD Sync Operation](./assets/screenshots/Argocd_productcatalog-app.png)

- **Post-Sync Validation: Application Healthy and Running**  
  ![Post-Sync Validation: Application Healthy and Running](./assets/screenshots/Argocd_productcatalog-app-successful.png)

The application is accessed via the **frontendproxy service**, mapped to a **custom domain** using **AWS Route 53**:  
🌐 [www.devopswithpritam.info](https://www.devopswithpritam.info)

### 🔧 Domain & DNS Configuration:

📌 **Route 53 & DNS Configuration Screenshots:**  

- **DNS Records for Domain Mapping**  
  ![DNS Records](./assets/screenshots/dns-records.png)

- **FrontendProxy Service Exposure**  
  ![FrontendProxy Service](./assets/videos/Opentelemetry-frontendproxy-demo-eks.mp4)

Deployment was carried out using the [`complete-deploy.yaml`](./kubernetes/complete-deploy.yaml), containing manifests for all **microservices** and **Kubernetes components**.

## 🌟 Project Highlights

- Designed and deployed a **highly available microservices-based application** on AWS EKS
- Developed **infrastructure automation** using Terraform
- Implemented **GitOps** workflows with Argo CD for automated deployments
- Automated CI/CD pipelines with GitHub Actions, including Docker image build, push, Trivy scans and Argo CD sync
- Configured **custom domain and DNS routing** using AWS Route 53: [www.devopswithpritam.info](https://www.devopswithpritam.info)

## 💡 Open Source Acknowledgement

This project is **inspired by OpenTelemetry**, and full credit goes to the **OpenTelemetry team** and **Mr. Abhishek Veermalla**.  
Abhishek worked hard to create the necessary files for this project, explained them in detail, and demonstrated their usage.  
Please check out his GitHub profile for more insightful content and projects:  
👉 **[Abhishek's GitHub](https://github.com/iam-veeramalla)**

## 🙏 Thank You!