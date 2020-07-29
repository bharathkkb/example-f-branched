pipeline {
  agent any
  stages {
    stage('setup') {
      steps {
          sh '''
          echo "setup"
          '''
        }
    }
    stage('TF plan-validate-all') {
        when {
                not {
                        anyOf {
                        branch 'dev'
                        branch 'prod'
                        branch 'nonprod'
                    }
                }
            }
      steps {
          sh '''
          echo "plan validate all"
          echo $BRANCH_NAME
          '''
        }
    }
    stage('TF init') {
        when {
                anyOf {
                    branch 'dev'
                    branch 'prod'
                    branch 'nonprod'
                }
            }
      steps {
          sh '''
          echo "init"
          echo $BRANCH_NAME
          '''
        }
    }
    stage('TF plan') {
        when {
                anyOf {
                    branch 'dev'
                    branch 'prod'
                    branch 'nonprod'
                }
            }
      steps {
          sh '''
          echo "plan"
          echo $BRANCH_NAME
          '''
        }
    }
    stage('TF validate') {
        when {
                anyOf {
                    branch 'dev'
                    branch 'prod'
                    branch 'nonprod'
                }
            }
      steps {
          sh '''
          echo "validate"
          echo $BRANCH_NAME
          '''
        }
    }
    stage('TF apply') {
        when {
                anyOf {
                    branch 'dev'
                    branch 'prod'
                    branch 'nonprod'
                }
            }
      steps {
          sh '''
          echo "apply"
          echo $BRANCH_NAME
          '''
        }
    }
  }
}
