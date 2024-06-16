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


![image](https://github.com/jaekimandy/K8s_Monitoring-Logging/assets/99704906/367fd535-a951-400b-a87e-bd24fd3b0461)
 
<a href="https://medium.com/avmconsulting-blog/prometheus-monitoring-with-elastic-stack-in-kubernetes-5cf0aaa7ce04">Reference Architecture</a>


# Fluentd vs Prometheus: What are the differences?  
**Introduction**: Fluentd and Prometheus are both popular open-source data collection and monitoring tools used in the field of DevOps. Although they serve similar purposes, there are some key differences between these two tools.  

**Data Collection Approach**: Fluentd is a log collector and aggregator that operates on logs in real-time. It collects logs from various sources, transforms them, and sends them to various destinations for further processing. On the other hand, Prometheus is a time-series database and monitoring system that is primarily used for monitoring and alerting. It collects metrics data from configured targets periodically and stores it for analysis and visualization.  

**Data Types**: Fluentd is more oriented towards collecting and processing unstructured log data. It accepts logs in various formats such as text, JSON, and others. Prometheus, on the other hand, focuses on collecting and analyzing numeric time-series data. It is designed to monitor and analyze metrics related to system performance, resource utilization, and application behavior.   

**Query Language**: Fluentd uses its own query language called Fluent Query Language (FLQL). It allows users to filter and manipulate log data using a SQL-like syntax. Prometheus, on the other hand, uses Prometheus Query Language (PromQL) for querying and analyzing time-series data. PromQL provides a powerful set of operators and functions specifically tailored for time-series analysis.   

**Monitoring Architecture**: Fluentd follows a centralized architecture where logs are collected from various sources and sent to a centralized server for processing and analysis. It provides a unified view of logs across the system. In contrast, Prometheus follows a decentralized architecture where it scrapes metrics data directly from configured targets at regular intervals. Each target maintains its own metrics data, and Prometheus queries these targets individually.   

**Alerting and Monitoring Capabilities**: Fluentd focuses on log aggregation and routing, and does not have built-in support for alerting and monitoring. Prometheus, on the other hand, has powerful alerting and monitoring capabilities. It allows users to define alert rules based on metric conditions and send alerts to various notification channels. It also provides a flexible dashboard for visualizing and analyzing metrics data.   

**Integration with Ecosystem**: Fluentd is highly extensible and can be integrated with various other tools, services, and platforms. It provides plugins for different log sources and destinations, allowing seamless integration with existing infrastructure. Prometheus also has a wide range of integrations with different systems and frameworks. It provides exporters for collecting metrics from various sources and supports integrations with popular monitoring and visualization tools.   

**In Summary, Fluentd is a log collector and aggregator that operates on unstructured log data, while Prometheus is a monitoring system that specializes in time-series data analysis and alerting. Fluentd uses FLQL for log querying, follows a centralized architecture, and does not have built-in monitoring capabilities. Prometheus uses PromQL for time-series analysis, follows a decentralized architecture, and provides powerful monitoring and alerting features. Both tools have extensive integrations with different systems and can be used together to create a comprehensive monitoring solution.

## FluentD logged in ElasticSearch shown through Kibana
![image](https://github.com/jaekimandy/K8s_Monitoring-Logging/assets/99704906/1ef71a1b-9c19-43c9-a7f3-eeff96bfc812)

![image](https://github.com/jaekimandy/K8s_Monitoring-Logging/assets/99704906/225246d1-738a-43bb-b12b-6ec251c73ae2)

## Prometheus Graphana Metrics
![image](https://github.com/jaekimandy/K8s_Monitoring-Logging/assets/99704906/8ba5c36d-b7f1-4770-bef2-f31a44bab4c5)

## Prometheus Aleart Rules
![image](https://github.com/jaekimandy/K8s_Monitoring-Logging/assets/99704906/f7eedcad-d5f7-4d7f-9d65-4529bcd00984)





