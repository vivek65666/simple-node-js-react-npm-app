pipeline {
    agent any
    environment {
        CI = 'true'
    }
    stages {
        stage('Build') {
            steps {
                bat 'npm install'
            }
        }
        stage('Test') {
            steps {
                // Simplified command to avoid double "run"
                bat 'npm test' 
            }
        }
        stage('Deploy') {
            steps {
                bat 'npm run build'
                echo 'Project Built Successfully!'
            }
        }
    }
}