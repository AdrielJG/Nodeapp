pipeline {
    agent any
    
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
