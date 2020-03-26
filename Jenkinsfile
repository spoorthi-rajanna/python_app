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
                withEnv(["HOME=${env.WORKSPACE}"]) {
               sh 'pip install --user -r requirements.txt'
                sh 'python index.py'
                }
            }
            stage('test') {
      steps {
        sh 'python test.py'
      }
        }
    }
}

