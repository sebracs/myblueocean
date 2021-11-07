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

    stage('MyStage') {
      agent any
      steps {
        sleep 10
        warnError(message: 'Error is not that bad') {
          error 'Oh nooooo!!!'
        }

      }
    }

  }
}