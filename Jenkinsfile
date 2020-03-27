pipeline {
    agent{
        label none
    }
    tools {
        jdk 'openjdk8'
        maven 'Maven'
        
}
    stages {
        stage ('Build') {
            steps {
                sh "mvn clean compile"
            }
        }
    }
    
}
