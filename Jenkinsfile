pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'sudo docker build -t static:1 .'
            }
        }
    }
}
