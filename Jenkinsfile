pipeline {
    agent {Label 'slave3'}
    stages {
        stage('Build') {
            steps {
                // Build the project and generate the WAR file
                sh 'mvn clean package'
            }
        }
    }
}
