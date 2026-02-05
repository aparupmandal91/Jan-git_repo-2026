pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/aparupmandal91/Jan-git_repo-2026.git'
            }
        }

        stage('Install Dependencies') {
            steps {
                sh '''
                python3 -m venv venv
                . venv/bin/activate
                pip install -r requirements.txt
                '''
            }
        }

        stage('Test') {
            steps {
                sh '''
                . venv/bin/activate
                pytest
                '''
            }
        }
    }
}

