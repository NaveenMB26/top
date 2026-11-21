
pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'master',
                    credentialsId: 'jen'
		    url: 'https://github.com/NaveenMB26/top.git'
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

