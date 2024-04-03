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
               bat ''' timeout /t 120 /nobreak  > NUL '''
               build job: 'Deploy_to_Tomcat', wait: true
            }  
        }
    }
}
