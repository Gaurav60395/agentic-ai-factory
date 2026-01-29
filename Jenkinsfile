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
                // Check if requirements.txt exists before installing
                script {
                    if (fileExists('requirements.txt')) {
                        sh 'pip install -r requirements.txt'
                    } else {
                        echo 'No requirements.txt found, skipping dependency installation.'
                    }
                }
            }
        }
        stage('Run Tests') {
            steps {
                // Check if tests exist before running
                script {
                    if (fileExists('tests/')) { // Assuming tests are in a 'tests' directory
                        sh 'pytest'
                    } else {
                        echo 'No tests found, skipping test execution.'
                    }
                }
            }
        }
    }
}
