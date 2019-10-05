pipeline {
     agent any
     stages {
          stage("Validate code") 
		  {
		  
              steps {
			  withMaven(maven: 'Local_Maven'){
				  agent 'java'
			  
                    sh "mvn compile"
               }
          }
		  }
		  }
		  }
