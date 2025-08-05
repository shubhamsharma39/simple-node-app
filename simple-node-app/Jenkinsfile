pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/shubhamsharma39/simple-node-app.git'
            }
        }

        stage('Build') {
            steps {
                sh 'docker build -t simple-node-app .'
            }
        }

        stage('Test') {
            steps {
                sh 'echo "No tests to run."'
            }
        }

        stage('Deploy') {
            steps {
                sh 'docker run -d -p 3000:3000 --name simple-node-app simple-node-app || echo "Container already running."'
            }
        }
    }
}
