pipeline {
    agent { label 'maven' }   // Run only on nodes labeled "maven"
    
    triggers {
        cron('H * * * *')     // Run every 1 hour
        githubPush()          // Also trigger on GitHub push
    }

    stages {
        stage('Checkout') {
            steps {
                git url: 'https://github.com/kumarianu264-arch/DemoProject.git',
                    branch: 'main',
                    credentialsId: 'apps_github'
            }
        }

        stage('Build') {
            steps {
                sh 'mvn clean install'   // Run Maven build
            }
        }

        stage('Test') {
            steps {
                sh 'mvn test'            // Run Maven tests
            }
        }
    }
}
