pipeline {
     agent any
     stages {
          stage("Validate code") 
		  {
		  
              steps {
			  withMaven(maven: 'Local_Maven'){
				  agent 'label'
			  
                    sh "mvn compile"
               }
          }
		  }
		  }
		  }
