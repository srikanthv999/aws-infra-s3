pipeline {
    agent any

    stages {
        stage('TF-Init') {
            steps {
                echo 'Run Terraform plan to perform the DRY run'
                sh 'terraform init'
            }
        }
      
        stage('TF-Plan') {
            steps {
                echo 'Run Terraform plan to perform the DRY run'
                sh 'terraform plan'
            }
        }
         stage('TF-Apply') {
            steps {
                echo 'Run the Terraform apply to create the infrastructure '
                sh 'terraform apply -auto-approve'
            }
        }
    }
}