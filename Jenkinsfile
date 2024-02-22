pipeline {
    agent any

    environment {
        registry = "ranimmbarek/DevopsLab"
        dockerImage = ''
    }
    stages{
        stage('Build Docker image') {
            steps {
               script {dockerImage =docker.build registry + ":$BUILD_NUMBER"}
            }
        }
    }    
}

