pipeline{
    tools{
        mvn 'maven-3'
    }    
    agent{
	label "AKS"
	}
     
stages{
    stage('SCM Checkout'){
     git 'https://github.com/javahometech/my-app'
   }
    stage('Mvn Package'){
	    steps {
		    bat 'mvn clean package'
    		}
	     }
	}
}
