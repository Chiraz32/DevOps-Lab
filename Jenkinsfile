pipeline {
    environment {
        registry = "ranimmbarek/DevopsLab"
        dockerImage = ''
    }
    agent any 
    stages {
        stage('Pull & Build') { 
            steps {
                sh 'git pull https://github.com/farahsedd/DevOps-Lab'
                bat 'cd nodejs-app'
            }
        }
    }
}
