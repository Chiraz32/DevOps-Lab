pipeline {
    agent any

    environment {
        registry = "ranimmbarek/DevopsLab"
    }
    stages{
        stage('Build Docker image') {
            steps {
                script {
                    docker.build("${registry}:${BUILD_NUMBER}")
                }
            }
        }
    }    
}

