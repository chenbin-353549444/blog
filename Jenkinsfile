pipeline {
  agent any
  stages {
    stage('test1') {
      parallel {
        stage('test') {
          steps {
            echo 'test1'
          }
        }
        stage('test2') {
          steps {
            echo 'test2'
          }
        }
      }
    }
    stage('success') {
      steps {
        echo 'success'
      }
    }
  }
}