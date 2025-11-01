pipeline {
    agent any

    stages {
        stage('Checkout Code') {
            steps {
                git branch: 'main', url: 'https://github.com/komma-gayathri/jenkins-demo.git'
            }
        }

        stage('Build') {
            steps {
                echo '🔧 Building the application...'
                sh 'echo Build successful!'
            }
        }

        stage('Deploy to Target Server') {
            steps {
                echo '🚀 Deploying to target server...'
                sh 'echo Deployment completed successfully!'
            }
        }
    }

    post {
        success {
            echo '✅ Build and deployment successful!'
        }
        failure {
            echo '❌ Build failed! Sending failure email...'
        }
    }
}
