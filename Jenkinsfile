pipeline {
    environment {
       registry = "farahseddik/learnin-app"
       registryCredential = 'farahgithub'
       dockerImage = ''
  }
  agent any
  stages {
     stage('Build') {
       steps {
        script {
          docker.build("${registry}:${BUILD_NUMBER}", "-f https://github.com/farahsedd/DevOps-Lab/blob/main/nodejs-app/Dockerfile")
        }       
      }
   }
 }
}
