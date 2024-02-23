pipeline {
    environment {
        registry = "ranimmbarek/DevopsLab"
    }
    agent any
    stages{
        stage('Build Docker image') {
            steps {
               script {
                   docker.build("${registry}:${BUILD_NUMBER}", "-f https://github.com/farahsedd/DevOps-Lab/blob/main/nodejs-app/Dockerfile")
               }
            }
        }
    }    
}

