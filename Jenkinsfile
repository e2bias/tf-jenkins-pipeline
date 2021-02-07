pipeline {
  agent any
  environment{
    GOOGLE_APPLICATION_CREDENTIALS = credentials('gcp-terraform-svc-key')
  }
  stages {
    stage ('build') {
      steps{
        sh 'echo "BUILD STAGE"'
        checkout scm
      }
    }
    stage ('test') {
      steps{
        container('terraform'){
          sh 'echo "TEST"'
          sh 'terraform version'
          sh 'terraform init'
        }
      }
    }
    stage ('approval') {
      steps{
        sh 'echo "APPROVAL"'
      }
    }
    stage ('deploy') {
      steps{
        sh 'echo "DEPLOY"'
      }
    }
  }
}
