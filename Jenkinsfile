pipeline {
    agent any

    stages {

        stage('Clean Workspace') {
            steps {
                deleteDir()
            }
        }

        stage('Checkout Code') {
            steps {
                git branch: 'main', url: 'https://github.com/Ayush-pd07/dev-poc.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t ayush-app .'
            }
        }

        stage('Run Docker Container') {
            steps {
                sh '''
                docker stop ayush-container || true
                docker rm ayush-container || true
                docker run -d -p 8081:80 --name ayush-container ayush-app
                '''
            }
        }
    }
}
