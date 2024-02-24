pipeline {
    environment {
       registry = "farahseddik/learnin-app"
       registryCredential = 'farahgithub'
       dockerImage = ''
       dockerfilePath = 'nodejs-app/Dockerfile'

  }
  agent any
  stages {
     stage('Build') {
       steps {
        script {
          docker.build("${registry}:${BUILD_NUMBER}","-f ${dockerfilePath} .")
        }       
      }
   }
    stage('Push') {
     steps {
        script {
            docker.withRegistry( '', registryCredential ) {
                  dockerImage.push()
            }
        }
     }
  }

 }
}
