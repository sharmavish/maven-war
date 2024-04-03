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
               bat ''' ping  -n 10 127.1.1.1 > nul '''
               build job: 'Deploy_to_Tomcat', wait: true
            }  
        }
    }
}
