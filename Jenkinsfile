pipeline {
  agent any
  stages {
    stage('Environment') {
      steps {
        cat '''
          printenv
          echo /etc/os-release
        '''
      }
    }
  }
}
