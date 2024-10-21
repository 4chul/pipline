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

node {
    stage('SCM') {
        checkout scm
    }
    stage('SonarQube Analysis') {
        def scannerHome = tool 'SonarScanner';  // название инструмента, которое вы указали в Jenkins
        withSonarQubeEnv('SonarQube') {  // название SonarQube сервера, которое вы указали
            sh "${scannerHome}/bin/sonar-scanner"
        }
    }
}
