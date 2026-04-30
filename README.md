# ☸️ Kubernetes Learnings — Zero to Production

> A comprehensive Kubernetes learning and project repository covering everything from core concepts to advanced production-grade deployments with monitoring, based on the **TrainWithShubham** full-length Kubernetes tutorial.

---

## 📁 Repository Structure

```
helm-monitoring/
├── apache/              # Apache web server K8s manifests
├── crd/                 # Custom Resource Definitions
├── dashboard/           # Kubernetes Dashboard manifests
├── django-notes-app/    # Django Notes App (3-tier project)
├── montioring/          # Prometheus & Grafana monitoring stack
├── mysql/               # MySQL database K8s manifests
└── nginx/               # Nginx ingress / web server manifests
```

---

## 🎯 What This Repository Covers

This repo is a hands-on companion to the complete Kubernetes tutorial by **TrainWithShubham**, taking you from Kubernetes fundamentals all the way to production-ready deployments.

---

## 📚 Learning Path

### 🏗️ Foundations & Architecture
![Beginner](https://img.shields.io/badge/Level-Beginner-green)

| Icon | Topic | Description |
|------|-------|-------------|
| 📜 | History of Kubernetes | Understand how K8s was born from Google's Borg and why it became the container orchestration standard |
| 🔄 | Monolithic → Microservices | Learn the architectural shift that made Kubernetes essential for modern software delivery |
| 🧠 | Kubernetes Architecture & kubectl | Explore control plane components (API server, etcd, scheduler) and how to interact with the cluster via kubectl |

**Key Concepts:** `Control Plane` → `Worker Nodes` → `etcd` → `kubectl` → `API Server`

---

### 🖥️ Cluster Setup
![Beginner](https://img.shields.io/badge/Level-Beginner-green)

| Icon | Cluster Type | Description |
|------|-------------|-------------|
| 🐳 | KIND (Kubernetes in Docker) | Spin up a lightweight multi-node cluster inside Docker containers — great for local CI/CD testing |
| 🚀 | Minikube | Run a single-node K8s cluster on your local machine with minimal setup |
| 🔩 | Kubeadm | Bootstrap a production-like multi-node cluster manually on bare-metal or VMs |

**Key Concepts:** `KIND` → `Minikube` → `Kubeadm` → `kubeconfig` → `cluster contexts`

---

### ⚙️ Core Workloads
![Intermediate](https://img.shields.io/badge/Level-Intermediate-yellow)

| Icon | Object | Description |
|------|--------|-------------|
| 📦 | Namespaces | Logically isolate resources within a cluster for multi-team or multi-env setups |
| 🟢 | Pods | The smallest deployable unit — runs one or more containers sharing network and storage |
| 🚢 | Deployments | Declaratively manage stateless app rollouts, rollbacks, and updates |
| 🔁 | ReplicaSets | Ensure a desired number of identical pod replicas are always running |
| 👾 | DaemonSets | Run exactly one pod per node — ideal for log collectors and monitoring agents |
| ⏱️ | Jobs | Run a task to completion once, useful for batch processing and migrations |
| 🕐 | CronJobs | Schedule recurring Jobs on a cron-like timetable |

**Key Concepts:** `Pods` → `ReplicaSets` → `Deployments` → `DaemonSets` → `Jobs` → `CronJobs`

---

### 💾 Storage & Networking
![Intermediate](https://img.shields.io/badge/Level-Intermediate-yellow)

| Icon | Topic | Description |
|------|-------|-------------|
| 🗄️ | StorageClasses, PV & PVC | Dynamically provision and claim persistent storage for stateful applications |
| 🌐 | Services | Expose pods internally or externally using ClusterIP, NodePort, and LoadBalancer types |
| 🔀 | Ingress Controllers | Route external HTTP/HTTPS traffic to services using rules and host/path-based routing |

**Key Concepts:** `PersistentVolume` → `PVC` → `StorageClass` → `ClusterIP` → `NodePort` → `Ingress`

---

### 🔧 Advanced Configuration & Scaling
![Advanced](https://img.shields.io/badge/Level-Advanced-red)

| Icon | Topic | Description |
|------|-------|-------------|
| 🗂️ | ConfigMaps | Decouple environment-specific configuration from container images |
| 🔒 | Secrets | Securely store and inject sensitive data like passwords, tokens, and keys |
| 📊 | Resource Quotas | Cap CPU/memory usage per namespace to prevent resource starvation |
| 🩺 | Probes (Liveness / Readiness) | Let Kubernetes self-heal and traffic-route based on real app health signals |
| 🚫 | Taints & Tolerations | Control which pods can be scheduled on which nodes for isolation and priority |
| 📈 | Horizontal Pod Autoscaler (HPA) | Automatically scale pod count up/down based on CPU or custom metrics |
| 📐 | Vertical Pod Autoscaler (VPA) | Automatically right-size CPU/memory requests and limits for running pods |

**Key Concepts:** `ConfigMaps` → `Secrets` → `ResourceQuota` → `Probes` → `Taints` → `HPA` → `VPA`

---

### 🔐 Security & Advanced Concepts
![Advanced](https://img.shields.io/badge/Level-Advanced-red)

| Icon | Topic | Description |
|------|-------|-------------|
| 🛡️ | RBAC | Define fine-grained permissions for users and service accounts using Roles and RoleBindings |
| 🧩 | Custom Resource Definitions (CRDs) | Extend the Kubernetes API with your own resource types and controllers |
| ⛵ | Helm & Operators | Package, version, and deploy complex K8s applications using Helm charts and Operators |
| 🪆 | SideCar & Init Containers | Run helper containers alongside or before the main app container for setup and proxying |

**Key Concepts:** `RBAC` → `ServiceAccounts` → `CRDs` → `Helm Charts` → `Operators` → `SideCar` → `Init Containers`

---

## 🚀 Hands-On Projects

### Project 1 — 3-Tier Chat Application on Minikube
![Intermediate](https://img.shields.io/badge/Level-Intermediate-yellow)

A full-stack 3-tier chat application deployed locally on a **Minikube** cluster. Demonstrates service communication, deployments, and persistent storage across frontend, backend, and database layers.

### Project 2 — .Net/Python 3-Tier App with Monitoring (KIND + Prometheus + Grafana)
![Advanced](https://img.shields.io/badge/Level-Advanced-red)

A production-style deployment on a **KIND** cluster featuring:
- .Net / Python 3-tier application
- **Prometheus** for metrics collection (see `montioring/`)
- **Grafana** dashboards for visualization
- Helm-based deployment workflow

---

## 🛠️ Prerequisites

- Docker
- kubectl
- KIND / Minikube / kubeadm (depending on the section)
- Helm 3.x
- Basic Linux/CLI familiarity

---

## 🚦 Getting Started

```bash
# Clone the repository
git clone https://github.com/<your-username>/kubernetes-learnings.git
cd kubernetes-learnings

# Apply a manifest (example: nginx)
kubectl apply -f nginx/

# Deploy the monitoring stack
kubectl apply -f montioring/
```

---

## 📖 Tutorial Reference

This repository was built alongside the **TrainWithShubham** Kubernetes Zero to Production tutorial — a comprehensive guide blending theory with hands-on practice across multiple cluster types.

---

## 🤝 Contributing

Pull requests are welcome! If you find issues or want to add improvements, feel free to open an issue or submit a PR.

---

## 📝 License

This project is open-source and available under the [MIT License](LICENSE).
