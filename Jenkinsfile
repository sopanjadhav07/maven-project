pipeline {
     agent any
     stages {
	
          stage('Validate code') 
		  
		  {
		  
              steps {
			  withMaven(maven: 'Local_Maven'){
				  agent {label 'java'}
		          sh "mvn clean compile"
               }
          }
		  }
		  }
		  }
		  
