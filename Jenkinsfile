pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/<your-username>/<repo-name>.git'
            }
        }
        stage('Install') {
            steps {
                bat 'npm install'
            }
        }
        stage('Build') {
            steps {
                bat 'echo "No build script, skipping..."'
            }
        }
        stage('Test') {
            steps {
                bat 'npm test'
            }
        }
        stage('Archive') {
            steps {
                archiveArtifacts artifacts: '**/*', onlyIfSuccessful: true
            }
        }
    }
}
