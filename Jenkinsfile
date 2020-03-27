pipeline {
    agent{
        label maven
    }
    tools {
        jdk 'openjdk8'
        maven 'Maven'
        
}
    stages {
        stage ('Build') {
            steps {
                sh "mvn clean test"
            }
        }
    }
    
}
