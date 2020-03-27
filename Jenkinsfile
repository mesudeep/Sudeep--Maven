pipeline {
    agent  maven
    tools {
        jdk 'openjdk8'
        maven 'maven3.6.3'
        
    stages {
        stage ('Build') {
            steps {
                sh "mvn clean test"
            }
        }
    }
    
}
