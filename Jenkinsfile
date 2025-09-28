pipeline {
    agent any

    triggers {
        // Trigger build on every push from GitHub webhook
        githubPush()
    }

    stages {
        stage('Checkout') {
            steps {
                // Replace with your repo URL
                git branch: 'main', url: 'https://github.com/kumarianu264-arch/DemoProject.git',
                credentialsId: 'anugit-creds'
            }
        }

        stage('Build with Maven') {
            steps {
                // Clean and build using Maven
                sh 'mvn clean install'
            }
        }
    }
}
