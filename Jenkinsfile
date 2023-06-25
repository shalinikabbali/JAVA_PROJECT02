pipeline {
    agent {label 'agent01'}
    stages {
        stage('Build') {
            steps {
                // Build the project and generate the WAR file
                sh 'mvn clean install'
            }
      	  }
	    }
    }
