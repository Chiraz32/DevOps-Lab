pipeline {
    environment {
       registry = "farahseddik/learnin-app"
       registryCredential = 'farahdocker'
       dockerImage = ''
       dockerfilePath = 'nodejs-app/Dockerfile'

  }
  agent any
  stages {
     stage('Build') {
       steps {
        script {
         dockerImage = docker.build("${registry}:${BUILD_NUMBER}","-f ${dockerfilePath} .")
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
   stage('Run') {
     steps {
       script {  dockerImage.run("-p 80:80 ")
       }
     }
   }
 }
}
