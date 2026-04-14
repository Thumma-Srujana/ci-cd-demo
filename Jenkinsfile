pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                echo 'Code pulled from GitHub'
            }
        }

        stage('Install') {
            steps {
                sh 'npm install'
            }
        }

        stage('Run App') {
            steps {
                sh 'node app.js &'
            }
        }
    }
}