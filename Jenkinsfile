pipeline {
  agent any
  stages {
//    stage('Clone Repository') {
//      steps {
//        checkout([$class: 'GitSCM',
//        branches: [[name: '*/main']],
//        userRemoteConfigs: [[url: 'https://github.com/Python-is-better-than-Java/PES2UG21CS096_Jenkins.git']]])
//      }
//    }
    stage('Build') {
      steps {
        build 'PES2UG21CS096-1'
        sh 'g++ main.cpp -o output'
      }
    }
    stage('Test') {
      steps {
        sh './output'
      }
    }
    stage('Test') {
      steps {
        echo 'deploy'
      }
    }
  }
  post {
    failure {
      error 'Pipeline failed'
    }
  }
}
