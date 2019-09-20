pipeline {
  agent {
    docker {
      image 'python:3.6-alpine'
      args '-p 3000:3000'
    }
  }
  environment {
    CI = 'true'
  }
  stages {
    stage('Build') {
      steps {
        sh 'pip install -r requirements.txt'
      }
    }
    stage('Test') {
      steps {
        sh 'pytest test_sample.py'
      }
    }
  }
}
