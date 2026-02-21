pipeline {
    agent any

    parameters {
        password(
            name: 'DEPLOY_PASSWORD',
            defaultValue: '',
            description: 'Enter deployment password'
        )
    }

    stages {
        stage('Example') {
            steps {
                echo "Password is ${params.DEPLOY_PASSWORD}"
            }
        }
    }
}
