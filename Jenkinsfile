pipeline {
     agent any
		stages {
			{
				stage ('scm checkout')
					{
						git 'https://github.com/sopanjadhav07/maven-project.git'	
					}
			}
		{	
          stage('Validate code') 
		  	{
				steps {
					withMaven(maven: 'Local_Maven'){
							sh "mvn clean compile"
							}
					}
			}
		}
	}
}
