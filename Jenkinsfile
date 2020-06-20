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
        sh 'docker inspect -f .maven:3.6.0-jdk-8-alpine'
      }
    }

  }
  environment {
    scm = 'master'
  }
}