# ArgoCD Usage in My DevOps CI/CD Project

## 📌 Why I'm Using ArgoCD

I chose ArgoCD because it is a powerful GitOps continuous delivery tool that simplifies Kubernetes deployments:

- ✅ ArgoCD automates Kubernetes application deployment by syncing manifests directly from Git repositories.
- 🔧 It integrates smoothly with CI tools like Jenkins and fits well in modern GitOps workflows.
- 🌍 ArgoCD is widely adopted in the Kubernetes ecosystem with strong community support.
- 🛠️ It enables declarative infrastructure management and ensures your cluster state matches the desired state stored in Git.
- 🔄 Supports automated or manual sync modes, giving flexibility and control over deployments.
- 🧠 Provides real-time monitoring and rollback capabilities for Kubernetes applications.
- 📚 Has excellent documentation and an intuitive UI for managing application states.

---

## 🛠️ How I'm Using ArgoCD

The diagram below show how ArgoCD fits into my DevOps pipeline:

![Architecture Diagram](/images/argo_pull.png)

### 🔄 Workflow Explanation

- ArgoCD continuously monitors the GitHub chart repository for any changes.
- When new updates are detected, ArgoCD pulls the latest changes from the repository to its internal cache.

---

This setup is the foundation of my CI/CD pipeline and forms the 4th step in building a full DevOps automation process.
