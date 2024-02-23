pipeline {
    environment {
       registry = "farahseddik/learnin-app"
       registryCredential = 'farahseddik'
       dockerImage = ''
  }
  agent any
  stages {
     stage('Build') {
       steps {
       bat 'cd nodejs-app'
        script {
          docker.build("${registry}:${BUILD_NUMBER}", "-f https://github.com/farahsedd/DevOps-Lab/blob/main/nodejs-app/Dockerfile")
        }       
      }
   }
 }
}
