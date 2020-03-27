pipeline {
    agent {
        label 'maven'
    }  
    tools {
        jdk 'openjdk8'
        maven '363'
    } 
    stages {
        stage ('Build') {
            steps {
                sh "mvn clean test"
            }
        }
    }
    
}
