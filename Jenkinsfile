pipeline {

    agent any

    stages {

        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('System Information') {
            steps {
                sh 'echo "Current User: $(whoami)"'
                sh 'echo "Current Directory: $(pwd)"'
                sh 'echo "Git Version:"'
                sh 'git --version'
                sh 'echo "Node Version:"'
                sh 'node -v'
                sh 'echo "NPM Version:"'
                sh 'npm -v'
            }
        }

        stage('Repository Contents') {
            steps {
                sh 'ls -la'
            }
        }

        stage('Success') {
            steps {
                sh 'echo "Repository cloned successfully!"'
            }
        }

    }

}