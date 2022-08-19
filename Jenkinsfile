pipeline {
   agent any
   parameters {
     string(name:'BRANCH_NAME',defaultValue:'master')
   }
stages {
		stage ('Checkout SCM') {
            when {
                expression { BRANCH_NAME ==  params.BRANCH_NAME}
            }
			steps {
				cleanWs()
                checkout scm
                sh "ls"
			}
		}
}
}
