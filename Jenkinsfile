pipeline {
    agent any
    
    stages {
        
        stage('clone code') {
            steps {
                git branch: 'main', url: 'https://github.com/vasanthp45/node-app.git'
            }
        }
        
        stage('Build Docker image') {
            steps {
                sh 'docker build -t node-app .'
            }
        }
        
        stage('Run Container') {
            steps {
                sh 'docker run -d -p 3000:3000 --name node-cont node-app'
            }
        }
    }
}
