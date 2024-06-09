# K8s_Monitoring-Logging

**Task 3: Monitoring and Logging**  
• Propose a monitoring and logging solution for a distributed system running on Kubernetes.  
• Explain how you would collect and centralize logs from multiple microservices.  
• Describe how you would set up alerts and notifications for critical issues.  
• Discuss your approach to monitoring key performance metrics and ensuring the system's health.  

![monitoring_logging_solution drawio](https://github.com/jaekimandy/K8s_Monitoring-Logging/assets/99704906/82323255-ac9e-4873-8f0b-0596f5f0b47d)


**Diagram Components**  

| **Infra** | **Description** | 
| :---   | :--- | 
| **Kubernetes Cluster** | Representing the distributed system   | 
| **Fluentd** | Agents on each node for log collection   | 
| **Elasticsearch** | Centralized log storage   | 
| **Kibana**: | Log visualization   | 
| **Prometheus** | Metrics collection   | 
| **Prometheus Exporters** | Collecting metrics from various sources   | 
| **Grafana** | Metrics visualization   | 
| **Prometheus Alertmanager** | Alerting and notifications   | 
| **Notification Channels** | Email, Slack, etc.   | 
