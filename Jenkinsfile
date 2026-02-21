pipeline {
    agent { label 'agent1' }

    stages {
        stage('Verify Agent') {
            steps {
                sh '''
                    echo "Running on Agent"
                    hostname
                    whoami
                    pwd
                '''
            }
        }
    }
}
