  pipeline{
	 tools{
        mvn 'maven-3'
    }    
	agent{
		label	"AKS"
	}
     
   stage('SCM Checkout'){
     git 'https://github.com/javahometech/my-app'
   }
    stage('Mvn Package'){
      sh 'mvn clean package'
    }
}


