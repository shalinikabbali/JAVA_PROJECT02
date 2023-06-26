pipeline {
    agent any	
    stages {
        stage('Build') {
            steps {
                // Build the project and generate the WAR file
                sh 'mvn clean install'
            }
      	  }
	    }
    }
