pipeline {
    agent  
    label maven
    tools {
        jdk 'openjdk8'
        maven 'maven3.6.3'
    }
        
    stages {
        stage ('Test') {
            steps {
                sh "mvn clean test"
            }
        }
    }
    
}
