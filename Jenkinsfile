  	def latestTag 
pipeline {
  

    agent any 	
	environment {
	 	PROJECT_ID = 'cr-lab-sshastri-1408204213'
                CLUSTER_NAME = 'cluster-1'
                LOCATION = 'us-central1-c'
                CREDENTIALS_ID = 'gcpk8creds'	


	} 

    stages {	
	   stage('Checkout') {            
		steps {
                       echo 'Pulling...' + env.GIT_BRANCH
                   script {
             latestTag = sh(returnStdout:  true, script: "git tag --sort=-creatordate | head -n 1").trim()
             env.BUILD_VERSION = latestTag
             echo "env-BUILD_VERSION"
             echo "${env.BUILD_VERSION}"
            }	
               //checkout scm
		}	
           }

	  
	   } 
    }
