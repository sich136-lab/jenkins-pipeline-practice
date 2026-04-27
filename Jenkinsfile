pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Install') {
            steps {
                bat 'echo install step'
            }
        }

        stage('Test') {
            steps {
                bat 'echo test step'
            }
        }

        stage('Start') {
            when {
                branch 'main'
            }
            steps {
                bat 'echo start step'
            }
        }
    }

    post {
        success {
            echo 'Pipeline 성공적으로 완료!'
        }
        failure {
            echo 'Pipeline 실패!'
        }
    }
}
