pipeline {
    agent any

    triggers {
        githubPush()
    }

    stages {
        stage('Checkout') {
            steps {
                git url: 'https://github.com/kumarianu264-arch/DemoProject.git', branch: 'main' , credentialsId: 'apps_github'
            }
        }

        stage('Build with Maven') {
            steps {
                sh 'mvn clean install'
            }
        }
        
    }
}
stage('Debug Workspace') {
    steps {
        sh 'pwd'
        sh 'ls -la'
        sh 'find . -name "pom.xml"'
    }
}