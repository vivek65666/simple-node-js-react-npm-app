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
                // We use npm test directly now that the scripts folder is gone
                bat 'npm test -- --watchAll=false' 
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