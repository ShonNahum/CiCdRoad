# 🚀 Jenkins Usage in My DevOps CI/CD Project

## 🤖 Why I'm Using Jenkins

Jenkins is my chosen CI/CD automation server for the following reasons:

- ✅ **Open Source & Flexible**: Fully open-source and endlessly extensible with plugins.
- 🔧 **Plugin Ecosystem**: Thousands of plugins support integration with tools like Docker, GitHub, Slack, AWS, Kubernetes, and more.
- 🔁 **Pipeline as Code**: Allows defining build/test/deploy workflows in a versioned `Jenkinsfile`.
- 🌐 **Web-Based UI**: Provides a user-friendly interface to monitor jobs, logs, and build history.
- 📦 **Robust Job Scheduling**: Supports triggers from GitHub webhooks, cron, manual inputs, etc.
- 🧠 **Community & Documentation**: Strong community support and detailed documentation for fast problem-solving.

---

## 🛠️ How Jenkins Fits into My DevOps Workflow

Jenkins acts as the automation backbone in my CI/CD pipeline. It connects my source code (from GitHub) to all the build, test, and deployment actions required in my workflow.

### 🔗 OverAll Integration Flow:
- Developers push code to GitHub.
- A GitHub **webhook** triggers Jenkins.
- Jenkins checks out the code, runs **linting** and **Docker builds**.
- images are pushed to a container registry (e.g., DockerHub or Artifactory).

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
