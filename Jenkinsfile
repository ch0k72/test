pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                // Ensure a clean checkout of a specific branch
                checkout([
                    $class: 'GitSCM',
                    branches: [[name: '*/main']],  // Or your branch name
                    userRemoteConfigs: [[url: 'https://github.com/ch0k72/test.git']]
                ])
            }
        }
        stage('Build') {
            steps {
                echo 'Building...'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing...'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying...'
                sh 'git show-ref'
            }
        }
    }
}
