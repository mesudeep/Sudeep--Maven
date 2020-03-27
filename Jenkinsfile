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
        stage('Deploy') {
            steps {
                sshagent(['sudeeptarget']) {
                  sh "scp  -o StrictHostKeyChecking=no target/my-app-1-RELEASE.jar ec2-user@172-31-42-156:/home/ec2-user"
}

            }
        }
    }
    
}
