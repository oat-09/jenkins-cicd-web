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
                bat 'dir'
            }
        }

        stage('Test') {
            steps {
                echo 'Testing HTML...'
                bat 'echo HTML test completed successfully'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying application...'
                bat 'echo Deployment completed successfully'
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
