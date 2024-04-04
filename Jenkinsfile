pipeline {
    agent any 
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
        stage('Deploy to QA') { 
            steps {
               echo "deploy to QA"
            }  
        }
    }
}
