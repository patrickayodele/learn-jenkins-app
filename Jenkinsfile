pipeline {
    agent any
    stages {
        stage('Test') {
            steps {
                sh 'docker pull node:18-alpine'
                sh 'docker run --rm -v "$PWD:/app" -w /app node:18-alpine npm install'
                sh 'docker run --rm -v "$PWD:/app" -w /app node:18-alpine npm test'
            }
        }
        //...rest of your pipeline
    }
}