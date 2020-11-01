pipeline {
  agent any
  stages {
    stage('build the code') {
      steps {
        echo 'This will fetch the code from git repo'
        echo 'And build the code'
      }
    }

    stage('Run smoke Tests') {
      steps {
        echo 'This stage will run the smoke tests'
      }
    }

    stage('certify the build') {
      steps {
        echo 'This is to verify the test results '
      }
    }

  }
  post {
    always {
      emailext(body: 'the build status is notified..please check', subject: 'test email', to: 'kadarla.pradeep4@gmail.com')
    }

  }
}