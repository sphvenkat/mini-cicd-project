pipeline {
    agent any

    stages {
        stage('Clone Code') {
            steps {
                echo 'Cloning source code from GitHub'
            }
        }

        stage('Deploy to Nginx') {
            steps {
                sh '''
                echo "Deploying website..."
                sudo rm -rf /usr/share/nginx/html/*
                sudo cp -r index.html /usr/share/nginx/html/
                sudo systemctl reload nginx
                '''
            }
        }
    }

    post {
        success {
            echo 'Deployment completed successfully!'
        }
        failure {
            echo 'Deployment failed!'
        }
    }
}
