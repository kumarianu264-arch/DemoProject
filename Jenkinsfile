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
                credentialsId: 'apps_github'
            }
        }

        stage('Build with Maven') {
            steps {
                 stage('Build with Maven') {
            steps {
                dir('some-subdir') { // 👈 change this if pom.xml is in a subfolder
                    sh 'mvn clean install'
                // Clean and build using Maven
                sh 'mvn clean install'
            }
        }
    }
}
