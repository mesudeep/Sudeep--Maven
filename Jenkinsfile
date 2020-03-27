pipeline {
    agent{
        label maven
    }
    tools {
        jdk 'openjdk8'
        maven 'maven'
        
}
    stages {
        stage ('Build') {
            steps {
                sh "mvn clean test"
            }
        }
    }
    
}
