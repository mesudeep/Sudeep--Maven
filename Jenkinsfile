pipeline {
    agent{
        label 'any'
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
    post {
        success {
            echo "Success"
            
        }
        failure {
            echo "Failed"
        }
        always {
            deleteDir()
        }
    }
}
