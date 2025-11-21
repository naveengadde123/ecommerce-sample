pipeline {
  agent {
    docker { image 'node:16-alpine' }
  }

  stages {

    stage('Clone Repository') {
      steps {
        checkout([
          $class: 'GitSCM',
          branches: [[name: '*/main']],
          userRemoteConfigs: [[url: 'https://github.com/naveengadde123/ecommerce-sample']]
        ])
      }
    }

    stage('Show Repo Files') {
      steps {
        sh 'ls -la'
      }
    }

    stage('Test Node Version') {
      steps {
        sh 'node --version'
      }
    }
  }
}
