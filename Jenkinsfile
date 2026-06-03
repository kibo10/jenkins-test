pipeline {
  agent any

  stages {

    stage('Build') {
      steps {
        echo 'Building app...'
      }
    }

    stage('Deploy') {
      steps {
        echo 'Deploying to Docker...'
        sh 'docker ps'
      }
    }
  }
}
