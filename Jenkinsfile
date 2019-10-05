pipeline {
     agent any
     stages {
          stage("Validate code") {
		  agent 'label'{
		  
              steps {
			  withMaven(maven: 'Local_Maven'){
			  
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
