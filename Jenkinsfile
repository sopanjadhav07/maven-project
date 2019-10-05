pipeline {
     agent any
     stages {
	 agent java
          stage('Validate code') 
		  
		  {
		  
              steps {
			  withMaven(maven: 'Local_Maven'){
				  
			  
                    sh "mvn compile"
               }
          }
		  }
		  }
		  }
