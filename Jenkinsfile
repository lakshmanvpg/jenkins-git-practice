pipeline {
    agent any

    stages {
        stage('Test Credentials') {
            steps {
                withCredentials([
                    usernamePassword(
                        credentialsId: 'github',
                        usernameVariable: 'USER',
                        passwordVariable: 'PASS'
                    )
                ]) {
                    sh '''
                        echo "Username is: $USER"
                        echo "Password is :$PASS"
                    '''
                }
            }
        }
    }
}
