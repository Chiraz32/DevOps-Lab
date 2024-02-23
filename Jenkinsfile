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
        script {dockerImage =docker.build registry + ":$BUILD_NUMBER"}
       }
  }
}
}
