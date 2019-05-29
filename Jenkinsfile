import jenkins.model.*

pipeline{
	   
	agent{
		label	"AKS"
	}
	options{
		skipDefaultCheckout()
		timestamps()
	}
	
	stages{
		
	stage('Source Checkout') {
			
		steps{
			cleanWs()
			script{
			checkout([$class: 'GitSCM', branches: [[name: '*/bitbucket']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: '864c9307-60a8-4204-b232-825d5a2c7e5b', url: 'git@github.com:jvenkat255/my-app-1.git']]])
			}
					
		}
	}
		
	stage('Source pull') {
			
		steps{
			
			script{
			git credentialsId: 'bit_bucket', url: 'https://vjagarlamudi1@bitbucket.org/medlineis/testrepo.git'
			}
					
		}
	  }
	
	}

}
