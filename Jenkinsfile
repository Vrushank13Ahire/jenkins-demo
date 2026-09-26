pipeline {
  agent any 
  stages {
    stage ('Build') {
      steps {
        echo "Building"
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
