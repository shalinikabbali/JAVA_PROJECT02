pipeline {
    agent {label 'slave3'}
    stages {
        stage('Build') {
            steps {
                // Build the project and generate the WAR file
                sh 'mvn clean install'
            }
      	  }
	    stage('Deploy to tomcat') {
			steps {
				sshagent(['Deploy-user']) {
                    sh "scp -o StrictHostKeyChecking=no /home/ec2-user/build03/workspace/pipeline-for-java/target/java-hello-world.war ec2-user@18.233.170.154:/opt/tomcat/webapps"
					
                       }
				}
			}
    
	    }
    }
