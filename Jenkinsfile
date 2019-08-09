pipeline {
  agent any
  stages {
    stage('unit tests') {
      steps {
        sh 'echo \'Running unit tests...\''
      }
    }
    stage('integration') {
      parallel {
        stage('integration') {
          steps {
            sh 'echo \'Running integration\''
          }
        }
        stage('ui') {
          steps {
            sh 'test'
          }
        }
      }
    }
    stage('deploy') {
      steps {
        sh 'echo \'deploy\''
      }
    }
  }
}