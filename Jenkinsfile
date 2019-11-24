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
                sh 'docker build -t sopanjadhav/myrepo:1.0.0 .'
			}
			}

node{
stage('Docker push image')
     {withCredentials([usernameColonPassword(credentialsId: 'dockerHubaccount', variable: 'dockerHubaccount')])
	 {
    sh "docker login -u sopanjadhav -p $Dockerhubpassword"
}

sh "docker push sopanjadhav/myrepo:1.0.0"

}
}
