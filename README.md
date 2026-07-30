# 🚀 End-to-End CI/CD Pipeline for Java Spring Boot using Jenkins, Docker, SonarQube, Prometheus & Grafana

<div align="center">

# 🚀 Java Spring Boot DevOps CI/CD Pipeline

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0F2027,50:203A43,100:2C5364&height=220&section=header&text=CI/CD%20Pipeline&fontSize=42&fontColor=ffffff&animation=fadeIn" width="100%"/>

<p align="center">
<img src="https://readme-typing-svg.herokuapp.com?font=Poppins&size=26&duration=3500&pause=1000&color=36BCF7&center=true&vCenter=true&width=900&lines=Java+Spring+Boot+CI%2FCD+Pipeline;Jenkins+%7C+Docker+%7C+SonarQube;Prometheus+%7C+Grafana+Monitoring;AWS+EC2+Deployment;DevOps+Automation+Project" />
</p>

---

### ⭐ Built with Modern DevOps Technologies

<p align="center">

![Java](https://img.shields.io/badge/Java-21-red?style=for-the-badge&logo=openjdk)

![Spring Boot](https://img.shields.io/badge/Spring_Boot-3-brightgreen?style=for-the-badge&logo=springboot)

![Maven](https://img.shields.io/badge/Maven-Build-blue?style=for-the-badge&logo=apachemaven)

![Jenkins](https://img.shields.io/badge/Jenkins-CI-red?style=for-the-badge&logo=jenkins)

![Docker](https://img.shields.io/badge/Docker-Container-blue?style=for-the-badge&logo=docker)

![SonarQube](https://img.shields.io/badge/SonarQube-Code_Quality-4E9BCD?style=for-the-badge&logo=sonarqube)

![Prometheus](https://img.shields.io/badge/Prometheus-Monitoring-orange?style=for-the-badge&logo=prometheus)

![Grafana](https://img.shields.io/badge/Grafana-Dashboard-F46800?style=for-the-badge&logo=grafana)

![AWS](https://img.shields.io/badge/AWS-EC2-orange?style=for-the-badge&logo=amazonaws)

![Ubuntu](https://img.shields.io/badge/Ubuntu-Linux-E95420?style=for-the-badge&logo=ubuntu)

</p>

---

<p align="center">

<a href="https://github.com/yourusername/java-demo">
<img src="https://img.shields.io/badge/View_Project-181717?style=for-the-badge&logo=github">
</a>

<a href="#">
<img src="https://img.shields.io/badge/Live_Demo-success?style=for-the-badge">
</a>

<a href="#">
<img src="https://img.shields.io/badge/Documentation-blue?style=for-the-badge">
</a>

<a href="#">
<img src="https://img.shields.io/badge/License-MIT-green?style=for-the-badge">
</a>

</p>

</div>

---

# 📖 Project Overview

This project demonstrates a **complete enterprise-level CI/CD pipeline** for a Java Spring Boot application using modern DevOps tools.

The pipeline automates the complete software delivery lifecycle—from code commit to deployment—while continuously monitoring application performance using **Prometheus** and **Grafana**.

---

# ✨ Features

✅ GitHub Source Code Integration

✅ Automated Jenkins Pipeline

✅ Maven Build Automation

✅ Unit Testing

✅ SonarQube Static Code Analysis

✅ Docker Image Creation

✅ Automatic Container Deployment

✅ AWS EC2 Deployment

✅ Spring Boot Actuator Metrics

✅ Prometheus Monitoring

✅ Grafana Dashboards

✅ Continuous Delivery

---

# 🛠 Technology Stack

| Technology | Purpose |
|------------|----------|
| Java 21 | Programming Language |
| Spring Boot 3 | Backend Framework |
| Maven | Build Tool |
| Jenkins | CI/CD |
| GitHub | Source Code |
| Docker | Containerization |
| SonarQube | Code Quality |
| Prometheus | Metrics Collection |
| Grafana | Visualization |
| AWS EC2 | Deployment |
| Ubuntu | Operating System |

---

# 🏗 Project Architecture

```text
                        GitHub Repository
                               │
                               ▼
                      Jenkins Pipeline
                               │
      ┌────────────────────────┼────────────────────────┐
      │                        │                        │
      ▼                        ▼                        ▼
 Maven Build             Unit Testing          SonarQube Scan
                               │
                               ▼
                    Build Docker Image
                               │
                               ▼
                 Stop Existing Container
                               │
                               ▼
                  Deploy New Container
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

# 🔄 CI/CD Workflow

```text
Developer
    │
    ▼
Git Push
    │
    ▼
GitHub Repository
    │
    ▼
Jenkins Pipeline
    │
    ├──────────────► Maven Build
    │
    ├──────────────► Unit Test
    │
    ├──────────────► SonarQube Scan
    │
    ├──────────────► Package Application
    │
    ├──────────────► Docker Build
    │
    ├──────────────► Docker Deploy
    │
    ▼
Running Spring Boot Application
    │
    ▼
Actuator Metrics
    │
    ▼
Prometheus
    │
    ▼
Grafana Dashboard
```

---

# 🚀 Jenkins Pipeline Stages

| Stage | Description |
|---------|-------------|
| Checkout | Clone GitHub Repository |
| Build | Maven Clean Package |
| Test | Execute Unit Tests |
| SonarQube | Static Code Analysis |
| Docker Build | Build Docker Image |
| Docker Deploy | Deploy Latest Container |
| Monitoring | Metrics Collection |

---

# 🚀 Running Locally

## Clone Repository

```bash
git clone https://github.com/yourusername/java-demo.git
```

```bash
cd java-demo
```

---

## Build

```bash
mvn clean package
```

---

## Run

```bash
java -jar target/java-demo-1.0.0.jar
```

---

Application

```
http://localhost:8081
```

Health

```
http://localhost:8081/actuator/health
```

Metrics

```
http://localhost:8081/actuator/prometheus
```

---

# 🐳 Docker Deployment

Build Image

```bash
docker build -t java-demo .
```

Run Container

```bash
docker run -d \
-p 8081:8081 \
--name java-demo-container \
java-demo
```

Check Running Containers

```bash
docker ps
```

---

# 📊 Monitoring Stack

```text
Spring Boot
      │
      ▼
Spring Boot Actuator
      │
      ▼
Prometheus
      │
      ▼
Grafana
```

---

## Start Monitoring

```bash
docker compose up -d
```

---

# 🌐 Services

| Service | URL |
|----------|------|
| Spring Boot | http://localhost:8081 |
| Actuator | http://localhost:8081/actuator |
| Prometheus | http://localhost:9090 |
| Grafana | http://localhost:3000 |
| SonarQube | http://localhost:9000 |

---

# 📈 Metrics Monitored

- JVM Memory
- Heap Usage
- CPU Usage
- HTTP Requests
- Active Threads
- Garbage Collection
- System Load
- Process Uptime
- Tomcat Metrics

---

# 📂 Project Structure

```text
java-demo
│
├── Dockerfile
├── docker-compose.yml
├── Jenkinsfile
├── pom.xml
├── README.md
│
├── monitoring
│   ├── prometheus
│   │      └── prometheus.yml
│   │
│   └── grafana
│       ├── dashboards
│       └── provisioning
│
├── src
│   ├── main
│   └── test
│
└── target
```

---

# 📷 Screenshots

Replace these placeholders with your screenshots.

| Jenkins | SonarQube |
|-----------|-----------|
| ![](images/jenkins.png) | ![](images/sonarqube.png) |

| Docker | Prometheus |
|----------|-------------|
| ![](images/docker.png) | ![](images/prometheus.png) |

| Grafana |
|----------|
| ![](images/grafana.png) |

---

# 🔮 Future Enhancements

- ☸ Kubernetes Deployment
- 🚀 Helm Charts
- 🔄 ArgoCD
- 📦 AWS ECR
- 📊 Node Exporter
- 📈 cAdvisor
- 🔔 AlertManager
- 💬 Slack Notifications
- 📧 Email Notifications
- ☁ Terraform Infrastructure
- 🐳 Multi-stage Docker Builds

---

# 👨‍💻 Author

## Mihika Patekar

### Skills

- AWS
- Docker
- Jenkins
- Kubernetes
- Terraform
- SonarQube
- Prometheus
- Grafana
- Maven
- Linux
- GitHub Actions

---

<div align="center">

## ⭐ Support

If you found this project useful,

### ⭐ Star this Repository ⭐

<img src="https://readme-typing-svg.herokuapp.com?font=Poppins&size=22&duration=3000&pause=1000&color=00FFAA&center=true&vCenter=true&width=600&lines=Thanks+for+visiting!;Happy+Learning!;Keep+Building+Awesome+Projects!"/>

---

Made with ❤️ using Java, Spring Boot, Jenkins, Docker & AWS

</div>
