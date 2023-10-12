pipeline {
    agent any

    stages {
        stage('Compile') {
            steps {
                echo 'Compile'
                bat  'atlas-compile'
            }
        }
       stage('Package') {
            steps {
                echo 'Build'
                bat  'atlas-package'
            }
        }
       stage('Deploy') {
            steps {
                echo 'Deploy'
                bat 'atlas-install-plugin --username rahulravindra --password Q5-9k195 --server 172.16.2.45 --http-port 8080 --plugin-key com.atlassian.jira.jira-api --context-path ""'
            }
        }
    }
}