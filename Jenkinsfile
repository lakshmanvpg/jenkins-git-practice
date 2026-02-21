pipeline {
    agent any

    stages {

        stage('login to Remote Server') {
            steps {
                sh '''
                    ssh jenkins@20.219.1.181 
                    '''}
        }
        stage('updating the pkg') {
            steps {
                sh '''
                        echo "Updating packages"
                        sudo apt update
                    '''
            }
        }
      stage('installing  the Nginx') {
            steps {
                sh '''
                        echo "Installing Nginx"
                        sudo apt install nginx -y
                    '''
            }
      }
     stage('installing  the Nginx') {
            steps {
                sh '''
                        echo "Starting Nginx"
                        sudo systemctl start nginx
                        sudo systemctl enable nginx

                        echo "Verifying Web Server"
                        curl -I http://localhost

                  '''
            }
     }
            }
        }
    
