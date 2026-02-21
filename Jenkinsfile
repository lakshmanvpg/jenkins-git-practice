pipeline {
    agent any

    parameters {
        choice(
            name: 'ENV',
            choices: ['dev', 'qa', 'prod'],
            description: 'Select environment'
        )
    }

    stages {
        stage('Stop Tomcat') {
            steps {
                script {

                    if (params.ENV == "dev") {
                        env.TOMCAT_PATH = "/opt/tomcat-dev"
                    }
                    else if (params.ENV == "qa") {
                        env.TOMCAT_PATH = "/opt/tomcat-qa"
                    }
                    else if (params.ENV == "prod") {
                        env.TOMCAT_PATH = "/opt/tomcat-prod"
                    }

                    echo "Stopping Tomcat in ${params.ENV}"
                    echo "Path: ${env.TOMCAT_PATH}"

                    sh """
                        ${env.TOMCAT_PATH}/bin/shutdown.sh
                    """
                }
            }
        }
    }
}
