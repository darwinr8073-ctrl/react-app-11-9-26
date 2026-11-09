pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/darwinr8073-ctrl/react-docker-compose.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t darwindoc/react-task-manager:latest ./frontend'
            }
        }

        stage('Deploy with Docker Compose') {
            steps {
                sh 'docker compose up -d --build'
            }
        }
    }
}
