pipeline {
    agent any
    
    tools {
        nodejs 'NodeJS-18'
    }

    stages {

        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/AdrielJG/Nodeapp.git'
            }
        }

        stage('Install Dependencies') {
            steps {
                bat 'npm install'
            }
        }

        stage('Test') {
            steps {
                bat 'echo No tests configured'
            }
        }

        stage('Build') {
            steps {
                bat 'echo Build successful'
            }
        }

        stage('Deploy') {
            steps {
                bat '''
                taskkill /IM node.exe /F 2>nul
                start cmd /c "npm start"
                '''
            }
        }
    }
}
