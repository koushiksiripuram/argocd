# 🚀 GitOps Deployment using ArgoCD

## 📌 Overview
This project demonstrates implementing GitOps-based continuous deployment using ArgoCD on Kubernetes.

ArgoCD automates application deployment by syncing Kubernetes cluster state with a Git repository, ensuring consistency and reliability.

---

## 🛠 Tech Stack
- Kubernetes
- ArgoCD
- Docker
- Git
- YAML

---

## ⚙️ Features
- GitOps-based deployment workflow
- Automated sync between Git and Kubernetes cluster
- Declarative infrastructure using YAML manifests
- Continuous deployment without manual intervention

---

## 🧪 Architecture / Workflow

1. Application configuration stored in Git repository  
2. ArgoCD monitors the repository  
3. Any change in Git triggers deployment  
4. Kubernetes cluster automatically syncs desired state  
5. Ensures consistency between code and running system  

---

## 🔄 GitOps Flow

Git Commit → ArgoCD Sync → Kubernetes Deployment → Application Updated

---

## ▶️ Setup & Run

### Prerequisites
- Kubernetes cluster (Minikube / EKS)
- kubectl installed
- ArgoCD installed

### Steps

```bash
# Install ArgoCD
kubectl create namespace argocd

# Apply ArgoCD manifests
kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml

# Access ArgoCD UI
kubectl port-forward svc/argocd-server -n argocd 8080:443
