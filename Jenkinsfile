pipeline {
  agent {
    docker {
      image 'maven:3-alpine'
      args '-v /root/.m2/repository:/root/.m2/repository'
    }

  }
  stages {
    stage('SCM') {
      steps {
        echo 'hello world'
      }
    }

    stage('build') {
      steps {
        sh 'mvn clean install'
      }
    }

  }
  environment {
    scm = 'master'
  }
}