pipeline{

agent any                                                                      

stages
{
	stage ('scm checkout')
{
git 'https://github.com/sopanjadhav07/maven-project.git'	
}
}

{
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

{
stage('code package') 
{

steps 
{
withMaven(maven: 'Local_Maven') 
{
     sh 'mvn package'
}
}
} 
}


{
stage('code deploy') 
{

steps 
{
withMaven(maven: 'Local_Maven') 
{
     sh 'mvn deploy'
}
}
}
}

{
stage ('deploy to tomcat'){

steps {
  sshagent (['172.31.39.232']) {
    sh 'scp -o StrictHostKeyChecking=no */target/*.war ec2-user@172.31.39.232:/var/lib/tomcat/webapps'
  }
}
}
}

{
stage ('Sonarqube dashboard data')

steps {
     withSonarQubeEnv(sonar: 'sonar') {
	 sh 'mvn clean install sonar:sonar'
    
}
}
}
}
