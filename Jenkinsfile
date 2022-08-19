pipeline {
  agent any
  parameters {
    gitParameter branchFilter: 'origin/(.*)', defaultValue: 'main', name: 'BRANCH', type: 'PT_BRANCH'
  }
  stages {
    stage('checkout') {
      steps {
        git branch: "${params.BRANCH}"
      }
    }
  }
}
