pipeline {
    agent any

    options {
        timeout(time: 1, unit: 'MINUTES')
    }

    stages {
        stage('Example') {
            steps {
                echo "Hello"
                sh 'exit 1' 
                
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
        }
        aborted {
        echo "Build was aborted"
    }
    }
}
