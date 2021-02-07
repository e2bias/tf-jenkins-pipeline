pipeline {
  agent any
  environment {
    GOOGLE_APPLICATION_CREDENTIALS = credentials('gcp-terraform-svc-key')
  }
  stages {
    stage ('build') {
      steps {
        sh 'echo "BUILD STAGE"'
        checkout scm
        sh 'export ${GOOGLE_APPLICATION_CREDENTIALS}'
        sh 'printenv | grep GOOGLE' 
      }
    }
    stage ('test') {
      steps {
        container('terraform') {
          sh 'echo "TEST"'
          sh 'terraform version'
        }
      }
    }
    stage ('approval') {
      steps {
        sh 'echo "APPROVAL"'
      }
    }
    stage ('deploy') {
      steps {
        sh 'echo "DEPLOY"'
      }
    }
  }
}
