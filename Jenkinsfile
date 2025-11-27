pipeline {
    agent any

    stages {
        stage('Clone Repo') {
            steps {
                git 'https://github.com/salmasulthana2010/devops-java-pipeline.git'
            }
        }

        stage('Build Java App') {
            steps {
                sh 'javac App.java'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t devops-java-app .'
            }
        }

        stage('Run Docker Container') {
            steps {
                sh 'docker run devops-java-app'
            }
        }
    }
}
