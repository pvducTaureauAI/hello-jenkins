pipeline {
  agent any

  tools {
    nodejs 'node18'
  }

  stages {
    stage('Checkout') {
      steps {
        checkout scm
      }
    }

    stage('Install') {
      steps {
        sh 'npm install'
      }
    }

    stage('Start App') {
      steps {
        sh '''
          npm install -g pm2
          pm2 stop hello-jenkins || true
          pm2 start index.js --name hello-jenkins
        '''
      }
    }
  }
}
