pipeline {
    agent any
    stages {
        stage('Build') { 
            
            steps {
                sh 'python -m py_compile index.py' 
                stash(name: 'compiled-results', includes: 'index.py*') 
            }
        }
    }
}

