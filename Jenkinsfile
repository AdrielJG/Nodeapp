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
                dir('nodeapp') {
                    bat 'npm install'
                }
            }
        }

        stage('Build') {
            steps {
                dir('nodeapp') {
                    bat 'echo Build successful'
                }
            }
        }

        stage('Deploy') {
            steps {
                dir('nodeapp') {
                    bat '''
                    taskkill /IM node.exe /F 2>nul
                    start cmd /c "npm start"
                    '''
                }
            }
        }
    }
}
