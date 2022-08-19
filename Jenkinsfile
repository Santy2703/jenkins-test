pipeline {
  agent any
  parameters {
    gitParameter branchFilter: 'origin/(.*)', defaultValue: 'main', name: 'BRANCH', type: 'PT_BRANCH'
  }
stages {
		stage ('Checkout SCM') {
            when {
                expression { BRANCH_NAME == ${params.BRANCH} }
            }
			steps {
				cleanWs()
                checkout scm
			}
		}
}
}
