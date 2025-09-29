pipeline {
    agent any 
    
    triggers {
        pollSCM('H/2 * * * *')
        cron('H/15 * * * 1-5')
        githubPush()
    }

    stages {
        stage('Checkout'){
            steps {
                // Explicitly poll will be excuted on below repo
                git url: 'https://github.com/kumarianu264-arch/DemoProject.git', 
                    branch: 'main', 
                    credentialsId: 'apps_github' 
            }
        }

       stage('A') {
          steps {
                echo "This is A stage test poll SCM"
          }
       } 

        stage('B') {
            steps {
                script {
                    try { 
                        sh 'exit 1'
                    } catch(e) {
                        echo "Caught an error: ${e}"
                    } 
                }
            }
        }

        stage('C') {
            steps {
                echo "Continue to next stages"
            }
        }

        stage('D') {
            steps {
                echo "Continue to next stages"
            }
        }
      
    }   

}