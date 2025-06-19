# 📊 Prometheus in My DevOps CI/CD Project

## 📌 Why Prometheus?

I use **Prometheus** as my primary monitoring tool because:

- 📈 Prometheus is one of the most widely adopted monitoring tools in the cloud-native world, used by major companies like Red Hat, SoundCloud, Weaveworks, and more.
- 🤝 It's part of the Cloud Native Computing Foundation (CNCF) — alongside Kubernetes, ArgoCD, and others.
- 📦 It collects **metrics** from applications, services, exporters, and Kubernetes itself.
- 🧩 It supports integrations with **Grafana** for advanced dashboards and visualizations.
- 🔄 Its **pull-based** architecture fits perfectly with dynamic environments like K3s.

---

## 🛠️ How Prometheus Fits in My CI/CD Flow

![Architecture Diagram](/images/prometheus.png)

### 🔁 Workflow Summary

- **Prometheus** scrapes metrics from services (e.g., GitHub Exporter,ArgoCD, MongoDB Exporter,SM Application,SMC Application,Jenkins).
- Metrics from applications and infrastructure are collected and stored in **time-series** format.

---

## 🧠 Summary

Prometheus gives me full observability over my DevOps , helping me:

- Monitor application health
- Track CI/CD performance
- Diagnose issues quickly

This makes it an essential part of my production-grade CI/CD automation.
