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
         
{		  
stage("SonarQube analysis and install") {
     steps {
	 withSonarQubeEnv ('sonar'){
	 withMaven(maven: 'Local_Maven'){
          sh "mvn install sonar:sonar"
     }
}
}

}
}
}
