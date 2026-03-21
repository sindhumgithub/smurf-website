# 🚀 Smurfit - Mini Project

## 📌 Overview
Smurf & Go is a DevOps-driven web application project that demonstrates the end-to-end implementation of modern deployment practices. The project focuses on containerizing a static web application using Docker, automating build and deployment pipelines with Jenkins, orchestrating containers using Kubernetes (Amazon EKS), and provisioning cloud infrastructure through Terraform.

It showcases how different DevOps tools integrate seamlessly to enable continuous integration and continuous deployment (CI/CD), ensuring scalability, reliability, and automation in application delivery.

---

## 🛠 Tech Stack

- Terraform
- AWS (or your cloud provider)
- Git & GitHub
- Docker
- Jenkins
- Kubernetes
- App Code

---

## 📂 Project Structure
Terraform/
│
├── eks.tf # To create EKS cluster
├── provider.tf # Provider configuration
├── variables.tf # Input variables
├── outputs.tf # Output values
├── vpc.tf # VPC Resource creation
└── README.md # Project documentation


---

## 🚀 How to Use This Project

### 🐳 Docker Setup

Build Docker image:

```bash
docker build -t ${DOCKERHUB_USER}/${IMAGE_NAME}:latest app/
echo $PASS | docker login -u $USER --password-stdin
docker push ${DOCKERHUB_USER}/${IMAGE_NAME}:latest

---
⚙️ Jenkins Pipeline
Pipeline stages:
Checkout code from GitHub
Build Docker image
Push image to DockerHub
Deploy to Kubernetes
---

☸️ Deploy to Kubernetes
kubectl apply -f k8s/deployment.yaml
kubectl apply -f k8s/service.yaml
---

🌐 Terraform (EKS Setup)
terraform init
terraform apply
---

🐳 Docker Setup
docker build -t smurf-go .
---

🔗 Application Access
smurfit.web.app
