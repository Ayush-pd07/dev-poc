pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                git 'https://github.com/Ayush-pd07/dev-poc.git'
            }
        }

        stage('Build') {
            steps {
                echo "Building..."
            }
        }
    }
}
