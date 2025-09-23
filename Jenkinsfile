pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/<your-username>/<your-repo>.git'
            }
        }
        stage('Build') {
            steps {
                sh 'pip install -r requirements.txt'
            }
        }
        stage('Test') {
            steps {
                sh 'echo "Running tests..."'
                sh 'python -m py_compile app.py'
            }
        }
        stage('Deploy') {
            steps {
                sh 'echo "Starting app..."'
                sh 'python app.py &'
            }
        }
    }
}
