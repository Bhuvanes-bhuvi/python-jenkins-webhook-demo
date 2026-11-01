
pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                echo 'Getting source code from GitHub'
            }
        }

        stage('Check Python') {
            steps {
                bat 'python --version'
            }
        }

        stage('Install Dependencies') {
            steps {
                bat 'python -m pip --version'
            }
        }

        stage('Run Python Tests') {
            steps {
                bat 'python -m unittest discover -s tests -v'
            }
        }

        stage('Build Success') {
            steps {
                echo 'Python application build completed successfully!'
            }
        }
    }
}
