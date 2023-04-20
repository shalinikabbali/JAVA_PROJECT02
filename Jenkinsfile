pipeline {
    agent {label 'slave3'}
    stages {
        stage('Build') {
            steps {
                // Build the project and generate the WAR file
                sh 'mvn clean package'
            }
      	  }
	    stage('Deploy to tomcat') {
			steps {
				sh 'scp target/java-hello-world.war ec2-user@172.31.81.164:/opt/tomcat/webapps/'
				sh 'ssh tomcat@172.31.81.164 "tomcatup"'
                                sh 'ssh tomcat@172.31.81.164 "tomcatdown"'
				}
			}
    
	    }
    }
