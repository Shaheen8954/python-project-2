@Library("Shared") _
pipeline {
    agent any

    stages {
        stage('Clone repo') {
            steps {
                clone()
            }
        }
        stage('Build image') {
            steps {
                sh "docker build -t python-project ."
            }
        }
        stage('Run container') {
            steps {
               sh "docker run -d -p 9001:9001 python-project"
            }
        }
    }
}
