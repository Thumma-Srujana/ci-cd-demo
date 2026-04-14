pipeline {
    agent any

    stages {
        stage('Build Docker Image') {
            steps {
                sh 'docker build -t ci-cd-demo .'
            }
        }

        stage('Run Container') {
            steps {
                sh '''
                docker stop app || true
                docker rm app || true
                docker run -d -p 3000:3000 --name app ci-cd-demo
                '''
            }
        }
    }
}