pipeline {
  agent any
  stages {
    stage(' Checkout Code') {
      steps {
        git(url: ' https://github.com/ksanjaykumar1/curriculum-app', branch: 'master')
      }
    }

    stage('logs') {
      parallel {
        stage('logs') {
          steps {
            sh 'ls -la'
          }
        }

        stage('Front-End Unit testing') {
          steps {
            sh 'cd curriculum-front && npm i && npm run test:unit'
          }
        }

      }
    }

    stage('Build') {
      steps {
        sh 'docker build -f curriculum-front/Dockerfile .'
      }
    }

  }
}