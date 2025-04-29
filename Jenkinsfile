pipeline {
    agent any

    stages {
        stage('Clone repo') {
            steps {
                git url: "https://github.com/Shaheen8954/python-project-2.git", branch: "main"
            }
        }
        stage('Build image') {
            steps {
                sh "docker build -t python-project ."
            }
        }
        stage('Run container') {
            steps {
                docker run -d -p 9001:9001 python-project
            }
        }
    }
}
