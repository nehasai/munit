pipeline
{
    agent any
    stages {
       
   stage('MUnit Test Report') {
        script {   	
       	echo "Publish MUnit Test report"
       	publishHTML(target: [allowMissing: false, alwaysLinkToLastBuild: false, keepAll: true, reportDir: 'MUnitTests', reportFiles: 'summary.html', reportName: 'MUnit Test Report', reportTitles: 'MUnit Test Coverage Report'])         
        }
    }
    }
}
