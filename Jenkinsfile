pipeline {
  agent any
  stages {
    stage('docker') {
      steps {
        sh '''wget -qO- https://ipecho.net/plain ; echo
docker-compose --version
docker-compose build
docker-compose up'''
      }
    }
  }
}