pipeline {
  agent any
  stages {
    stage('SCM') {
      steps {
        echo 'hello world'
      }
    }

    stage('test') {
      steps {
        echo 'test'
      }
    }

  }
  environment {
    scm = 'master'
  }
}