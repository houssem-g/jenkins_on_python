pipeline {
  agent any
  stages {
    stage('SCM') {
      steps {
        echo 'hello world'
      }
    }

    stage('compile') {
      agent any
      steps {
        sh 'docker pull maven:3.6.0-jdk-8-alpine'
        sh './mvnw clean install'
      }
    }

  }
  environment {
    scm = 'master'
  }
}