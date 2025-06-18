# K3s Usage in My DevOps CI/CD Project

## 📌 Why I'm Using K3s

I chose K3s because it is a k8s lightweight, easy-to-install Kubernetes distribution designed for production workloads in resource-constrained environments:

- ✅ K3s provides a fully compliant Kubernetes cluster with minimal resource requirements.
- 🔧 It simplifies Kubernetes setup and management, making it ideal for edge, IoT, and small-scale environments.
- 🌍 K3s has strong community support and is widely adopted for lightweight Kubernetes deployments.
- 🛠️ It supports all standard Kubernetes features, enabling seamless integration with tools like ArgoCD and Jenkins.
- 🔄 K3s works well in both single-node and multi-node cluster configurations, offering flexibility and scalability.
- 🧠 It includes built-in components like a container runtime, networking, and storage to reduce complexity.
- 📚 Has extensive documentation and a simple installation process.

---

## 🛠️ How I'm Using K3s

The diagram below shows how K3s fits into my DevOps pipeline alongside ArgoCD:

![Architecture Diagram](/images/argocd_deploy.png)

### 🔄 Workflow Explanation

- ArgoCD continuously monitors the GitHub chart repository for changes  
- When it detects updates, ArgoCD pulls the latest manifests or Helm charts into its control plane.
- It compares the desired state from Git with the current state in the k3s cluster.
- ArgoCD then automatically applies any necessary changes to the K3s cluster to keep it in sync with Git.

---

This setup forms the foundation of my CI/CD pipeline and represents the deployment stage in my overall DevOps automation process.
