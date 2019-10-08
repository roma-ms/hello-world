pipeline {
  agent any
  stages {
    stage('test') {
      parallel {
        stage('test') {
          steps {
            sh 'echo "hello  world"'
          }
        }
        stage('new') {
          steps {
            retry(count: 3) {
              sh 'mkdir "henry"'
            }

          }
        }
      }
    }
  }
  environment {
    username = 'ari'
    password = 'ari13'
  }
}