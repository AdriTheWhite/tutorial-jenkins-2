#!groovy

pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo 'Building'
                
                archiveArtifacts artifacts: '**/target/*.jar', fingerprint: true 
            }
        }
    }
    post { 
        failure { 
            echo 'Ha habido un error :v'
        }
    }
}
