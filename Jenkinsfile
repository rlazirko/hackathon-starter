pipeline {
  agent any
  stages {
    stage('docker') {
      steps {
        sh '''wget -qO- https://ipecho.net/plain
curl -fsSL https://get.docker.com -o get-docker.sh
sh get-docker.sh
docker-compose --version
docker-compose build
docker-compose up'''
      }
    }
  }
}