pipeline {
    agent { docker { image 'node:20.14.0-alpine3.20' } }
    stages {
        stage('Build') {
            steps {
                sh 'node --version'
                sh 'npm --version'
                sh 'npm install'
                sh 'npm run build'
            }
        }
        stage('Test') {
            steps {
                sh 'npm test'
            }
        }
        stage('Deploy') {
            steps {
                sh 'echo "Deploying..."'
                // Add deployment steps here
            }
        }
    }
}
