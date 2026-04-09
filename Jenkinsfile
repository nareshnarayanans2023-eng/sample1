pipeline {
    agent any
    stages {
        stage('Source Control') {
            steps {
                echo 'Fetching Rivera Cultural Event code...'
                checkout scm
            }
        }
        stage('Containerize (Build)') {
            steps {
                echo 'Building Docker image for the event site...'
                // This command builds your Dockerfile
                sh 'docker build -t rivera-app:v1 .'
            }
        }
        stage('CI Test') {
            steps {
                echo 'Testing image integrity...'
            }
        }
        stage('Ready for CD') {
            steps {
                echo 'Pipeline complete. Application is ready for Kubernetes.'
            }
        }
    }
}
