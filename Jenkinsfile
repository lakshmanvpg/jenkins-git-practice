pipeline {
    agent any

    parameters {
        string(name: 'name', defaultValue: 'lakshman', description: 'Enter username')
        string(name: 'host', defaultValue: 'myserver', description: 'Enter servername')
    }

    stages {
        stage('Example') {
            steps {
                echo "myname is  ${params.username}"
                echo "servername is  ${params.hostname}"
                
            }
        }
    }
}
