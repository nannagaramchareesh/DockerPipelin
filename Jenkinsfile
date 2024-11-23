pipeline {
    agent any 

    stages {
        stage('Build') {
            steps {
                script {
                    bat 'docker build -t my-nodejs-app .'
                }
            }
        }
        stage('container') {
            steps {
                script {
                    bat 'docker run -d -p 8083:3000 my-nodejs-app'
                }
            }
        }
    }
}