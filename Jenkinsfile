pipeline {
    environment {
       registry = "farahseddik/learnin-app"
       registryCredential = 'farahseddik'
       docker Image = ''
  }
  agent any
  stages {
     stage('Build') {
       steps {
        script {dockerImage =docker.build registry + ":$BUILD_NUMBER"}
       }
  }
}
}
