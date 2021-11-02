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

  }
}