pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                git 'https://github.com/kibo10/jenkins-test.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t myapp:latest .'
            }
        }

        stage('Deploy') {
            steps {
                sh '''
                    docker stop myapp || true
                    docker rm myapp || true
                    docker run -d --name myapp -p 3000:3000 myapp:latest
                '''
            }
        }
    }
}
