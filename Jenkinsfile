pipeline {
    agent any

    triggers {
        cron('H/2 * * * *')
        githubpush()
    }

    stages{
        stage('checkout')
        steps {
            git url: 'https://github.com/kumarianu264-arch/DemoProject.git',
            branch: 'main',
            credentialsID:'apps_github'
        }
    }

    stage('A') {
        steps {
            echo "testing"
        }
    }

    stage('B') {
        steps {
            echo "Building"
        }
    }
}            

