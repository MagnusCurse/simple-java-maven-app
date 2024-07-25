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
    }
}
