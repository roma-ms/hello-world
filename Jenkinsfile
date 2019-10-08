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
    stage('error') {
      steps {
        mail(subject: 'test', body: 'test', from: 'holuwande@gmail.com', to: 'holuwande@yahoo.co.uk')
      }
    }
  }
  environment {
    username = 'ari'
    password = 'ari13'
  }
}