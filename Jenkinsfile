pipeline {
    agent any  
    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/yourusername/my-java-app.git'  
            }
        }
        stage('Build') {
            steps {
                sh 'mvn clean package'  // For Maven projects  
            }
        }
        stage('Test') {
            steps {
                sh 'mvn test'  
                junit '**/target/surefire-reports/*.xml'  // Publish test results  
            }
        }
        stage('Deploy') {
            steps {
                sh 'echo "Deploying to staging..."'  
                // Add deployment commands (e.g., scp, Ansible, Docker)  
            }
        }
    }
    post {
        success {
            mail to: 'team@example.com',  
                 subject: 'Build Success',  
                 body: 'The build succeeded!'  
        }
        failure {
            mail to: 'team@example.com',  
                 subject: 'Build Failed',  
                 body: 'The build failed. Check Jenkins!'  
        }
    }
}
