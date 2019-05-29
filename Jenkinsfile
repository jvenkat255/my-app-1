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
				checkout([$class: 'GitSCM', branches: [[name: "${params.ciGitCommit}"]], 
						doGenerateSubmoduleConfigurations: false, 
						extensions: [], 
						submoduleCfg: [], 
						userRemoteConfigs: [[credentialsId: 'jvenkat255', url: 'https://github.com/jvenkat255/my-app-1.git']]])
					}
					
				}
			}
		}
}
