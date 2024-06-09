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
| **Kibana** | Log visualization   | 
| **Prometheus** | Metrics collection   | 
| **Prometheus Exporters** | Collecting metrics from various sources   | 
| **Grafana** | Metrics visualization   | 
| **Prometheus Alertmanager** | Alerting and notifications   | 
| **Notification Channels** | Email, Slack, etc.   | 


| **** | **** | **** | 
| :---   | :--- |  :--- | 
| **Collecting and Centralizing Logs** | Log Collection  |Use Fluentd as a logging agent on each Kubernetes node to collect logs from all containers   | 
| ^  |   |   | 
| ^  |   |   | 
| **Fluentd** | Agents on each node for log collection   | 
| **Elasticsearch** | Centralized log storage   | 
| **Kibana** | Log visualization   | 
| **Prometheus** | Metrics collection   | 
| **Prometheus Exporters** | Collecting metrics from various sources   | 
| **Grafana** | Metrics visualization   | 
| **Prometheus Alertmanager** | Alerting and notifications   | 
| **Notification Channels** | Email, Slack, etc.   | 

<table>
  <tr>
    <th>Stage </th>
    <th>Stage Specifics</th>
    <th>Description</th>
  </tr>
  <tr>
    <td rowspan="3">Collecting and Centralizing Logs</td>
    <td>Log Collection</td>
    <td>Use Fluentd as a logging agent on each Kubernetes node to collect logs from all containers</td>
  </tr>
  <tr>
    <td>Log Aggregation</td>
    <td>Forward the collected logs to a centralized log storage system, such as Elasticsearch</td>
  </tr>
  <tr>
    <td>Log Visualization</td>
    <td>Use Kibana to visualize and analyze the logs stored in Elasticsearch</td>
  </tr>
  <tr>
    <td rowspan="3">Setting Up Alerts and Notifications Logs</td>
    <td>Alerting System</td>
    <td>Integrate Prometheus Alertmanager for alerting</td>
  </tr>
  <tr>
    <td>Alert Rules</td>
    <td>Define alerting rules in Prometheus based on metrics and logs</td>
  </tr>
  <tr>
    <td>Notification Channels</td>
    <td>Configure Alertmanager to send notifications via email, Slack, or other messaging services</td>
  </tr>
  <tr>
    <td rowspan="4">Monitoring Key Performance Metrics</td>
    <td>Metrics Collection</td>
    <td>Use Prometheus to collect metrics from Kubernetes nodes, pods, and services</td>
  </tr>
  <tr>
    <td>Metrics Exporters</td>
    <td>Deploy various Prometheus exporters (e.g., node_exporter, kube-state-metrics) to gather metrics from different sources</td>
  </tr>
  <tr>
    <td>Metrics Storage and Querying</td>
    <td>Store metrics in Prometheus and use Grafana for querying and visualization</td>
  </tr>
  <tr>
    <td>Dashboards</td>
    <td>Set up Grafana dashboards to monitor key performance metrics such as CPU, memory usage, request latency, and error rates</td>
  </tr>

</table
