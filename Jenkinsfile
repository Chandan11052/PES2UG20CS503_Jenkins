pipeline {
  agent any
  stages {
    stage('Build'){
      steps {
        sh 'g++ workjhvding.cpp'
        build job: "PES2UG20CS503-1", wait: true
      }
    }
    stage('Test'){
      steps{
        sh './a.out'
      }
    }
  }
  post {
    failure {
      echo 'pipeline failed'
    }
  }
}
