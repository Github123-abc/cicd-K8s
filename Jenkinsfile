pipeline {
    agent any

    stages {
        stage('docker') {
            steps {
                sh 'sudo docker build -t static:1 .'
               
            }
        }
        stage('ecr') {
            steps {
                sh 'sudo aws ecr-public get-login-password --region us-east-1 | sudo docker login --username AWS --password-stdin public.ecr.aws/c6e9q6u8'
                sh 'sudo docker build -t cicd:latest public.ecr.aws/c6e9q6u8/cicd:latest .'
                sh 'sudo docker push public.ecr.aws/c6e9q6u8/cicd:latest'
               
            }
        }
    }
}