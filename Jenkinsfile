pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', 
                    url: 'https://github.com/yourname/repo.git',
                    credentialsId: 'github-creds'
            }
        }
        stage('Build') {
            steps {
                sh 'mvn clean package'  // Replace with your build command
            }
        }
        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }
    }
}