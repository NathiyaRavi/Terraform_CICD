pipeline {
    agent any

    stages {
        stage('GIT Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/NathiyaRavi/Terraform_CICD.git'
            }
        }
        stage('Terraform Init') {
            steps {
                sh 'terraform init'
            }
        }
        stage('Terraform Plan') {
            steps {
                sh 'terraform plan'
            }
        }
        stage('Print Env Value') {
            steps {
                echo "Environment is: ${params.environment}"
            }
        }
        
    }
}
