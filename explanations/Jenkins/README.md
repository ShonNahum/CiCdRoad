# 🚀 Jenkins Usage in My DevOps CI/CD Project

## 📌 Why I'm Using Jenkins

GitHub is my chosen Source Control Management (SCM) platform for the following reasons:

- ✅ **Powerful SCM**: Reliable and feature-rich source control platform.
- 🔧 **CI/CD Integrations**: Seamless integration with Jenkins, GitHub Actions, ArgoCD, and other DevOps tools.
- 🌍 **Vast Community**: Backed by a large open-source community and widely adopted in the industry.
- 🧩 **Tool Compatibility**: Most DevOps tools and learning resources assume GitHub integration by default.
- 🧠 **Versioning & History**: Tracks full commit history and allows easy rollback.
- 📚 **User-Friendly**: Simple UI and extensive documentation.
- 💸 **Free Tier**: Supports unlimited public and private repositories at no cost.

---

## 🛠️ How Jenkins Fits into My DevOps Workflow

### 🔭 High-Level Architecture

![High-Level Architecture Diagram](/images/HL_Jenkins.png)

At a high level, Jenkins acts as the CI orchestrator.

---

### 📦 Current Pipelines

I currently manage two pipelines:

---

### 1️⃣ ImageComposer Pipeline

![ImageComposer Pipeline Diagram](/images/image_composer.png)

**🔄 Workflow Explanation:**
- Accepts `REPO`, `BRANCH`, and `TAG` as input parameters.
- Builds a Docker image from the specified repo and branch.
- Pushes the image to a Docker registry (e.g., DockerHub or Artifactory).

---

### 2️⃣ Pylint Pipeline

![Pylint Pipeline Diagram](/images/pylint.png)

**🔄 Workflow Explanation:**
- Triggered by a code push to GitHub.
- Jenkins runs `pylint` on the entire repository.
- If `pylint` passes without critical issues, a **Pull Request to `main`** is created.
- If it fails, the build is marked as failed and no PR is opened.

---

## ✅ Summary

This setup represents the foundation of my CI process:

- GitHub handles version control.
- Jenkins automates testing, linting, and Docker image delivery.

---
