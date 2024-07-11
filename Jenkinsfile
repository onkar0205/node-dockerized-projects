pipeline {
    agent any
    stage{
        stage()"checkout"){
            steps{
            checkout scm
            }
        }
        stage("Text"){
            steps{
                sh 'sudo apt install npm'
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