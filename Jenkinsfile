
pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo 'Configurando variables'
                
           
                
                bat 'java -version'
                
                checkout scm
                
                echo 'Compilando aplicación'
                
                bat 'mvn clen compile'
               
            }
        }
        stage('Deploy') {
            when {
                branch 'master'
            }
            steps {
                echo 'Deploying'
            }
        }
    }
}
