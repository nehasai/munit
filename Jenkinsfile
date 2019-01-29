pipeline
{
    agent any
    stages {
       
   stage('MUnit Test Report') {
       steps {
        script { 
       	publishHTML(target: [allowMissing: false, alwaysLinkToLastBuild: false, keepAll: true, reportDir: 'target/site/munit/coverage/MUnitTests', reportFiles: 'summary.html', reportName: 'MUnit Test Report', reportTitles: 'MUnit Test Coverage Report'])         
        }
       }
    }
    }
}
