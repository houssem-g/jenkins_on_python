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
        sh ' docker pull maven:3.6.3-jdk-8-alpine'
        sh 'mvn clean compile'
      }
    }

  }
  environment {
    scm = 'master'
  }
}