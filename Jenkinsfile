pipeline {
  agent {
      any
  }
  stages {
    stage('setup') {
      steps {
          sh '''
          echo "setup"
          '''
        }
    }
    stage('TF init') {
      steps {
          sh '''
          echo "init"
          echo $BRANCH_NAME
          '''
        }
    }
    stage('TF plan') {
      steps {
          sh '''
          echo "plan"
          echo $BRANCH_NAME
          '''
        }
    }
    stage('TF validate') {
      steps {
          sh '''
          echo "validate"
          echo $BRANCH_NAME
          '''
        }
    }
    stage('TF apply') {
      steps {
          sh '''
          echo "apply"
          echo $BRANCH_NAME
          '''
        }
    }
  }
}
