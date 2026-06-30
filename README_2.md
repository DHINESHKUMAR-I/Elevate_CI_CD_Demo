# Jenkins CI/CD Pipeline for Spring Boot Application

## 📌 Project Overview

This project demonstrates a simple Continuous Integration and Continuous Deployment (CI/CD) pipeline using **Jenkins**, **Docker**, and a **Spring Boot** application.

The Jenkins pipeline automatically performs the following tasks:

- Clones the source code from GitHub
- Builds the Spring Boot application using Maven
- Runs the project tests
- Builds a Docker image
- Deploys the application by running a Docker container

This project was completed as part of the **Elevate Labs DevOps Internship - Task 2**.

---

## 🚀 Technologies Used

- Java 24
- Spring Boot
- Maven
- Jenkins
- Docker
- Git
- GitHub

---

## 📂 Project Structure

```
Elevate_CI_CD_Demo
│
├── src/
├── Dockerfile
├── Jenkinsfile
├── pom.xml
├── mvnw
├── mvnw.cmd
├── README.md
└── .gitignore
```

---

## ⚙️ Jenkins Pipeline Stages

The Jenkins pipeline performs the following stages:

1. Checkout Source Code
2. Build Spring Boot Application
3. Run Tests
4. Build Docker Image
5. Run Docker Container

---

## 📄 Jenkinsfile

The pipeline is defined in the `Jenkinsfile` located in the project root.

---

## 🐳 Docker

### Build Docker Image

```bash
docker build -t springboot-cicd-demo .
```

### Run Docker Container

```bash
docker run -d -p 8081:8080 --name springboot-container springboot-cicd-demo
```

---

## ▶️ Running the Application

After successful deployment, access the application at:

```
http://localhost:8081/hello
```

Expected Output:

```
Hello from Spring Boot CI/CD!
```

---

## 🔧 Jenkins Configuration

- Pipeline Job
- Pipeline Script from SCM
- GitHub Repository Integration
- Jenkinsfile Configuration
- Automatic Build Execution

---

## 📷 Screenshots

Include the following screenshots:

- Jenkins Dashboard
- Successful Pipeline Execution
- Console Output (Finished: SUCCESS)
- Docker Desktop Running Container
- Spring Boot Application Output in Browser

---

## 📚 Learning Outcomes

Through this project, I learned:

- Jenkins Installation and Configuration
- Creating Jenkins Pipelines
- Writing a Jenkinsfile
- GitHub Integration with Jenkins
- Maven Build Automation
- Docker Image Creation
- Docker Container Deployment
- CI/CD Pipeline Automation

---

## 👨‍💻 Author

**Dhineshkumar I**

DevOps Internship – Elevate Labs