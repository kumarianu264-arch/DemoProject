pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git url: 'https://github.com/kumarianu264-arch/DemoProject.git', branch: 'main', credentialsId:apps_github
            }
        }
        stage('Build') {
            steps {
                sh 'ls -al'   // 👈 check files in workspace
                sh 'mvn clean install'
            }
        }
    }
}
