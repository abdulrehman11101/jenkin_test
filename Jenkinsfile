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
        stage('Install Dependencies') {
            steps {
                sh 'npm install'  // Installs all package.json dependencies
            }
        }
        stage('Build') {
            steps {
                sh 'npm run build'  // Runs the "build" script from package.json
            }
        }
        stage('Test') {
            steps {
                sh 'npm test'  // Runs the "test" script from package.json
            }
        }
    }
}