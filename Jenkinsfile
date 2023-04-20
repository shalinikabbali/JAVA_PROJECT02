pipeline {
    stages {
        stage('Build') {
            agent { Label 'slave3' }
            steps {
                // Build the project and generate the WAR file
                sh 'mvn clean package'
            }
        }
    }
}
