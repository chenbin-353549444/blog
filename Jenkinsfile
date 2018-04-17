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
    stage('post') {
      steps {
        mail(body: '${env.JOB_NAME} - Build # ${env.BUILD_NUMBER} - ${currentBuild.currentResult}: Check console output at ${env.BUILD_URL} to view the results.', subject: '${env.JOB_NAME} - Build # ${env.BUILD_NUMBER} - ${currentBuild.currentResult}!', to: '353549444@qq.com')
      }
    }
  }
}