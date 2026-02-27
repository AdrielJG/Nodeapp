pipeline {
    agent any
    
    tools {
        nodejs 'NodeJS-18'
    }

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/your-username/your-repo.git'
            }
        }

        stage('Install Dependencies') {
            steps {
                sh 'npm install'
            }
        }

        stage('Test') {
            steps {
                sh 'echo "No tests configured"'
            }
        }

        stage('Build') {
            steps {
                sh 'echo "Build successful"'
            }
        }

        stage('Deploy') {
            steps {
                sh '''
                pkill node || true
                nohup npm start &
                '''
            }
        }
    }
}
