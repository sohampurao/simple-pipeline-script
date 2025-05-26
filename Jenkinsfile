pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                checkout scm  // Checks out code from SCM
            }
        }
        stage('Build') {
            steps {
                sh 'echo "Building the project..."'  // Replace with build commands
            }
        }
        stage('Test') {
            steps {
                sh 'echo "Running tests..."'  // Replace with test commands
            }
        }
    }
    post {
        success {
            echo 'Pipeline succeeded!'
        }
        failure {
            echo 'Pipeline failed!'
        }
    }
}
