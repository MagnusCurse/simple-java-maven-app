pipeline {
    agent any
     tools {
       jdk 'Java17'
       maven 'Maven 3.9.8'
    }
    stages {
        stage('Build') {
            steps {
                // This sh step runs the Maven command to cleanly build your Java application without running any tests.
                sh 'mvn -B -DskipTests clean package'
            }
        }
    }
}