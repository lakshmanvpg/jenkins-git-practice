pipeline {
    agent any

    parameters {
        choice(name: 'ENV', choices: ['dev', 'qa', 'prod'])
        booleanParam(name: 'STOP_TOMCAT', defaultValue: false)
    }

    stages {
        stage('Stop Tomcat') {
            when {
                expression { params.STOP_TOMCAT }
            }
            steps {
                script {

                    def tomcatMap = [
                        dev  : "/opt/tomcat-dev",
                        qa   : "/opt/tomcat-qa",
                        prod : "/opt/tomcat-prod"
                    ]

                    env.TOMCAT_PATH = tomcatMap[params.ENV]

                    echo "Environment: ${params.ENV}"
                    echo "Stopping Tomcat at ${env.TOMCAT_PATH}"

                    sh "${env.TOMCAT_PATH}/bin/shutdown.sh"
                }
            }
        }
    }
}
