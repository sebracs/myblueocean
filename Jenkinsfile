pipeline {
  agent any
  stages {
    stage('Environment') {
      agent any
      steps {
        sh '''printenv
echo /etc/os-release'''
      }
    }

  }
}