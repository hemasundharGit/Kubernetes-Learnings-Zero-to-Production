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

## 📚 Learning Path & Timestamps

### 🏗️ Foundations & Architecture
| Topic | Timestamp |
|---|---|
| History of Kubernetes | 03:05 |
| Monolithic → Microservices shift | 06:20 |
| Kubernetes Architecture & kubectl | 10:12 |

### 🖥️ Cluster Setup
| Cluster Type | Timestamp |
|---|---|
| KIND (Kubernetes in Docker) | 35:25 |
| Minikube | 57:20 |
| Kubeadm | 01:04:02 |

### ⚙️ Core Workloads
| Object | Timestamp |
|---|---|
| Namespaces | 01:20:11 |
| Pods | 01:35:22 |
| Deployments | 01:44:00 |
| ReplicaSets | 02:04:34 |
| DaemonSets | 02:06:48 |
| Jobs | 02:12:15 |
| CronJobs | 02:21:10 |

### 💾 Storage & Networking
| Topic | Timestamp |
|---|---|
| StorageClasses, PV & PVC | 02:39:20 |
| Services | 03:04:05 |
| Ingress Controllers | 03:24:30 |

### 🔧 Advanced Configuration & Scaling
| Topic | Timestamp |
|---|---|
| ConfigMaps | 04:11:10 |
| Secrets | 04:18:00 |
| Resource Quotas | 04:32:30 |
| Probes (Liveness / Readiness) | 04:40:45 |
| Taints & Tolerations | 04:48:55 |
| Horizontal Pod Autoscaler (HPA) | 04:59:30 |
| Vertical Pod Autoscaler (VPA) | 05:50:45 |

### 🔐 Security & Advanced Concepts
| Topic | Timestamp |
|---|---|
| RBAC (Role-Based Access Control) | 06:11:55 |
| Custom Resource Definitions (CRDs) | 07:13:55 |
| Helm & Operators | 07:36:55 |
| SideCar & Init Containers | 08:13:20 |

---

## 🚀 Hands-On Projects

### Project 1 — 3-Tier Chat Application on Minikube
**Timestamp:** `09:09:40`

A full-stack 3-tier chat application deployed locally on a **Minikube** cluster. Demonstrates service communication, deployments, and persistent storage across frontend, backend, and database layers.

### Project 2 — .Net/Python 3-Tier App with Monitoring (KIND + Prometheus + Grafana)
**Timestamp:** `10:25:15`

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
