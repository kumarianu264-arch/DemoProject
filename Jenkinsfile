pipeline {
    agent any
    
    triggers {
        cron('H/2 * * * *')   // Run every 2 minutes
        githubPush()          // Correct camelCase trigger
    }

    stages {
        stage('Checkout') {
            steps {
                git url: 'https://github.com/kumarianu264-arch/DemoProject.git',
                    branch: 'main',
                    credentialsId: 'apps_github'
            }
        }

        stage('A') {
            steps {
                echo "Running Stage A"
            }
        }

        stage('B') {
            steps {
                echo "This is for testing"
            }
        }
    }
}
