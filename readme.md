# Kubernetes Manifest Collection 🚀

This repository contains a comprehensive set of Kubernetes manifest files designed to help you learn, experiment, and master Kubernetes core concepts through real-world examples and hands-on mini projects.

---

## 📁 Repository Structure
1. Pods and replicaset/ # Basic pod definitions and ReplicaSet usage

2. Scaling_Deployment_Rollbacks/ # Deployments, scaling techniques, and rollback scenarios

3. Services_Namespaces/ # Cluster networking, service types, and namespaces
4.1 Mini Project with Pods/ # A mini project demonstrating pod usage in isolation
4.2 Mini Project with Deployments/ # Deployment-based mini project

5. Resource requests and Limits/ # Defining CPU and memory limits for containers

6. Ingress/ # Ingress controllers and routing configuration

7. Kubernetes Volumes/ # Volume types: emptyDir, hostPath, configMap, secret, etc.

8. Statefulset/ # Managing stateful applications with StatefulSets

9. HPA/ # Horizontal Pod Autoscaling configurations

10. DaemonSets/ # Running pods on all (or some) nodes using DaemonSets

11. Helm Charts/ # Helm-based deployment management

12. Advance Scheduling Mechanism/ # Taints, tolerations, affinities, and node selectors

## 🧩 Usage

1. **Clone the repository**
   ```bash
   git clone https://github.com/<your-username>/<your-repo-name>.git
   cd <your-repo-name>
2. **Apply a manifest file**
   ```bash
   kubectl apply -f <path-to-yaml>
3. **Explore by folder**
   Navigate to any topic folder and explore different manifest examples related to that concept.

## 🛠️ Prerequisites
   Kubernetes cluster (e.g., Minikube, Kind, EKS, GKE)
   kubectl CLI installed
   (Optional) helm for chart-based deployments

## 📌 Notes
   All YAML files are tested on Kubernetes v1.27+
   Recommended to explore in order for a structured learning experience
   Real-world examples included to build confidence in production setups

   Local change
