pipeline {
	agent any
	parameters {
	    choice(choices: ['dev', 'qa', 'prod'], description: 'Environment', name: 'ENVIRONMENT')
		string(name: 'DOCKER_TAG', defaultValue: 'LATEST', description: 'Docker image tag to be deployed. "LATEST" deploys the newest image.' )
	}
	stages {
		stage('Checkout SCM') {
			steps {
				script {
				 env.ENV = params.ENVIRONMENT
				 env.cpu_dev_limits = 10
				 env.cpu_qa_limits  = 20
				 sh 'printenv'
				}
			}
		}
		stage('Checkout SCM 2') {
			steps {
				script {
				contentReplace(configs: [fileContentReplaceConfig(configs: [
						fileContentReplaceItemConfig(matchCount: 0, replace: params.ENVIRONMENT, search: '@ENVIRONMENT')
						

				 	],                                                                                                                                                                  
					
                                        fileEncoding: 'UTF-8', filePath: "${WORKSPACE}/deployment.yml")])
				}
			}
		}
	}
			
}
