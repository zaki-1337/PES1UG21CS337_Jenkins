pipeline {
  agent any

  stages {
    
    stage('Build') {
      steps {
        build 'PES1UG21CS337-1'
        sh 'g++ hello2.cpp -o hello2'
      }
    }
    stage('Test') {
      steps {
        sh './hello2'
      }
    }
    stage('Deploy') {
      steps {
        echo 'Deploy'
      }
    }
  }

  post {
    failure {
      echo 'Pipeline failed!'
    }
  }
}
