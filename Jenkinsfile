pipeline {

    agent any

    stages {

        stage('Clone') {
            steps {
                echo 'Cloning Project'
            }
        }

        stage('Build Docker Image') {
            steps {
                bat 'docker build -t foodwebsite .'
            }
        }

        stage('Run Docker Container') {
            steps {
                bat 'docker rm -f foodwebsite || exit 0'
                bat 'docker run -d -p 8080:80 --name foodwebsite foodwebsite'
            }
        }

    }
}