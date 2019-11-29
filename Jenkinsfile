pipeline {
  agent {
    docker {
      image 'node:6-alpine'
      args '-p 3001:3000 -p 5000:5000'
    }

  }
  stages {
    stage('Build') {
      parallel {
        stage('Build') {
          steps {
            sh 'npm install'
          }
        }

        stage('Test') {
          steps {
            sh './jenkins/scripts/test.sh'
          }
        }

      }
    }

  }
  environment {
    CI = 'true'
  }
}