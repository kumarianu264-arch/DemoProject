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
stage('Build with Maven') {
            steps {
                // If pom.xml is in a subfolder, e.g. 'my-app'
                dir('my-app') {
                    sh 'mvn clean install'
                }
            }    