pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Build') {
            steps {
                echo 'Building Java application'
                bat 'javac test.java'
            }
        }

        stage('Test') {
            steps {
                echo 'Testing Java application'
            }
        }

        stage('Run Application') {
            steps {
                echo 'Running Java application'
                bat 'java test'
            }
        }
    }

    post {
        success {
            echo 'CI pipeline completed successfully'
        }
        failure {
            echo 'CI pipeline failed'
        }
    }
}

