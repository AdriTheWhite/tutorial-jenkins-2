pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo 'Configurando variables'
                def mvnHome = tool 'M3'
                env.PATH = "${mvnHome}/bin:${env.PATH}"
                echo "var mvnHome='${mvnHome}'"
                echo "var env.PATH='${env.PATH}'"
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
