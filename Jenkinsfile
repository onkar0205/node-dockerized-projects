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
                sh 'echo "iauro100" | sudo -S apt install npm'
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