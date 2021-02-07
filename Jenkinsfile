pipeline {
  agent any
  environment{
    GOOGLE_CREDENTIALS = credentials('gcp-terraform-svc-key')
  }
  stages {
    stage ('build') {
      steps{
        sh 'echo "BUILD STAGE"'
        sh 'echo ${GOOGLE_APPLICATION_CREDENTIALS}'
      }
    }
    stage ('test') {
      steps{
        sh 'echo "TEST"'
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
