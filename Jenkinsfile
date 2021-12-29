pipeline {
    agent any
  
    stages {
        stage('pull git code') {
            steps { 
                git branch: "${params.tag}",
                credentialsId: 'vijaymanikanta180',
                url: 'https://github.com/vijaymanikanta180/finalassessment.git' 
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
