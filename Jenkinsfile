pipeline {
    agent {label 'agent01'}
	parameters {
  string defaultValue: 'dev', name: 'ENV'
                 }
    stages {
        stage('Build') {
            steps {
                // Build the project and generate the WAR file
                sh 'mvn clean install'
            }
      	  }
	    }
    }
