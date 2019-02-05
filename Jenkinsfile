pipeline {
    agent any
    stages {
        stage('test') {
               steps {
                   script {
                       sh 'mvn clean test'
                    }                
                } 
            }
        stage('build') {
            steps {
                sh 'mvn clean install package'
                }
        }
        stage('MUnit Test Report') { 
            steps {
                script {
                    echo "Publish MUnit Test Report"
                    publishHTML(target:[allowMissing: false, alwaysLinkToLastBuild: false, keepAll: true, 
                    reportDir: 'MUnitTests', reportFiles: 'summary.html', reportName: 'MUnit Test Report', reportTitles: 'MUnit Test Coverage Report'])
                }
            }
        }
    }
}
