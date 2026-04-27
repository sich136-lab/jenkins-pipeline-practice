pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Run') {
            steps {
                bat 'type hello.txt'
            }
        }
    }

    post {
        success {
            echo 'Pipeline 성공'
        }
        failure {
            echo 'Pipeline 실패'
        }
    }
}
