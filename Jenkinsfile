pipeline {
  agent { docker { image 'python:3.5.1' } }
  stages {
    stage('prebuild') {
      steps {
        sh 'whoami; id'
      }
    }
    stage('build') {
      steps {
        sh 'python --version'
      }
    }
  }
}
