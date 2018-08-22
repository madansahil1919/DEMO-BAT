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
			 sh 'scp -o StrictHostKeyChecking=no **/*.war ec2-user@172.31.27.69:/opt/wildfly-13.0.0.Final/standalone/deployments'
    // some block
}

	}
     
       
}
