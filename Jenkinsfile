pipeline {
  agent { docker { image 'python:3.5.1' } }
  stages {
    stage('precheck') {
      steps {
        sh 'id; whoami'
      }
    }
    stage('build') {
      steps {
        sh 'python --version'
      }
    }
  }
}
