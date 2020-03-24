pipeline {
    agent any
    stages {
        stage('Build') { 
            agent {
                docker {
                    image 'python:2-alpine' 
                }
            }
            steps {
                sh 'python -m py_compile index.py' 
                stash(name: 'compiled-results', includes: 'index.py*') 
            }
        }
    }
}

