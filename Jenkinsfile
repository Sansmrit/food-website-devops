pipeline {

    agent any

    stages {

        stage('Build Docker Image') {
            steps {
                bat 'docker build -t foodwebsite .'
            }
        }

        stage('Deploy Using Ansible') {
            steps {
                bat 'wsl ansible-playbook /mnt/c/ProgramData/Jenkins/.jenkins/workspace/FoodWebsitePipeline/deploy.yml'
            }
        }

    }
}