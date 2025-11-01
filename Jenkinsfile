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
                sh '🔧 Building the application...'
                bat 'echo Simulating build step...'
            }
        }

        stage('Deploy to Target Server') {
            steps {
                echo '🚀 Deploying to remote server via SSH...'
                bat '''
                echo Cleaning old files...
                echo Copying new files...
                echo Restarting Node/Python service...
                '''
            }
        }
    }

    post {
        success {
            echo '✅ Build succeeded! Sending success email...'
        }
        failure {
            echo '❌ Build failed! Sending failure email...'
        }
    }
}
