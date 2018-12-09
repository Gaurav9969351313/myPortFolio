pipeline {
  agent {
    docker {
      args '-p 3000:3000'
      image 'node:6-alpine'
    }

  }
  stages {
    stage('build') {
      steps {
        sh 'npm install'
      }
    }
    stage('create dir') {
      steps {
        sh '''cd myPortFolio_master
ng build --prod'''
      }
    }
  }
}