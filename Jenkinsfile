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
                sh 'docker build -t my-node-app:1.0 .'
            }
        }
        stage('Docker Push') {
            steps {
                sh 'docker login -u ${DOCKERHUB_USERNAME} -p ${DOCKERHUB_PASSWORD}'
                sh 'docker tag my-node-app:1.0 naikonkar0205/my-node-app:1.0'
                sh 'docker push naikonkar0205/my-node-app:1.0'
                sh 'docker logout'
            }
        }
    }
}
