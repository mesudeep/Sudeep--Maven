pipeline {
    agent {
        label 'master'
    }  
    tools {
        jdk 'openjdk8'
        maven '363'
    } 
    stages {
        stage ('Build') {
            steps {
                sh "mvn clean compile"
            }
        }
    }
    
}
