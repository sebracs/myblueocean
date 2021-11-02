pipeline {
  agent any
  stages {
    stage('Environment') {
      parallel {
        stage('Environment') {
          steps {
            sh '''printenv
cat /etc/os-release
        '''
          }
        }

        stage('Test') {
          agent any
          steps {
            input 'Was test successful?'
          }
        }

      }
    }

  }
}