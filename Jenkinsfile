pipeline
{
    agent any
    stages {
        stage(reports)
{
    steps {
        sh 'mkdir coverage'
        publishHTML([allowMissing: false, alwaysLinkToLastBuild: false, keepAll: true, reportDir: 'target/site/munit/coverage', reportFiles: 'summary.html', reportName: 'HTML Report', reportTitles: ''])
    }
}
    }
}
