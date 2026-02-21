pipeline {
    agent any

    stages {

        stage('Update packages on remote server') {
            steps {
                sh '''
                    ssh jenkins@20.219.1.181 << 'EOF'
                        echo "Updating packages"
                        sudo apt update
                    EOF
                '''
            }
        }

        stage('Install Nginx on remote server') {
            steps {
                sh '''
                    ssh jenkins@20.219.1.181 << 'EOF'
                        echo "Installing Nginx"
                        sudo apt install nginx -y
                    EOF
                '''
            }
        }

        stage('Start & Verify Nginx') {
            steps {
                sh '''
                    ssh jenkins@20.219.1.181 << 'EOF'
                        echo "Starting Nginx"
                        sudo systemctl start nginx
                        sudo systemctl enable nginx

                        echo "Verifying Web Server"
                        curl -I http://localhost
                    EOF
                '''
            }
        }
    }
}
