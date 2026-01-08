pipeline {
    agent any

    stages {

        stage('Checkout Code') {
            steps {
                checkout scm
            }
        }

        stage('Deploy to Nginx') {
            steps {
                sh '''
                echo "Deploying application..."
                sudo rm -rf /usr/share/nginx/html/*
                sudo cp index.html /usr/share/nginx/html/
                sudo systemctl reload nginx
                '''
            }
        }
    }

    post {
        success {
            echo 'Pipeline executed successfully'
        }
        failure {
            echo 'Pipeline failed'
        }
    }
}
