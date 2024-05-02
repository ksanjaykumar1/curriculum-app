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

    stage('Build') {
      steps {
        sh 'docker build -f curriculum-front/Dockerfile .'
      }
    }

    stage('Login into Dockerhub') {
      environment {
        DOCKERHUB_USER = 'sanjayImages'
        DOCKERHUB_PASSWORD = 'PmUmTCAAw'
      }
      steps {
        sh 'docker login -u $DOCKERHUB_USER -p $DOCKERHUB_PASSWORD'
      }
    }

  }
}