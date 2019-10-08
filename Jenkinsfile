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
    stage('test2') {
      parallel {
        stage('test2') {
          steps {
            echo 'i hope am getting this'
          }
        }
        stage('') {
          steps {
            mail(subject: 'test', body: 'test', from: 'holuwande@gmail.com', to: 'holuwande@yahoo.co.uk')
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