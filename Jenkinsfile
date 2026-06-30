pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                git branch: 'main',
                url: 'https://github.com/DHINESHKUMAR-I/Elevate_CI_CD_Demo.git'
            }
        }

        stage('Build') {
            steps {
                bat 'mvnw.cmd clean package'
            }
        }

        stage('Test') {
            steps {
                bat 'mvnw.cmd test'
            }
        }

        stage('Build Docker Image') {
            steps {
                bat 'docker build -t springboot-cicd-demo .'
            }
        }

        stage('Run Docker Container') {
            steps {
                bat 'docker run -d -p 8081:8080 --name springboot-container springboot-cicd-demo'
            }
        }
    }
}