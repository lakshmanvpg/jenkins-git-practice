pipeline {
    agent any

    parameters {
        text(
            name: 'DEPLOY_NOTES',
            defaultValue: 'Enter deployment notes here...',
            description: 'Provide release details'
        )
    }

    stages {
        stage('Print Notes') {
            steps {
                echo "Notes:"
                echo "${params.DEPLOY_NOTES}"
            }
        }
    }
}
