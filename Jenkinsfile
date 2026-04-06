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

        stage('Build') {
            steps {
                echo 'Build Stage Running...'
            }
        }

        stage('Test') {
            steps {
                echo 'Testing Stage Running...'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deployment Stage Running...'
            }
        }
    }
}
