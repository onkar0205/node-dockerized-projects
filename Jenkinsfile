pipeline {
    agent any
    stages {
        stage("checkout") {
            steps {
                checkout scm
            }
        }
        stage("Text") {
            steps {
                sh 'npm test'
            }
        }
        stage("Build") {
            steps {
                sh 'npm run build'
            }
        }
        stage("Build Image") {
            steps {
                sh 'Docker build -t my-node-app:1.0'
            }
        }
    }
}
