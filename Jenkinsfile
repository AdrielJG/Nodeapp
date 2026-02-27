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

        stage('Run App') {
            steps {
                dir('nodeapp') {
                    bat 'node index.js'
                }
            }
        }
    }
}
