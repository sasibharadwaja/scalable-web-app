pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                script {
                    sh 'npm install'
                }
            }
        }
        stage('Test') {
            steps {
                script {
                    sh 'npm test' 
                }
            }
        }
        stage('Deploy') {
            steps {
                script {
                    sh 'docker build -t scalable-web-app .'
                    sh 'docker run -d -p 3000:3000 scalable-web-app'
                }
            }
        }
    }
}
