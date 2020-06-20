pipeline {
  agent any
  stages {
    stage('SCM') {
      steps {
        echo 'hello world'
      }
    }

    stage('compile') {
      steps {
        sh 'docker pull maven:3.6.0-jdk-8-alpine'
        sh 'docker inspect -f . maven:3.6.0-jdk-8-alpine'
      }
    }

  }
  environment {
    scm = 'master'
  }
}