pipeline {
    agent {
        docker {
            image 'IMAGE_NAME:TAG'
            args '-v /var/run/docker.sock:/var/run/docker.sock'
        }
    }
    stages {
        stage('Build') {
            steps {
                sh 'docker build ...'
            }
        }
        stage('Test') {
            steps {
                sh 'docker run ...'
            }
        }
        stage('Deploy') {
            steps {
                sh 'docker push ...'
            }
        }
    }
}