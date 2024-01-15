pipeline {
    agent any

    stages {
        stage('Clone Code') {
            steps {
                cleanWs()
                echo 'Show Workspace'
                bat 'git clone https://github.com/mydadisalive/devops-course-2024.git'
            }
        }
        stage('Build') {
            steps {
                echo 'Build'
                bat 'docker pull hello-world'
            }
        }
        stage('Test') {
            steps {
                echo 'Test'
                bat 'docker run hello-world'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploy'
            }
        }
    }
}
