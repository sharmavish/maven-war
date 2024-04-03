pipeline {
    agent any 
    stages {
        stage('clean') { 
            steps {
               bat 'mvn clean'
            }
        }
        stage('build') { 
            steps {
               bat 'mvn package'
            }
        }
        stage('archive') { 
            steps {
               archiveArtifacts artifacts: '**/*.war'
            }
        }   
        stage('Deploy to QA') { 
            steps {
               sh 'sleep 120' 
               build job: 'Deploy_to_Tomcat', wait: true
            }  
        }
    }
}
