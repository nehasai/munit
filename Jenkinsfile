pipeline
{
    stages {
        stage(reports)
{
    steps {
        publishHTML([allowMissing: false, alwaysLinkToLastBuild: false, keepAll: true, reportDir: 'coverage', reportFiles: 'summary.html', reportName: 'HTML Report', reportTitles: ''])
    }
}
    }
}
