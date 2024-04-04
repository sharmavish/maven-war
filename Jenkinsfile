pipeline {
    agent any 
     triggers {
        pollSCM('* * * * *')
     }
    stages {
        stage('clean') { 
            steps {
               echo "clean"
            }
        }
        stage('build') { 
            steps {
               echo " build"
            }
        }
        stage('archive') { 
            steps {
               echo "Archive"
            }
        }   
        stage('Deploy to dev') { 
            steps {
               echo "deploy to dev"
            }  
        }
        stage('Deploy to QA') { 
            steps {
               echo "deploy to QA"
            }  
        }
        stage('Deploy to prod') { 
            steps {
               echo "deploy to prod"
            }  
        }
    }
}
