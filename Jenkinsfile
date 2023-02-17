pipeline {
  agent any

  stages {
    stage('Build') {
      steps {
        sh 'g++ -o cs168 cs168.cpp'
        build job: 'PES1UG20CS168-1'
        echo "BUILD successful"
      }
    }
    stage('Test') {
      steps {
        sh './cs168'
        echo "TEST successful"
      }
    }
    stage('Deploy') {
      steps {
        sh 'echo "Deployment stage"'
        //sh 'exit 1'
        echo "DEPLOY successful"
      }
    }
  }

  post {
    failure {
     echo 'Pipeline failed.'
    }
  }
}
