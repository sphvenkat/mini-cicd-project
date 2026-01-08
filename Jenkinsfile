pipeline {
    agent any

    stages {
        stage('Triggered from GitHub') {
            steps {
                sh '''
                echo "CICD testing project"
                whoami
                pwd
                ls -la
                '''
            }
        }
    }
}
