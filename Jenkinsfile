pipeline {
  agent any
  stages {
    stage(' Checkout Code') {
      steps {
        git(url: ' https://github.com/ksanjaykumar1/curriculum-app', branch: 'master')
      }
    }

    stage('logs') {
      steps {
        sh 'ls -la'
      }
    }

  }
}