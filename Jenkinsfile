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
            input {
                message "Want ot archive "
                ok "Yes, I am"
            }
            steps {
               archiveArtifacts artifacts: '**/*.war'
            }
        stage('Deploy to QA') { 
            steps {
               build job: "Deploy_to_Tomcat"
            }  
        }
    }
}
