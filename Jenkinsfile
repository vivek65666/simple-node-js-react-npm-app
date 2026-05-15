pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                bat 'npm install' 
            }
        }
        stage('Test') {
            steps {
                // Since we moved Jenkinsfile to the root, 
                // we must point to the scripts inside the folder
                bat 'jenkins/scripts/test.sh' 
            }
        }
    }
}