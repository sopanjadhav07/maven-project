pipeline
{

 agent any                                                                      
{ 
	
stage "scm checkout" {
git 'https://github.com/sopanjadhav07/maven-project.git'	
}

stage "code test" {
withMaven(maven: 'LocalMaven') {
     sh 'mvn test'
}	 
}
}	
} 
