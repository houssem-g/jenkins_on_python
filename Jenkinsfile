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
          image 'maven:3.6.0-jdk-8-alpine'
        }

      }
      steps {
        sh 'mvn clean compile'
      }
    }

  }
  environment {
    scm = 'master'
  }
}