pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                echo 'Cloning project from GitHub...'
            }
        }

        stage('Build') {
            steps {
                echo 'Build Step: Checking files in workspace'
                sh 'ls -la'
            }
        }

        stage('Test') {
            steps {
                echo 'Testing HTML...'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying application...'
            }
        }
    }

    post {
        success {
            echo 'Pipeline finished successfully!'
        }

        failure {
            echo 'Pipeline failed! Check build logs.'
        }
    }
}
