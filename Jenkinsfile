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
				sh 'scp target/java-hello-world.war tomcat@18.233.170.154:/opt/tomcat/webapps/'
				}
			}
    
	    }
    }
