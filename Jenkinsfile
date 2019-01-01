pipeline {
	/*
		this can also be a labelled worker agent
  	agent { label 'slave1' }
	*/
  agent { docker { image 'python:3.5.1' } }

	environment {
		FOO = 'bar'
		MESSAGE = 'hello world'
	}

	options {
		timeout(10)
	}

  stages {

    stage('prebuild') {
      steps {
        sh '''
					echo hello world
					echo mary had a little lamb
					pwd
					id
				'''
      }
    }

    stage('build 1') {
			when {
				branch '*/master'
			}
      steps {
        sh 'python --version'
      }
    }

    stage('build 2') {
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

	/* notification
	post {
		success {
			mail to: "user@gmail.com",
			subject: "SUCCESS: ${currentBuild.fullDisplayName}",
			body: "yay, we passed"
		}
		failure {
			mail to: "user@gmail.com",
			subject: "FAILURE: ${currentBuild.fullDisplayName}",
			body: "boo, we failed"
		}
	}
	*/

}
