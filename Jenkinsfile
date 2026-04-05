pipeline {
    agent any

    stages {
        

        stage('Build') {
            steps {
                bat 'mvn clean compile'
            }
        }

        stage('Test') {
            steps {
                bat 'mvn test'
            }
        }

        stage('Report') {
            steps {
                publishHTML([
                    reportDir: 'target',
                    reportFiles: 'extent-report.html',
                    reportName: 'Test Report'
                ])
            }
        }
    }
}
