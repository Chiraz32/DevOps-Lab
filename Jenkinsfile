pipeline {
    environment {
       registry = "farahseddik/learnin-app"
       registryCredential = 'farahseddik'
       dockerImage = ''
  }
  agent any
  stages {
     stage('Build') {
         bat 'cd nodejs-app'
       steps {
        script {dockerImage =docker.build registry + ":$BUILD_NUMBER"}
       }
  }
}
}
