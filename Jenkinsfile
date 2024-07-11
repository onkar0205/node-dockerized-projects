pipeline {
    agent any
    stages{
        stage("checkout"){
            steps{
            checkout scm
            }
        }
        stage("Text"){
            steps{
                sh 'apt install npm'
                sh 'npm test'
            }
        }
        stage("Build") {
            steps{
                sh 'npm run build'
            }
        }
    }
}