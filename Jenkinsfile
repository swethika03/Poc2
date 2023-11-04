pipeline {
    environment {
       AWS_ACCESS_KEY_ID     = credentials('AWS_ACCESS_KEY_ID')
       AWS_SECRET_ACCESS_KEY = credentials('AWS_SECRET_ACCESS_KEY')
    }
agent any
      stages {

        stage('Checkout Git') {
            steps {
               git branch: 'main', url: 'https://github.com/swethika03/Poc2.git'
        }

        }

            stage('terraform init') {
            steps {
                sh 'terraform init'
                }
              }
         stage('terraform plan') {
            steps {
                sh 'terraform plan'
            }
        }
        stage('terraform apply') {
            steps {
                sh 'terraform apply --auto-approve'
            }
        }
    }
} 
