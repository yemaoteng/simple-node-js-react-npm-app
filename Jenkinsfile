pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    docker.image('node:14-alpine').inside {
                        sh 'npm install'
                    }
                }
            }
        }
        stage('Test') {
            steps {
                script {
                    docker.image('node:14-alpine').inside {
                        sh 'npm test'
                    }
                }
            }
        }
    }
}
