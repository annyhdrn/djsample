pipeline {
  agent any
  stages {
    stage('Checkout Code') {
      steps {
        git(url: 'https://github.com/annyhdrn/djsample', branch: 'master')
      }
    }

    stage('') {
      steps {
        sh 'ls -la'
      }
    }

  }
}