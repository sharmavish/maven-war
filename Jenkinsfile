pipeline {
    agent any 
    stages {
        stage('clean') { 
            steps {
               sh 'mvn clean'
            }
        }
        stage('build') { 
            steps {
               sh 'mvn package'
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
        }
    }
}
