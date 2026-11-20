     stage('Build') {
            steps {
                echo 'Building java application'
                bat 'java -m py_compile test.java'
                echo 'Building Java application'
                bat 'javac test.java'
            }
        }

        stage('Test') {
            steps {
                echo 'Executing automated tests'
                bat 'java -m unittest app'
                echo 'Testing Java application'
            }
        }

        stage('Run Application') {
            steps {
                bat 'java test.java'
                echo 'Running Java application'
                bat 'java test'
            }
        }
    }
 pipeline {
        success {
            echo 'CI pipeline completed successfully'
        }

        failure {
            echo 'CI pipeline failed'
        }
    }
}
