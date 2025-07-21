pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', 
                    url: 'https://github.com/abdulrehman11101/jenkin_test',
                    credentialsId: 'b83b77f5-f4e1-4d8a-8b41-896c81213b9c'
            }
        }
        stage('Build') {
            steps {
                sh 'npm install'  // Replace with your build command
            }
        }
        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }
    }
}