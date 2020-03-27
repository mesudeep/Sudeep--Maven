pipeline {
    agent{
        label 'maven'
    }
    tools {
        maven 'Maven'
        jdk 'openjdk8'
}
    stages {
        stege ('Build'){
            steps {
                sh "mvn clean compile"
            }
        }
    }
}
