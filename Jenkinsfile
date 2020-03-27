pipeline {
    agent {
        label 'maven'
    }  
    tools {
        jdk 'openjdk8'
        maven '363'
    } 
    stages {
        stage ('Test') {
            steps {
                sh "mvn clean test"
            }
        }
        stage('Packaging'){
            steps {
                sh "mvn package"
            }
        }
    }
    
}
