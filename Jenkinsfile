pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Build') {
            steps {
                echo 'Building the application...'
                // Example: sh 'mvn clean package' or npm install
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
                // Example: sh 'mvn test'
            }
        }

        stage('Deploy') {
            when { branch 'main' }
            steps {
                echo 'Deploying application...'
            }
        }
    }

    post {
        always {
            echo 'Pipeline completed!'
        }
    }
}
