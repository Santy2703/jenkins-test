pipeline {
   agent any
   parameters {
     string(name:'BRANCH_NAME',defaultValue:'master')
   }
   stages {
    stage('Checkout') {
      steps {
        script {
           // The below will clone your repo and will be checked out to master branch by default.
           // url: 'https://github.com/Santy2703/jenkins-test'
           // Do a ls -lart to view all the files are cloned. It will be clonned. This is just for you to be sure about it.
           
           sh "ls" 
           sh "git checkout params.BRANCH_NAME"
           sh "ls"
          }
       }
    }
  }
}
