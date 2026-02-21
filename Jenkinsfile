pipeline {
    agent any

    options {
        timeout(time: 1, unit: 'MINUTES')
    }

    stages {
        stage('Example') {
            steps {
                echo "Hello"
                sleep 70
            }
        }
    }
    post {
        success {
            echo "Build succeeded"
        }

        failure {
            echo "Build failed"
        }

        always {
            echo "This always runs"
        }
        aborted {
        echo "Build was aborted"
    }
    }
}
