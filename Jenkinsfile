pipeline
{
    agent any
    stages {
       
   stage('MUnit Test Report') {
       steps {
        script {   
		sh 'mvn clean test'
           	fileOperations([
	   	    folderCreateOperation(
		            folderPath: 'MUnitTests'),
	   	    folderCopyOperation(
	   	            sourceFolderPath: 'target/munit-reports/coverage',
	   	            destinationFolderPath: 'MUnitTests')
            	])
       	publishHTML(target: [allowMissing: false, alwaysLinkToLastBuild: false, keepAll: true, reportDir: 'MUnitTests', reportFiles: 'summary.html', reportName: 'MUnit Test Report', reportTitles: 'MUnit Test Coverage Report'])         
        }
       }
    }
    }
}
