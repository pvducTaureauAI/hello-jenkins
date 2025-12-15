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

    stage('Install Dependencies') {
      steps {
        sh 'npm install'
      }
    }

    stage('Run App') {
      steps {
        sh 'node index.js'
      }
    }
  }
}
