node{
	        stage('SCM checkout')
			        {git 'https://github.com/sopanjadhav07/maven-project/'}
	}

node{
	
	 stage('package'){
					       sh 'mvn clean package'
						   }
		}
node{
     stage('docker image build')
	 {
		 sh 'docker rmi -f sopanjadhav/spring-boot-mongo'
                sh 'docker build -t sopanjadhav/spring-boot-mongo .'
			}
			}

node{
stage('Docker push image')
     {withCredentials([string(credentialsId: 'dockerHubaccount', variable: 'dockerHubaccount')]) 
      {
    sh "docker login -u sopanjadhav -p $dockerHubaccount"
}

sh "docker push sopanjadhav/spring-boot-mongo"
}
}

