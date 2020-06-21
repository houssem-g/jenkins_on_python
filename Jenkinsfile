pipeline {
  agent {
    docker {
      image 'maven:3.6.0-jdk-8-alpine'
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
      agent {
        docker {
          image 'maven:3.6.0-jdk-8-alpine'
          args '-v /root/.m2/repository:/root/.m2/repository'
        }

      }
      steps {
        sh 'mvn clean install'
      }
    }

  }
  environment {
    scm = 'master'
  }
}