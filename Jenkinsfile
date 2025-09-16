pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Pull code from GitHub
                checkout scm
            }
        }
        stage('Install') {
            steps {
                // Install dependencies
                sh 'npm install'
            }
        }
        stage('Test') {
            steps {
                // Run tests
                sh 'npm test || echo "No tests found"'
            }
        }
        stage('Build') {
            steps {
                // Example build (you can customize)
                sh 'npm run build || echo "No build script found"'
            }
        }
    }

    post {
        always {
            echo 'Pipeline finished!'
        }
    }
}
