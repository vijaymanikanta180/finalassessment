pipeline {
    agent any
  
    stages {
        stage('pull git code') {
            steps { 
                git branch: 'branchversion1',
                credentialsId: 'vijaymanikanta180',
                url: 'https://github.com/vijaymanikanta180/finalassessmentversion2.git' 
            } 
        }
       
        stage('Build docker') {
            steps {
                // Run docker
                sh "docker build -t apache2:1.0 ."
                sh "docker run -itd -p 81:80 apache2:1.0"                
            }
        }
    }
}
