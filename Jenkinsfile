pipeline {
    agent any 

    stages {
        stage('Checkout') {
            steps {
                // Checkout the code from the repository
                git 'https://your-repo-url.git'
            }
        }
        stage('Install Dependencies') {
            steps {
                // Install dependencies (if any)
                sh 'pip install -r requirements.txt'
            }
        }
        stage('Run Tests') {
            steps {
                // Run tests (if any)
                sh 'pytest'
            }
        }
    }
}
