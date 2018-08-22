#!groovy

node {
	   
	stage('Checkout'){

          checkout scm
       }
	
	 stage('Sonar') {
                    //add stage sonar
                   // sh 'mvn sonar:sonar'
                }

       stage('BuildArtifact'){

         // sh 'mvn install'
	       
	       sh 'mvn deploy'
       }
	  stage('Tomcat')
	{
		sshagent(['549f4f30-c230-4392-bb0a-23cddce7d60b']) {
            sh 'scp -o StrictHostKeyChecking=no target/*.war ec2-user@172.31.27.69:/opt/apache-tomcat-8.0.53/webapps'
    // some block
}

	}
     
       
}
