pipeline {
    agent { label 'built-in' }

    stages {
        stage('Run on Built-In Node') {
            steps {
                sh '''
                    echo "Running on Built-In Node"
                    hostname
                    echo "Node: $NODE_NAME"
                '''
            }
        }
    }
}
