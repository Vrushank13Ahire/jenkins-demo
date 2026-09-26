pipeline {
  agent any
  parameters{
    choice( name: 'ENVIRONMENT' , choices: ['staging', 'production'], description: 'Target')
  }
  stages {
    stage ('Checkout SCM'){
      steps {
        checkout scm
      }
    }
    stage ('Test') {
      parallel {
        stage('Unit') { steps { sh 'echo Unit Testing'}}
        stage('Integration') { steps { sh 'echo Integration Testing'}}
      }
    }
    stage('Approve'){
      steps {
        input message :"Deploy to production"
      }
    }
    stage('Deploy') {
      steps {
        sh "echo Deploying to ${params.ENVIRONMENT}" 
      }
    }
  }


post {
  success {
    echo "Pipeline success"
  }
  failure {
    echo "pipeline Failed"
  }
}
}
