pipeline {
    agent any

    stages {
        stage('Triggered from GitHub') {
            steps {
                sh '''
                echo "CICD testing project"
                echo "Second commit"
                whoami
                pwd
                ls -la
                '''
            }
        }
    }
}
