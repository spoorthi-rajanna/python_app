pipeline {
    agent any
    stages {
        stage('Build') {
            agent {
                docker {
                    image 'python:3-alpine'
                }
            }
            steps {
                sh 'pip install --user -r requirements.txt'
                sh 'python index.py'
            
            }
        }
    }
}

