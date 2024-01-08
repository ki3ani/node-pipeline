pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Build') {
            steps {
                echo 'Building the application...'
                script {
                    // Install dependencies
                    sh 'npm install'
                }
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
                script {
                    // Run tests
                    sh 'npm test'
                }
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying the application...'
                // Add deployment commands here (e.g., copying files to a server)
            }
        }
    }
}
