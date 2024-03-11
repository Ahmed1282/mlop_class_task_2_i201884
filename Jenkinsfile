pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
                script {
                    git branch: 'main', url: 'https://github.com/Ahmed1282/mlop_class_task_2_i201884.git'
                }
            }
        }
        
        stage('Set up Python') {
            steps {
                script {
                    // Assuming Python is already installed in your Jenkins environment
                    sh 'python3.x --version' // Check Python version
                }
            }
        }
        
        stage('Install dependencies') {
            steps {
                script {
                    sh 'make install'
                }
            }
        }
        
        stage('Run tests') {
            steps {
                script {
                    sh 'make test'
                }
            }
        }
    }
}
