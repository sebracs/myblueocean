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
      parallel {
        stage('Hallo') {
          steps {
            echo 'Hallo'
          }
        }

        stage('Question') {
          steps {
            sh 'echo "How are you?"'
          }
        }

        stage('Anwser') {
          steps {
            pwsh 'echo "Thanks all good!"'
          }
        }

      }
    }

  }
}