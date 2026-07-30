# End-to-End CI/CD Pipeline for Java Spring Boot Application using Jenkins, Docker, SonarQube, Prometheus & Grafana

## Project Overview

This project demonstrates an end-to-end Continuous Integration and Continuous Deployment (CI/CD) pipeline for a Java Spring Boot application. The pipeline automates the software delivery lifecycle—from source code integration to deployment—using modern DevOps tools and best practices.

In addition to CI/CD automation, the project includes a complete monitoring solution using Spring Boot Actuator, Prometheus, and Grafana to collect and visualize application metrics in real time.

---

# Key Features

* Automated GitHub source code checkout
* Maven build and dependency management
* Automated unit testing
* SonarQube static code analysis
* Docker image creation
* Automatic container replacement
* AWS EC2 deployment
* Spring Boot Actuator integration
* Prometheus metrics collection
* Grafana dashboards for monitoring
* Fully automated Jenkins pipeline
* Continuous code quality and application monitoring

---

# Technology Stack

| Category             | Technology    |
| -------------------- | ------------- |
| Programming Language | Java 21       |
| Framework            | Spring Boot 3 |
| Build Tool           | Maven         |
| Version Control      | Git & GitHub  |
| CI/CD                | Jenkins       |
| Code Quality         | SonarQube     |
| Containerization     | Docker        |
| Monitoring           | Prometheus    |
| Visualization        | Grafana       |
| Cloud Platform       | AWS EC2       |
| Operating System     | Ubuntu Linux  |

---

# Project Architecture

```text
                    GitHub Repository
                           │
                           ▼
                    Jenkins Pipeline
                           │
        ┌──────────────────┼──────────────────┐
        │                  │                  │
        ▼                  ▼                  ▼
   Maven Build      Unit Testing      SonarQube Analysis
                           │
                           ▼
                  Docker Image Build
                           │
                           ▼
             Stop Existing Container
                           │
                           ▼
            Deploy New Docker Container
                           │
                           ▼
              Spring Boot Application
                           │
                /actuator/prometheus
                           │
                           ▼
                     Prometheus Server
                           │
                           ▼
                    Grafana Dashboard
```

---

# CI/CD Pipeline Workflow

1. Checkout source code from GitHub.
2. Build the application using Maven.
3. Execute unit tests.
4. Perform static code analysis using SonarQube.
5. Package the application.
6. Build the Docker image.
7. Stop and remove the existing container.
8. Deploy the latest Docker container.
9. Expose Spring Boot Actuator metrics.
10. Prometheus scrapes the application metrics.
11. Grafana visualizes the collected metrics.

---

# Running the Application Locally

Clone the repository:

```bash
git clone https://github.com/<your-username>/java-demo.git
```

Navigate to the project directory:

```bash
cd java-demo
```

Build the project:

```bash
mvn clean package
```

Run the application:

```bash
java -jar target/java-demo-1.0.0.jar
```

Access the application:

```text
http://localhost:8081
```

Health Endpoint:

```text
http://localhost:8081/actuator/health
```

Prometheus Metrics Endpoint:

```text
http://localhost:8081/actuator/prometheus
```

---

# Docker Deployment

Build the Docker image:

```bash
docker build -t java-demo .
```

Run the Docker container:

```bash
docker run -d \
-p 8081:8081 \
--name java-demo-container \
java-demo
```

Verify the running container:

```bash
docker ps
```

---

# Monitoring Stack

The project uses Spring Boot Actuator, Micrometer, Prometheus, and Grafana to monitor the application.

## Monitoring Workflow

```text
Spring Boot Application
          │
          │ /actuator/prometheus
          ▼
     Prometheus
          │
          ▼
      Grafana
```

Start the monitoring services:

```bash
docker compose up -d
```

Verify the running containers:

```bash
docker ps
```

---

# Access Services

| Service                 | URL                            |
| ----------------------- | ------------------------------ |
| Spring Boot Application | http://localhost:8081          |
| Spring Boot Actuator    | http://localhost:8081/actuator |
| Prometheus              | http://localhost:9090          |
| Grafana                 | http://localhost:3000          |
| SonarQube               | http://localhost:9000          |

---

# Grafana

Default Login

```text
Username: admin
Password: admin
```

Recommended Dashboards

* Spring Boot Statistics (Dashboard ID: 11378)
* JVM Metrics
* Docker Container Metrics

---

# Prometheus Configuration

Prometheus scrapes metrics from the Spring Boot Actuator endpoint.

Example configuration:

```yaml
global:
  scrape_interval: 15s

scrape_configs:
  - job_name: spring-boot-app
    metrics_path: /actuator/prometheus
    static_configs:
      - targets:
          - java-demo-container:8081
```

---

# Jenkins Configuration

Configure the following before running the pipeline:

* JDK
* Maven
* Docker
* Jenkins Pipeline
* SonarQube Server
* GitHub Repository Integration

---

# SonarQube

Access the SonarQube dashboard:

```text
http://<EC2-Public-IP>:9000
```

Run code analysis:

```bash
mvn sonar:sonar
```

---

# Metrics Monitored

* JVM Memory Usage
* Heap Memory
* Non-Heap Memory
* CPU Usage
* HTTP Request Metrics
* Tomcat Session Metrics
* Active Threads
* Garbage Collection
* Process Uptime
* System Load

---

# Project Structure

```text
java-demo/
├── Dockerfile
├── docker-compose.yml
├── monitoring/
│   ├── prometheus/
│   │   └── prometheus.yml
│   └── grafana/
│       ├── dashboards/
│       └── provisioning/
│           ├── dashboards/
│           └── datasources/
├── src/
│   ├── main/
│   └── test/
├── target/
├── pom.xml
├── README.md
└── .gitignore
```

---

# Screenshots

Include screenshots of the following:

* Jenkins Dashboard
* Jenkins Pipeline Execution
* SonarQube Dashboard
* Docker Images
* Running Docker Containers
* Spring Boot Application
* Spring Boot Actuator Metrics
* Prometheus Targets
* Prometheus Graph
* Grafana Dashboard
* AWS EC2 Instance

---

# Future Enhancements

* Kubernetes Deployment
* Helm Charts
* Argo CD Integration
* AWS ECR Integration
* Node Exporter Monitoring
* cAdvisor Integration
* Prometheus Alertmanager
* Slack Notifications
* Email Notifications
* Terraform Infrastructure Provisioning
* Multi-stage Docker Builds

---

# Author

**Mihika Patekar**

## Skills

* AWS
* Jenkins
* Docker
* Kubernetes
* Terraform
* Maven
* SonarQube
* Prometheus
* Grafana
* Linux
* Git & GitHub
* CI/CD Automation

---

# License

This project is intended for learning and demonstration purposes.

---

If you found this project useful, consider starring the repository.
