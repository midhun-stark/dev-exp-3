pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Test') {
            steps {
                bat 'if not exist index.html exit 1'
                echo 'HTML file exists - Test passed'
            }
        }

        stage('Build') {
            steps {
                echo 'Preparing HTML application...'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying HTML application...'
            }
        }
    }

    post {
        success {
            echo 'HTML application deployed successfully!'
        }

        failure {
            echo 'Pipeline failed!'
        }
    }
}