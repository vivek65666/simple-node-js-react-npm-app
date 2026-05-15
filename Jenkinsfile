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
                // Vitest uses 'run' to execute tests once without watching
                bat 'npm test -- run' 
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