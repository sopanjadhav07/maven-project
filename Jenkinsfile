pipeline{

agent any                                                                      

{
	
stage ('scm checkout')
{
git 'https://github.com/sopanjadhav07/maven-project.git'	
}

}
	
stage('code test') 
{

steps 
{
withMaven(maven: 'Local_Maven') 
{
     sh 'mvn test'
}	 
}
}	
}
