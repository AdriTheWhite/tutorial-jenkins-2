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
        stage('Test') {
            steps {
                /* `make check` returns non-zero on test failures,
                * using `true` to allow the Pipeline to continue nonetheless
                */
                
                junit '**/target/*.xml' 
            }
        }
    }
    post { 
        failure { 
            echo 'Ha habido un error :v'
        }
    }
}
