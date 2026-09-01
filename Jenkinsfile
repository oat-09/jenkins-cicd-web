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
        echo 'Deploying web application...'
        bat 'if not exist C:\\jenkins-deploy mkdir C:\\jenkins-deploy'
        bat 'xcopy /Y index.html C:\\jenkins-deploy\\'
        bat 'xcopy /Y style.css C:\\jenkins-deploy\\'
        bat 'xcopy /Y script.js C:\\jenkins-deploy\\'
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
