pipeline {
  agent any
  parameters {
    gitParameter branchFilter: 'origin/(.*)', defaultValue: 'main', name: 'BRANCH', type: 'PT_BRANCH'
  }
  stages {
    stage('checkout') {
      steps {
        git branch: "${params.BRANCH}", url: 'https://github.com/Santy2703/jenkins-test'
      }
    }
  }
}
