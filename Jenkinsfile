pipeline {
  agent any
  stages {
    stage('Hello'){
      step{
        echo "Hello from Jenkins"
        sh 'echo This is the real shell cmd'
        sh 'pwd'
        sh 'ls -la'
      }
    }
  }
}
