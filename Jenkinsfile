pipeline {
    environment {
        registry = "ranimmbarek/DevopsLab"
        dockerImage = ''
    }
    agent any
    stages{
        stage('Build Docker image') {
            steps {
               script {dockerImage =docker.build registry + ":$BUILD_NUMBER"}
            }
        }
    }    
}

