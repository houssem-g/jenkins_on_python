pipeline {
  agent any
  stages {
    stage('SCM') {
      steps {
        echo 'hello world'
      }
    }

    stage('compile') {
      agent {
        docker {
          image 'maven:3.6.3-jdk-8'
          args '-v /home/.m2/repository:/root/.m2/repository'
          reuseNode true
        }

      }
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