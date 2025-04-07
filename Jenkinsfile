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
                echo 'Building..'
            }
        }
    }
}