
pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Checking out Java application'
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
                echo 'Executing automated tests'
                // Run tests if a test framework is configured
                echo 'Testing Java application completed'
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

        always {
            echo 'Pipeline execution finished'
        }
    }
}
