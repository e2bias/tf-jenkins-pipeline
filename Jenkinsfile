pipeline {
  agent any
  stages {
    stage ('build') {
      steps{
        sh 'echo "BUILD STAGE"'
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
