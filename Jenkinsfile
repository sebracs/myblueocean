pipeline {
  agent any
  stages {
    stage('Environment') {
      steps {
        sh '''printenv
cat /etc/os-release
        '''
      }
    }

    stage('Test') {
      steps {
        input 'Was test good?'
      }
    }

    stage('Errors') {
      agent any
      steps {
        warnError(message: 'Error is not that bad') {
          error 'Oh nooooo!!!'
        }

      }
    }

  }
}