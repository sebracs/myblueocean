pipeline {
  agent any
  stages {
    stage('Environment') {
      steps {
        sh '''printenv
'''
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

    stage('Hallo') {
      steps {
        echo 'Hallo'
      }
    }

  }
}