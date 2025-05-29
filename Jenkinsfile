pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                echo 'Cloning the repository...'
                checkout scm
            }
        }

        stage('Install Python') {
            steps {
                echo 'Checking Python version...'
                sh 'python3 --version || python --version'
            }
        }

        stage('Run Python Script') {
            steps {
                echo 'Running Python script...'
                sh 'python3 hello.py || python hello.py'
            }
        }
    }

    post {
        success {
            echo 'Python script executed successfully!'
        }
        failure {
            echo 'Something went wrong.'
        }
    }
}
