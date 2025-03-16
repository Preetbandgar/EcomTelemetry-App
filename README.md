# 🚀 EcomTelemetry - OpenTelemetry Demo E-Commerce Application

## 📝 Project Overview

**EcomTelemetry** is an open-source, microservices-based **e-commerce** application inspired by the **OpenTelemetry Demo** project. It demonstrates **observability**, **scalability**, and **automation** best practices for deploying and managing modern cloud-native applications on AWS using Kubernetes.

This project demonstrates end-to-end DevOps practices, including CI/CD pipelines, infrastructure automation, and GitOps deployment, providing a practical example for DevOps and cloud professionals.
---

## ✨ Key Features

✅ Microservices architecture deployed on **Kubernetes (EKS)**  
✅ **Infrastructure as Code (IaC)** with **Terraform** for AWS provisioning  
✅ Automated **CI/CD pipelines** via **GitHub Actions** and **Argo CD (GitOps)**  
✅ **Custom domain mapping** with **AWS Route 53**  
✅ **End-to-End automation** from code commit to deployment  
✅ Comprehensive **observability** inspired by **OpenTelemetry**  
✅ Fully documented **architecture diagrams**, **screenshots**, and **demo videos**

---

## 🏗️ Project Architecture

A high-level **Project Architecture Diagram** provides an overview of system design and component interactions.

📌 **Project Architecture Diagram:**  
![Project Architecture Diagram](./assets/project-architecture.png)

---

## ☁️ Infrastructure Setup Using Terraform

The complete infrastructure setup for this project has been implemented using the following GitHub repository:

🔗 [Terraform AWS EKS Repository](https://github.com/Preetbandgar/EcomTelemetry-App.git)

This repository includes all necessary **Terraform code** to provision AWS resources:  
✅ Elastic Kubernetes Service (**EKS**)  
✅ Virtual Private Cloud (**VPC**)  
✅ IAM roles & policies  
✅ Security Groups  
✅ S3 Buckets  
✅ DynamoDB (for remote state locking and consistency)

---

## 💡 Open Source Acknowledgement

This project is **inspired by OpenTelemetry**, and full credit goes to the **OpenTelemetry team** and **Abhishek Veermalla**.  
Abhishek worked hard to create the foundational files for this project, explained them in detail, and demonstrated their usage.  
Please check out his GitHub profile for more insightful content and projects:  
👉 **[Abhishek Veermalla's GitHub](https://github.com/iam-veeramalla)**

---

## 🚀 Deployment Details

The application is accessed via the **frontendproxy service**, mapped to a **custom domain** using **AWS Route 53**.

### 🔧 Domain & DNS Configuration  
Domain mapping and DNS setup have been thoroughly documented with screenshots and demo videos for clarity.

📌 **Route 53 & DNS Configuration Screenshots:**  
- [Route 53 Hosted Zone Setup](./assets/route53-hosted-zone.png)  
- [DNS Records for Domain Mapping](./assets/dns-records.png)  
- [FrontendProxy Service Exposure](./assets/frontendproxy-service.png)

Deployment was carried out using the **`complete-deploy.yaml`**, containing manifests for all **microservices** and **Kubernetes components**.

---

## 🔄 CI/CD Pipeline and GitOps Implementation

The project implements an end-to-end **CI/CD pipeline** using **GitHub Actions** integrated with **Argo CD**, managing the build, scan, deployment, and synchronization workflows.

### ⚙️ CI/CD Workflow Details

Each time a **push** or **pull_request** event occurs in the GitHub repository, the following stages are triggered as part of the **CI/CD pipeline**:

1. **`build`**  
   ✅ Compile and build the `productcatalog` microservice code (Go application).  
   ✅ Validate the build output for correctness.

2. **`code-quality`**  
   ✅ Run **SonarQube** for static code analysis and enforce quality gates.  
   ✅ Ensure code adheres to best practices and maintainability standards.

3. **`go-code-check`**  
   ✅ Execute **GolangCI-Lint** for Go code linting.  
   ✅ Identify and fix coding issues, inefficiencies, and potential bugs.

4. **`docker`**  
   ✅ Build Docker images of the `productcatalog` microservice.  
   ✅ Tag and push images to **DockerHub** securely.

5. **`trivy-docker-image-scan`**  
   ✅ Scan Docker images with **Trivy** for security vulnerabilities and misconfigurations.  
   ✅ Block the pipeline if critical vulnerabilities are detected.

6. **`updatek8s`**  
   ✅ Update Kubernetes deployment manifests (e.g., new Docker image tag).  

7. **Argo CD GitOps Sync**  
   ✅ Argo CD automatically syncs the updated Kubernetes manifests from GitHub.  
   ✅ Triggers rolling updates in the EKS cluster, ensuring zero downtime deployment.

---

📌 **CI/CD Pipeline Screenshots**  
- [GitHub Actions Workflow Run](./assets/github-actions-workflow.png)  
- [SonarQube Code Quality Report](./assets/sonarqube-report.png)  
- [GolangCI-Lint Code Check](./assets/golangci-lint.png)  
- [Docker Image Build & Push](./assets/docker-image-push.png)  
- [Trivy Docker Image Scan Results](./assets/trivy-scan-results.png)  
- [Kubernetes Manifest Update](./assets/k8s-manifest-update.png)  
- [Argo CD Sync Operation](./assets/argo-cd-sync.png)  
- [Rolling Update in Progress](./assets/rolling-update.png)

---

## 🛠️ Tech Stack

| Category              | Tools & Technologies        |
|-----------------------|-----------------------------|
| ☁️ Cloud Provider     | AWS                         |
| 🚢 Orchestration      | Kubernetes (EKS)            |
| ⚙️ Infrastructure     | Terraform                   |
| 🔄 CI/CD              | GitHub Actions, Argo CD     |
| 🐳 Containers         | Docker                      |
| 🔐 Vulnerability Scan | Trivy                       |
| ✅ Code Quality       | SonarQube, GolangCI-Lint    |
| 🌐 DNS/Domain         | AWS Route 53                |
| 📦 Artifact Registry  | DockerHub                   |

---

## 🌟 Project Highlights

✅ Designed and deployed a **highly available microservices-based application** on AWS EKS  
✅ Developed **infrastructure automation** using Terraform  
✅ Implemented **GitOps workflows** with Argo CD for automated deployments  
✅ Automated **CI/CD pipelines** with GitHub Actions, covering the entire build-to-deploy lifecycle  
✅ Integrated **code quality checks**, **security scans**, and **linting tools**  
✅ Configured **custom domain and DNS routing** using AWS Route 53  

---

## 📸 Screenshots & Demo Videos

Screenshots and video assets are available in the `/assets` folder (or as per your repo structure):  
🖼️ **Infrastructure Setup**  
🖼️ **CI/CD Pipelines**  
🖼️ **DNS/Route 53 Configuration**  
📹 **Video Walkthroughs**

---

## 🙏 Thank You!

---
