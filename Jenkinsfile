pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }
        
        stage('Stop') {
            steps {
                sh 'docker-compose down || true'
            }
        }
        
        stage('Run') {
            steps {
                sh 'docker-compose up -d'
            }
        }
    }
}
