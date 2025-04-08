pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                // Lệnh này sẽ kéo toàn bộ source code từ Git repository
                checkout scm
            }
        }
        stage('Build') {
            steps {
                withDockerRegistry(credentialsId: 'jenkin2', url: 'https://index.docker.io/v1/') {
                    sh '''docker build -t haitran001/jenkinsnet-v1 ./Jenkins
                        docker push -t haitran001/jenkinsnet-v1
                        '''
                }
            }
        }
    }
}