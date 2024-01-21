pipeline {
    agent any

    triggers {
        // poll SCM every 5 minutes
        pollSCM('*/5 * * * *')
    }
    
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
                // will be replaced with docker build commands
            }
        }
        stage('Test') {
            steps {
                echo 'Test'
                bat 'docker run hello-world'
                // run tests
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploy'
                // deploy commands
            }
        }
    }
}
