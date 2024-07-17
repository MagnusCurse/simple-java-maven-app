pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                // This sh step runs the Maven command to cleanly build your Java application without running any tests.
                sh 'mvn -B -DskipTests clean package'
            }
        }
    }
}