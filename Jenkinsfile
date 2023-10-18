pipeline {
    agent {
        docker {
            image 'node:18.18.0-alpine3.18'
            args '-p 3000:3000'
        }
    }
    stages {
        stage('Build') {
            steps {
                sh 'npm install'
            }
        }
        stage('Deliver'){
            steps {
                sh 'set -x'
                sh 'npm run startV2'
                sh 'echo $! > .pidfile'
                sh 'set +x'
            }
        }
    }
}