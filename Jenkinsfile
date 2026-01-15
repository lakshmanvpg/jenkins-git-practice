pipeline {
    agent any

    stages {
        stage('Stage 1 - Checkout') {
            steps {
                echo 'Code checked out from Git'
            }
        }

        stage('Stage 2 - Read File') {
            steps {
                echo 'Reading hello.txt file'
                bat 'type hello.txt'
            }
        }

        stage('Stage 3 - Done') {
            steps {
                echo 'Pipeline completed successfully'
            }
        }
    }
}
