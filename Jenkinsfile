pipeline {
    agent {
        docker {
            image 'node:18.18.0-alpine3.18'
            args '-p 3200:3200'
        }
    }
    stages {
        stage('Build') {
            steps {
                sh 'npm install'
                sh 'ng serve --port=3200'
            }
        }
    }
}