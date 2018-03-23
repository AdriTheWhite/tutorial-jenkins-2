
pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo 'Configurando variables'
                echo bat 'javac -version'
               
            }
        }
        stage('Deploy') {
            when {
                branch 'production'
            }
            steps {
                echo 'Deploying'
            }
        }
    }
}
