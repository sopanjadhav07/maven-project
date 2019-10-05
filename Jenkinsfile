pipeline {
     agent any
     stages {
          stage("Validate code") 
		  {
		  
              steps {
		      withMaven(maven: 'Local_Maven'){
			  
                    sh "mvn compile"
               }
          }
		  }
		  }
}
		  
