pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                echo 'Cloning repository...'
                git url: 'https://github.com/your-username/your-repo.git', branch: 'main'
            }
        }

        stage('Build') {
            steps {
                echo 'Running basic validation (optional)...'
                // e.g., validate HTML or check JS syntax
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying application...'
                // Example: Copy files to a web server directory
                sh '''
                    rm -rf /var/www/html/*
                    cp -r * /var/www/html/
                '''
            }
        }
    }

    post {
        success {
            echo 'Deployment successful.'
        }
        failure {
            echo 'Deployment failed or passed.'
        }
    }
}
