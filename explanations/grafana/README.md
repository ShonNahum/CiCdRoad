# 📊 Grafana in My DevOps CI/CD Project

## 📌 Why I Use Grafana

**Grafana** is the central dashboarding and observability tool in my DevOps. It provides a unified view of **logs**, **metrics**, and **traces**, and here's why it's essential in my setup:

- 🧩 Native support for multiple data sources like **Prometheus** (metrics), **Loki** (logs), and **Jaeger** (traces).
- 🔍 Powerful querying with **PromQL** for metrics, **LogQL** for logs, and trace visualization with **Jaeger** integration.
- 🧠 Combines logs, metrics, and traces in a single interface for deep troubleshooting and full-stack visibility.
- 📊 Custom dashboards for applications, infrastructure, CI/CD tools, and distributed tracing.
- 🌐 Built to work seamlessly with cloud-native environments like Kubernetes and K3s.

---

## 🛠️ How Grafana Fits Into My Workflow

![Grafana Architecture Diagram](/images/grafana.png)

### 🔸 Metrics (via Prometheus)

- **Prometheus** scrapes metrics from:
  - Application Exporters
  - Custom applications (e.g., SM, SMC)
- Grafana pulls this data from Prometheus and visualizes it through dashboards.

### 🔹 Logs (via Loki)

- Applications (SM, SMC) push structured logs directly to **Loki** using the `/loki/api/v1/push` endpoint.
- Logs include labels like info, warning, error for filtering.
- Grafana queries logs from Loki with **LogQL** for searching and troubleshooting.

### 🔸 Traces (via Jaeger)

- Distributed tracing is enabled through **Jaeger**, collecting traces from my microservices and applications.
- Grafana connects to Jaeger to visualize traces, enabling root cause analysis by correlating traces with logs and metrics.
- This gives me end-to-end visibility of requests as they flow through the system.

---

## 🧠 Benefits of Using Grafana with Prometheus, Loki, and Jaeger

By combining all three observability pillars in Grafana, I get:

- ✅ Real-time system and application monitoring through metrics
- ✅ Centralized log collection and efficient search
- ✅ Distributed tracing for detailed request flow and latency analysis
- ✅ Unified dashboards for infrastructure, CI/CD, and full-stack observability
- ✅ Faster debugging by correlating metrics, logs, and traces seamlessly

Grafana acts as a single pane of glass for my entire DevOps observability stack, delivering complete visibility and faster troubleshooting.

---

## 📊 My Grafana Dashboards

---

![Grafana docker dashboard Diagram](/images/grafana_docker.png)  
===  
![Grafana github dashboard Diagram](/images/grafana_github.png)  
===  
![Grafana jenkins dashboard Diagram](/images/grafana_jenkins.png)  
===  
![Grafana logs dashboard Diagram](/images/grafana_logs.png)  
===  
![Grafana prometheus dashboard Diagram](/images/grafana_prometheus.png)  
===  
![Grafana argoCD dashboard Diagram](/images/grafana_argocd.png)  
===  
![Grafana traces dashboard Diagram](/images/grafana_trace.png)

---
