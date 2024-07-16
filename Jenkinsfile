pipeline {
    agent any
    stages{
        stage('Clone'){
            steps {
                git branch: 'main', credentialsId: 'github', url: 'https://github.com/tien00113/techstackfrontend.git'
            }
        }
        stage('Push Docker Hub'){
            steps {
                withDockerRegistry(credentialsId: 'dockerhub', url: '') {
                    sh label: '', script: 'docker build -t tien00113/techstack:latest .'
                    sh label: '', script: 'docker push tien00113/techstack:latest'
                    // sh label: '', script: 'docker push aaa'
                    // sh label: '', script: 'docker push tien00113/discovery'
                }
            }
        }
    }
}