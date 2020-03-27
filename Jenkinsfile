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
                sh "mvn clean test surefire-report:report-only"
                publishHTML([allowMissing: true, alwaysLinkToLastBuild: false, keepAll: false, reportDir: '/target/site', reportFiles: 'surefire-index.html', reportName: 'HTML Report', reportTitles: ''])
            }
        }
        stage('Packaging'){
            steps {
                sh "mvn package -DskipTests=true"
            }
        }
    }
    
}
