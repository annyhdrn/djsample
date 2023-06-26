pipeline {
  agent any
  stages {
    stage('Checkout Code') {
      steps {
        git(url: 'https://github.com/annyhdrn/djsample', branch: 'master')
      }
    }

    stage('log') {
      steps {
        sh '''ls -la
'''
      }
    }

    stage('Install Dependencies') {
      steps {
        sh '''pip install -r requirements.txt
sh deploy/setup.sh'''
      }
    }

    stage('Deploy') {
      steps {
        sh '''python manage.py migrate
python manage.py runserver'''
      }
    }

  }
}