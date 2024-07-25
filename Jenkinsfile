pipeline {
    agent {
        label 'Agent1'
    }
    
    tools {
       maven 'Maven3.9.8'
    }

    stages {
        stage('Build') {
            steps {
                sh 'env | grep -e PATH -e JAVA_HOME'
                sh 'which java'
                sh 'java --version'
                
                sh 'mvn -B -DskipTests clean package'
            }
        }
        stage('Test') {
            steps {
                // Execute Maven unit tests
                sh 'mvn test'
            }
            // Executes after the steps are completed
            post {
                // always means it will continue regardless of success or failure of the steps
                always {
                    junit 'target/surefire-reports/*.xml'
                }
            }
        }
    }
}
