
pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main',
                    credentialsId: 'github-credentials',
                    url: 'https://github.com/USERNAME/jenkins-demo.git'
            }
        }

        stage('Build') {
            steps {
                echo 'Application building'
                sh 'ls -l'
            }
        }

        stage('Test') {
            steps {
                echo 'Application testing'
            }
        }
    }

    post {
        success {
            echo 'Build Successful'
        }
        failure {
            echo 'Build Failed'
        }
    }
}

