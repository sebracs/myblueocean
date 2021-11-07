pipeline {
  agent any
  stages {
    stage('Environment') {
      steps {
        sh '''printenv
'''
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

        stage('Answer') {
          agent {
            kubernetes {
              inheritFrom 'default'
              defaultContainer 'powershell-core'
              yaml '''
                spec:
                  containers:
                  - name: powershell-core
                    image: mcr.microsoft.com/powershell:alpine-3.13
                    command:
                    - cat
                    tty: true
              '''
            }

          }
          steps {
            pwsh 'echo "Thanks all good!"'
          }
        }

      }
    }

  }
}