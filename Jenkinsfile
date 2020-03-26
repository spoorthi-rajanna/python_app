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
               sh 'pip install --user spoorthiraj1919 -r requirements.txt'
                sh 'python index.py'
            
            }
        }
    }
}

