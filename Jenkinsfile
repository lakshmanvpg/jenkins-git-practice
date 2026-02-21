pipeline {
    agent any

    options {
        timeout(time: 1, unit: 'MINUTES')
    }

    stages {
        stage('Example') {
            steps {
                echo "Hello"
                               
            }
        }
    }
    post {
        changed {
            echo "Build result changed from last run"
        }
        success {
            echo "Build succeeded"
        }

        failure {
            echo "Build failed"
                    }

        always {
            echo "This always runs"
            cleanWs()
        }
        aborted {
        echo "Build was aborted"
    }
    }
}
