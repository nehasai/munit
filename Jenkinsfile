pipeline
{
    agent any
    stages {
       
   stage('MUnit Test Report') {
       steps {
        script { 
             echo "Copy files started"
           	fileOperations([
	   	    folderCreateOperation(
		            folderPath: 'MUnitTests'),
	   	    folderCopyOperation(
	   	            sourceFolderPath: 'target/munit-reports/coverage',
	   	            destinationFolderPath: 'MUnitTests')
            	])
            	echo "Copy files ended"
       	publishHTML(target: [allowMissing: false, alwaysLinkToLastBuild: false, keepAll: true, reportDir: 'target/munit-reports/coverage', reportFiles: 'summary.html', reportName: 'MUnit Test Report', reportTitles: 'MUnit Test Coverage Report'])         
        }
       }
    }
    }
}
