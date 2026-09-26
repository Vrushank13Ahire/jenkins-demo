pipeline {
  agent any 
  stages {
    stage ('Build') {
      steps {
        echo "Building"
      }
    }
    stage ('Approve'){
      steps{
        input message: "Do u wan tto proceed?"
      }
    }
    stage ('Test'){
      parallel {
        stage('Unit'){
          steps {
            echo "Unit testing"
          }
        }
        stage ('Itegration'){
          steps {
            echo "Integration Testing"
          }
        }
      }
    }
  }
}
