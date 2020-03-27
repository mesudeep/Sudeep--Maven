pipeline {
    agent{
        label 'maven'
    }
    tools {
        maven 'Maven'
        jdk 'openjdk8'
}
    stages {
        stage ('Build') {
            steps {
                sh "mvn clean compile"
            }
        }
    }
}
