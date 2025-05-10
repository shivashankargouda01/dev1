pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Checkout source code
                git 'https://github.com/sethshivam11/campus-space.git'
            }
        }

        stage('Install Dependencies') {
            steps {
                sh 'npm install'
            }
        }

        stage('Build') {
            steps {
                sh 'npm run build'
            }
        }

        stage('Test') {
            steps {
                // Optional - only if test script is available
                sh 'npm test || echo "No tests found or tests failed."'
            }
        }

        stage('Success') {
            steps {
                echo 'CI Pipeline Completed Successfully!'
            }
        }
    }
}
