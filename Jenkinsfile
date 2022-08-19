pipeline {
   agent any
   parameters {
     string(name:'BRANCH_NAME',defaultValue:'master')
   }
stages {
	stage ('Checkout Xyz') {
 
		steps {
			git branch: 'params.BRANCH_NAME', url: 'https://github.com/Santy2703/jenkins-test'	
		}
	}
   }
}
