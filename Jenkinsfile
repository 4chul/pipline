pipeline {
    agent any
    stages {
        stage('Clone Repository') {
            steps {
                git branch: 'main', url: 'https://github.com/4chul/pipline.git'
            }
        }
        stage('Build') {
            steps {
                sh 'echo "Build stage"'
            }
        }
        stage('Test') {
            steps {
                sh 'echo "Test stage"'
            }
        }
        stage('Deploy') {
            steps {
                sh 'echo "Deploy stage"'
            }
        }
    }
}
