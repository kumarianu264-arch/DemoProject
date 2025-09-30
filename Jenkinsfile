pipeline {
    agent any
    
    triggers {
        cron('H/2 * * * *')
        githubpush()
    }  

    stages {
        stage('checkout')
        steps {
              git url:'https://github.com/kumarianu264-arch/DemoProject.git',
              branch:'main',
              credentialsId:'apps_github'

        }
    } 

    stage('A') {
        steps {
            echo "This is stage A"
        }
    }

    stage('B') {
        steps {
            echo "This is for testing"
        }
    } 
}
           
