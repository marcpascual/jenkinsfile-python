pipeline {
  agent { docker { image 'python:3.5.1' } }
  stages {
    stage('prebuild') {
      steps {
        sh 'uname -a; id'
      }
    }
    stage('build') {
      steps {
        sh 'python --version'
      }
    }
    stage('postbuild') {
      steps {
        sh 'uname -a; id'
      }
    }
  }
}
