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
                echo 'Building java application'
                bat 'java -m py_compile test.java'
            }
        }

        stage('Test') {
            steps {
                echo 'Executing automated tests'
                bat 'java -m unittest app'
            }
        }

        stage('Run Application') {
            steps {
                bat 'java test.java'
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
