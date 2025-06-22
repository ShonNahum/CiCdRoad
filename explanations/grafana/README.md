# 📊 Grafana in My DevOps CI/CD Project

## 📌 Why I Use Grafana

**Grafana** is the central dashboarding and observability tool in my DevOps. It provides a unified view of both **logs** and **metrics**, and here's why it's essential in my setup:

- 🧩 Native support for multiple data sources like **Prometheus** (metrics) and **Loki** (logs).
- 🔍 Powerful querying with **PromQL** for metrics and **LogQL** for logs.
- 🧠 Combines logs and metrics in a single interface for deep troubleshooting and visibility.
- 📊 Custom dashboards for applications, infrastructure, and CI/CD tools.
- 🌐 Built to work with cloud-native environments like Kubernetes and K3s.

---

## 🛠️ How Grafana Fits Into My Workflow

![Grafana Architecture Diagram](/images/grafana.png)

### 🔸 Metrics (via Prometheus)

- **Prometheus** scrapes metrics from:
  - Application Exporters
  - My custom applications (e.g., SM, SMC)
- Grafana pulls this data from Prometheus and visualizes it through dashboards.

### 🔹 Logs (via Loki)

- My applications (SM, SMC) push structured logs directly to **Loki** using the `/loki/api/v1/push` endpoint.
- Each log entry includes labels info,warning,error for filtering.
- Grafana queries logs from Loki using **LogQL** for searching and troubleshooting.

---

## 🧠 Benefits of Using Grafana

With Grafana connected to both Prometheus and Loki, I get:

- ✅ Real-time system and application monitoring
- ✅ Centralized log collection and search
- ✅ Unified dashboards for everything from infrastructure to CI/CD
- ✅ Faster debugging by correlating metrics with logs

Grafana is the single pane of glass for my entire observability stack, giving me complete visibility into logs and metrics across my DevOps environment.

## 📊 My Grafana Dashboards
---

![Grafana Architecture Diagram](images/grafana_docker.png)
![Grafana Architecture Diagram](images/grafana_github.png)
![Grafana Architecture Diagram](images/grafana_jenkins.png)
![Grafana Architecture Diagram](images/grafana_logs.png)
![Grafana Architecture Diagram](images/grafana_prometheus.png)

---