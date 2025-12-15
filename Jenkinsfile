pipeline {
  agent any

  stages {
    stage('Checkout') {
      steps {
        checkout scm
      }
    }

    stage('Install Dependencies') {
      steps {
        bat 'npm install'
      }
    }

    stage('Run App') {
      steps {
        bat '''
        echo Starting NodeJS app...
        node index.js
        '''
      }
    }
  }
}
