#!groovy

pipeline {
    agent any
    stages {
        stage('Test') {
            steps {
                bat 'make check'
            }
        }
    }
    post {
        always {
            junit '**/target/*.xml'
        }
        failure {
            mail to: aescriche@isoco.com, subject: 'The Pipeline failed :('
        }
    }
}
