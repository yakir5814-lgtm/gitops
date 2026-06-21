# GitOps Final Project - Automated Deployment

This project demonstrates a fully automated CI/CD pipeline built with GitOps principles.

## 🛠 Tech Stack
* **Kubernetes (Minikube):** The application runtime environment.
* **Jenkins:** Handles the CI process (building the Docker image and pushing it to Docker Hub).
* **Argo CD:** Manages the CD process (automatically synchronizing Kubernetes configurations from Git to the cluster).
* **Docker:** Containerization for the application.

## 🚀 How it works
1. **CI Pipeline:** Upon any code change, Jenkins builds a new Docker image and updates the version tag on Docker Hub.
2. **Git Update:** The pipeline automatically updates the `nginx-deployment.yaml` file in this repository with the latest image version.
3. **Continuous Deployment:** Argo CD detects the change in Git and immediately synchronizes the cluster, performing a rolling update to the pods.

## 📂 Directory Structure
* `/apps`: Contains the Kubernetes deployment and service configurations.
* `application.yaml`: The Argo CD Application definition that connects this repository to the cluster.

## 📊 System Status
The system is set to **Healthy** and is automatically synchronized with the Kubernetes cluster via Argo CD (Auto-sync enabled).

---
*Built with love for the Final Project.*
