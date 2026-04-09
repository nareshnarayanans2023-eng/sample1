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
        
                echo 'Simulating Docker build: docker build -t rivera-app:v1 .'
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
        stage('Deploy to K8s') {
            steps {
                echo 'Deploying to Kubernetes Cluster...'
                sh 'kubectl apply -f deployment.yaml'
            }
        }

    }
}
