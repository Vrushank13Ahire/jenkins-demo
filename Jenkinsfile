pipeline{
  agent any
  environment {
    APP_ENV = 'test'
  }
  stages {
    stage('Checkout') {
      steps {
        checkout scm
      }
    }
    stage ('Build'){
      steps {
        sh 'echo Building'
      }
    }
    stage ('Test'){
      steps {
        sh 'echo Testing'
      }
    }
  }

    post {
      success {
        echo 'All steps passed'
      }
      failure {
        echo 'Failed'
      }
    }
  }
