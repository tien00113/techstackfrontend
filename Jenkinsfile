pipeline {
    agent any
    stages{
        stage('Clone'){
            steps {
                git branch: 'main', credentialsId: 'github', url: 'https://github.com/tien00113/techstackfrontend.git'
            }
        }
    }
}