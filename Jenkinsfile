pipeline {
  agent any
  stages {
    stage('Checkout Code') {
      steps {
        git(url: 'https://github.com/annyhdrn/djsample', branch: 'master')
      }
    }

    stage('log') {
      parallel {
        stage('log') {
          steps {
            sh 'ls -la'
          }
        }

        stage('backen_test') {
          steps {
            sh 'cd phantomapp && npm i && npm run test:unit'
          }
        }

      }
    }

  }
}