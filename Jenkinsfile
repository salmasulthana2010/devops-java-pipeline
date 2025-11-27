pipeline {
    agent any

    stages {

        stage('Clone Repository') {
            steps {
                git branch: 'main', 
                url: 'https://github.com/salmasulthana2010/devops-java-pipeline.git'
            }
        }

        stage('Build Java Application') {
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
                sh 'docker run --rm devops-java-app'
            }
        }
    }
}
