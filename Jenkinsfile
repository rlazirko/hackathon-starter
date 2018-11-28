pipeline {
  agent any
  stages {
    stage('docker') {
      steps {
        sh '''echo "Installing docker..."
sudo apt-get update
sudo apt-key adv --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 58118E89F3A912897C070ADBF76221572C52609D
sudo apt-add-repository \'deb https://apt.dockerproject.org/repo ubuntu-xenial main\'
sudo apt-get update
apt-cache policy docker-engine
sudo apt-get install -y docker-engine
sudo systemctl status docker
curl -L https://github.com/docker/compose/releases/download/1.8.0/docker-compose-`uname -s`-`uname -m` > /usr/local/bin/docker-compose
'''
        sh '''wget -qO- https://ipecho.net/plain ; echo
docker-compose --version
docker-compose build
docker-compose up'''
      }
    }
  }
}