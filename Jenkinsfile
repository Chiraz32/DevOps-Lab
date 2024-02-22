pipeline {
    agent any

    environment {
        registry = "ranimmbarek/DevopsLab"
    }
    stages{
        stage('Build Docker image') {
            steps {
                script {
                    def docker = docker.image('docker')
                    docker.build("${registry}:${BUILD_NUMBER}")
                }
            }
        }
    }    
}

