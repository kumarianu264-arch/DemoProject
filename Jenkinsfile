pipeline {
    agent any
    triggers {
        cron ('H/2 * * * *')
    }
    stages {
        stage ('checkout') {
            steps {
                git url: 'https://github.com/kumarianu264-arch/DemoProject.git',
                git branch : 'main',
                credentialsId: 'apps_github'
            }
        }
    }           

    stage ('build') {
        steps {
            echo "building"

        }
    }
}                       