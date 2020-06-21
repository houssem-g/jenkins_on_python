pipeline {
  agent any
  stages {
    stage('SCM') {
      steps {
        echo 'hello world'
      }
    }

    stage('build') {
      agent any
      steps {
        sh 'docker pull maven:3.6.0-jdk-8-alpine'
        sh 'mvn clean install'
      }
    }

  }
  environment {
    scm = 'master'
  }
}