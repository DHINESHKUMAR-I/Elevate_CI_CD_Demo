# Spring Boot CI/CD Pipeline using GitHub Actions & Docker

## 📌 Project Overview

This project demonstrates a complete Continuous Integration and Continuous Deployment (CI/CD) pipeline for a Spring Boot application using **GitHub Actions** and **Docker**.

Whenever code is pushed to the `main` branch, GitHub Actions automatically:

- Checks out the source code
- Sets up Java
- Builds the Spring Boot application using Maven
- Builds a Docker image
- Pushes the Docker image to Docker Hub

This project was completed as part of the **Elevate Labs DevOps Internship - Task 1**.

---

## 🚀 Technologies Used

- Java 24
- Spring Boot
- Maven
- Docker
- Docker Hub
- GitHub
- GitHub Actions

---

## 📁 Project Structure

```
Elevate_CI_CD_Demo
│
├── .github
│   └── workflows
│       └── main.yml
├── src
├── Dockerfile
├── pom.xml
├── mvnw
├── mvnw.cmd
├── README.md
└── .gitignore
```

---

## ⚙️ CI/CD Workflow

The GitHub Actions workflow performs the following steps automatically whenever code is pushed to the `main` branch:

1. Checkout the repository
2. Set up Java 24
3. Cache Maven dependencies
4. Build the Spring Boot project
5. Login to Docker Hub
6. Build the Docker image
7. Push the Docker image to Docker Hub

---

## 🐳 Docker

### Build Docker Image

```bash
docker build -t springboot-cicd-demo .
```

### Run Docker Container

```bash
docker run -p 8080:8080 springboot-cicd-demo
```

---

## ☁️ Docker Hub

Docker image is automatically pushed to Docker Hub using GitHub Actions after every successful build.

Repository Format:

```
docker.io/<dockerhub-username>/springboot-cicd-demo
```

---

## ▶️ Running the Application

### Clone Repository

```bash
git clone https://github.com/<your-github-username>/Elevate_CI_CD_Demo.git
```

### Navigate to Project

```bash
cd Elevate_CI_CD_Demo
```

### Build Project

```bash
./mvnw clean package
```

### Run Application

```bash
java -jar target/*.jar
```

Open:

```
http://localhost:8080/hello
```

Expected Output:

```
Hello from Spring Boot CI/CD!
```

---

## 🔄 GitHub Actions Workflow

Workflow file location:

```
.github/workflows/main.yml
```

The pipeline is triggered automatically on every push to the `main` branch.

---

## 🔐 GitHub Secrets

The following repository secrets are used:

- DOCKER_USERNAME
- DOCKER_PASSWORD

These secrets securely authenticate GitHub Actions with Docker Hub.

---

## 📷 Screenshots

Add the following screenshots:

- Spring Boot application running
- Docker container running
- Docker Hub repository
- GitHub Actions successful workflow
- Docker image pushed successfully

---

## 📚 Learning Outcomes

Through this project, I learned:

- Continuous Integration (CI)
- Continuous Deployment (CD)
- GitHub Actions workflows
- Docker image creation
- Docker Hub integration
- GitHub Secrets
- Automated application deployment
- CI/CD pipeline automation

---

## 👨‍💻 Author

**Dhineshkumar I**

DevOps Internship - Elevate Labs
