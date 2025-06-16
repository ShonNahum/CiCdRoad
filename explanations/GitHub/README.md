# GitHub Usage in My DevOps CI/CD Project

## 📌 Why I'm Using GitHub

There are several reasons why I chose GitHub as my Source Control Management (SCM) platform:

- ✅ GitHub is a powerful and reliable tool for SCM (Source Control Management).
- 🔧 It provides robust CI/CD integrations with tools like Jenkins, GitHub Actions, and ArgoCD.
- 🌍 It has a huge open-source community and is one of the most widely adopted platforms in the DevOps world.
- 🧩 Most DevOps tools and tutorials (e.g., ArgoCD, Jenkins) assume GitHub as the default integration.
- 🧠 GitHub stores all versions of my code, providing complete version history and easy rollback capabilities.
- 📚 It’s user-friendly, with great documentation and a simple UI.
- 💸 Offers a generous free tier with unlimited public and private repositories.

---

## 🛠️ How I'm Using GitHub

Below is the architecture showing how GitHub fits into my DevOps workflow:

![Architecture Diagram](/images/dev_to_github.png)

### 🔄 Workflow Explanation

- A developer **pushes code** to a GitHub repository.
- That push **triggers a webhook** configured in GitHub.
- The webhook notifies **Jenkins**, which starts a CI/CD pipeline automatically.
- Jenkins then handles the **build, test, and deployment** stages as configured.

---

This setup is the foundation of my CI/CD pipeline and forms the first step in building a full DevOps automation process.
