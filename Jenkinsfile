pipeline {
  agent any
  stages {
    stage('Checkout Sources') {
      steps {
        git(url: 'https://github.com/bepoland-academy/deployment-configuration.git', branch: 'development')
      }
    }
    stage('Pull Images') {
      steps {
        sh 'docker-compose -H main-server:2376 -f production/docker-compose.yml pull'
      }
    }
    stage('Redeploy Services') {
      steps {
        sh 'docker-compose -H main-server:2376 -f production/docker-compose.yml up -d'
      }
    }
  }
}