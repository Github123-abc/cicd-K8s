pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh "docker build -t static:1 ."
            }
        }
    }
}
