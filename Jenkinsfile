pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        build 'PES2UG21CS070_1'
        sh 'cd main \ng++ main.cpp -o output'
      }
    }
    stage('Test') {
      steps {
        sh './main/output'
      }
    }
    stage('Deploy') {
      steps {
        echo 'deploy'
      }
    }
  }
  post{
    failure{
      error 'Pipeline failed'
    }
  }
}
